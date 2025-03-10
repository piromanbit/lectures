## Теорема Рао-Крамера
$\hat{\theta}$ для неизвестного параметра $\theta$

Пусть
    1. $M \hat{\theta} = \int \cdots \int \hat{\theta} \ L(\vec{x_n}, \theta) \, dx_1 \cdots \, dx_n = \theta + \delta_{\hat{\theta}}(\theta)$
    2. Условия регулярности $p_\xi(x, \theta)$
    2.1. Область, где $p_\xi(x, \theta) \neq 0$ не зависимо от $\theta$
    2.2. В 1. и $\int L(\vec{x_n}, \theta) \, dx = 1$ возможно $\frac{\partial}{\partial \theta}$ под $\int$
    $\exists \frac{\partial L}{\partial \theta}(\vec{x}, \theta))$ и $L(\vec{x}, \theta) > 0$
    2.3. $I(\vec{x_n}, \theta) \neq 0$

Тогда $\forall$ оценки $\hat{\theta}(\vec{x_n})$ параметра $\theta$ имеет место неравенство.
    $$M(\hat{\theta}(\vec{x_n}) - \theta)^2 \geq \frac{\left[1 + \frac{\partial \delta_{\hat{\theta}}(\theta)}{\partial\theta}\right]^2}{I(\theta, \vec{x_n})}$$

$\Delta$:

> 1\. и 2. дифференцируемы по $\theta$ 
> 1. $$\implies \int \hat{\theta} \frac{\partial L(\vec{x}, \theta)}{\partial \theta} \, d\vec{x} = \int \left[\hat{\theta} \frac{\partial \ln L(\vec{x}, \theta)}{\partial \theta}\right] \cdot L(\vec{x}, \theta) \, d\vec{x} = M(\hat{\theta} \frac{\partial \ln L(\vec{x}, \theta) }{\partial \theta}) = 1 + \frac{\partial \delta(\theta)}{\partial \theta}$$
> 2. $$\implies \int \left[\frac{\partial \ln L(\vec{x}, \theta)}{\partial \theta}\right] L(\vec{x}, \theta) \, d\vec{x} = M\left[\frac{\partial \ln L(\vec{x}, \theta)}{\partial \theta}\right] = 0$$
> 1.-2. $\theta$: $$\int (\hat{\theta} - \theta) \frac{\partial \ln L(\vec{x}, \theta)}{\partial \theta} L(\vec{x}, \theta) \, d\vec{x} = 1 + \frac{\partial \delta_\hat{\theta}(\theta)}{\partial \theta}$$
> $$M\left[(\hat{\theta} - \theta) \frac{\partial \ln L(\vec{x}, \theta)}{\partial \theta} - M(\frac{\partial \ln L}{\partial \theta}\right] = 1 + \frac{\partial \delta_{\hat{\theta}}(\theta)}{\partial \theta}$$
> Неравенство Коши-Буняковского для математических ожиданий
> $$\left[M(\xi \cdot \eta)\right]^2 \leq M\xi^2 \cdot M\eta^2$$
> $$\left[1 + \frac{\partial \delta(\theta)}{\partial \theta}\right]^2 \leq M(\hat{ \theta} - \theta^2) M\left(\frac{\partial \ln L}{\partial \theta} - M \frac{\partial \ln L}{\partial \theta}\right)^2$$
> $$M(\hat{\theta} - \theta)^2 \geq \frac{\left[1 + \frac{\partial \delta(\theta)}{\partial \theta}\right]^2}{M\left[\frac{\partial \ln L}{\partial \theta}\right]^2}$$

□

Показатель эффективности: $e(\hat{\theta}) = \frac{D_\min}{D(\hat{\theta})}$
    Если $e(\hat{\theta}) = 1$, то $\hat{\theta}$ - эффективная
    Если $e(\hat{\theta}) \to 1, \ n \to \infty$, то $\hat{\theta}$ - ассимптотически эффективная

Все вышеперечисленные результаты справедливы для дискретного распределения:
    1. $p_\xi(x, \theta) = P(\xi = x, \theta)$
    2. $\int \to \sum$

<u>Пример:</u> 
    $$P(\xi = k) = \frac{\lambda^k e^{-\lambda}}{k!},\ k = 0, 1$$
    $$I(\vec{x_n}, \theta) = n I(x_1, \theta) = n \int \left[\frac{\partial \ln p_\xi(x, \theta)}{\partial \theta}\right]^2\cdot p_\xi(x, \theta) \, dx$$
    $$I(\vec{x_n}, \lambda = n \sum_{k = 0}^\infty \left[\frac{\partial \ln \frac{\lambda^k e^{-\lambda}}{k!}}{\partial \lambda}\right]^2 \frac{\lambda^k e^{-\lambda}}{k!} = n \sum_{k = 0}^\infty \left(\frac{k}{\lambda} - 1\right)^2 \frac{\lambda^k e^{-\lambda}}{k!} = n e^{-\lambda} \left[e^\lambda + \frac{1}{\lambda}e^\lambda - e^\lambda\right] = \frac{n}{\lambda} \implies D_\min = \frac{\lambda}{n}$$
    $$\bar{x} = \frac{1}{n}\sum_{i = 1}^n x_i \ \ \ \ D \bar{x} = \frac{1}{n^2}\sum_{i=1}^n Dx_i = \frac{D \xi}{n} = \frac{\lambda}{n} \implies e(\bar{x}) = 1$$

<u>Теорема</u> (Критерий эффективности несмещенной оценки)
    Пусть выполняются условия теорема Рао-Крамера
    $\hat{\theta}(\vec{x_n})$ - несмещенная оценка $\theta$
    Тогда $$(\hat{\theta}(\vec{x_n}) - эффективная) \iff \left(\frac{\partial \ln L(\vec{x}, \theta)}{\partial \theta} = A(\theta) \cdot(\hat{\theta} - \theta)\right)$$

## Метод статистического оценивания параметров
1. Максимального правдоподобия(ММП, МП)
    $L(\vec{x_n}, \theta) = p_\xi(x_1, \theta) \cdot \ldots \cdot p_\xi(x_n, \theta)$
    $\vec{x_n} = \{x_1, \ldots, x_n\}$ - выборка генеральной совокупности $\xi$ с $p_\xi(x, \theta)$
    $\hat{\theta}_\min(\vec{x_n}) = \arg\, \max L(\vec{x_n}, \theta)$
    Если $\hat{\theta} = \{\theta_1, \ldots, \theta_p\}$ - вектор оценки неизвестных параметров, то ММП оценки могут быть получены из $$\frac{\partial \ln L(\vec{x_n}, \vec{\theta})}{\partial \theta_i} = 0,\ i = 1, \ldots, p$$

2. Метод моментов
    $\vec{\theta} = \{\theta_1, \ldots, \theta_p\}$ вектор неизвестных параметров распределения случайной величины $\gamma$, $p_\gamma = (x, \vec{\theta})$
    $\hat{\theta}_MM$ находится из следующей системы,
    $$
    \begin{cases} 
        \nu_s(\theta_1, \ldots, \theta_p) = \hat{\nu_s}, \ s = 1, \ldots, p
        \\
        \nu_s(\theta_1, \ldots \theta_p) = M\xi^2 = \int x^s p_\xi(x, \vec{\theta}) \, dx
        \\
        \hat{\nu_s} = \frac{1}{n}\sum_{i = 1}^n x_i^s
    \end{cases}
    $$

3. Байевское оценивание параметров
    Особенности:
    1. Интерпретация вероятности события, как степени нашего доверия событию
    2. Для принятия решения в качестве исходной информации используется одновременно инфеормация двух типов:
        - Априорная информация о явлении(параметре, эксперименте)
        - Информация из статистических данных $\vec{x_n}$
    $p(\theta) \to p(\theta, \vec{x_n}^{(1)}) \to p(\theta, \vec{x_n}^{(2)})$

    Алгоритм байевского оценивания
    1. Сбор априорных сведений о параметре $\theta \implies p(\theta)$ - априорное распределение
        В случае нехватки априорной информации 
        $$p(\theta) = \frac{1}{\theta_\max - \theta_\min},\ \theta \in [\theta_\min,\ \theta_\max]$$
    2. Сбор статистических данных $x_1, x_2, \ldots, x_n \implies \vec{x_n}$ - выборка
    3. Функция правдоподобия 
        $$L(\vec{x_n} \mid \theta) = p_\xi(x_1 \mid \theta) \cdot \ldots \cdot p_\xi(x_n \mid \theta)$$
        $p_\xi(x \mid \theta)$ - функция плотности генеральной совокупности $\xi$ в предположении, что значение параметра $= 0$
    4. Апостериорное распределение значений параметра $\theta$
        $$p(\theta \mid \vec{x}) = \frac{p(\theta) \cdot L(\vec{x} \mid \theta)}{p(\vec{x_n})} = \frac{p(\theta)\ L(\vec{x_n} \mid \theta)}{\int L(\vec{x}, \theta)\ p(\theta) \, d\theta}$$
