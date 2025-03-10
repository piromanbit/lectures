### 3. Эффективность
$\xi$ - случайная величина, измеряем $n$ раз.
$\vec{x_n}^{(1)} = \{x_1^{(1)}, x_2^{(1)}, ..., x_n^{(1)}\} \implies (\hat{\theta_1}^{(1)}, \hat{\theta_2}^{(1)})$
$\vec{x_n}^{(2)} = \{x_1^{(2)}, x_2^{(2)}, ..., x_n^{(2)}\} \implies (\hat{\theta_1}^{(2)}, \hat{\theta_2}^{(2)})$
...
$\vec{x_n}^{(k)} = \{x_1^{(k)}, x_2^{(k)}, ..., x_n^{(k)}\} \implies (\hat{\theta_1}^{(k)}, \hat{\theta_2}^{(k)})$

![](/mathstat/lecture2/image1.jpg)

□ - значения оценок
    $\hat{\theta_1}^\ast$, $\hat{\theta_2}^\ast$ - смещенные оценки параметров $\theta_1$ и $\theta_2$
    $\hat{\theta_1}', \hat{\theta_2}'$ - другие точные оценки значений тех же параметров $\theta_1$ и $\theta_2$
    $\theta_1$, $\theta_2$ - точные значения

<u>Опр.</u> Оценка $\hat{\theta}(\vec{x_n})$ называется эффективной, если среди прочих оценок этого параметраона обладает наименьшей мерой разброса вокруг истинного значения параметра.
    Мера разброса: $M(\hat{\theta}(\vec{x_n}) - \theta)^2$
    Если $\hat{\theta}(\vec{x_n})$ - несмещенная $\implies M(\hat{\theta}(\vec{x_n}) - M(\hat{\theta}(\vec{x_n})))^2 = D \hat{\theta}(\vec{x_n})$

## Функция правдоподобия (ФП)
$\vec{x_n} = \{x_1, x_2, ..., x_n\}$ выборка из генеральной совокупности $\xi$ (выборка измерений СВ $\xi$)

Пусть $p_\xi(x, \theta)$ - плотность СВ $\xi$, если $\xi$ непрерывна, и $=P(\xi=x; \theta)$ - закон распределения $\xi$, если $\xi$ дискретно.
    $\theta$ - неизвестный параметр распределения СВ $\xi$
    $$L(\vec{x_n}, \theta) = p_\xi (x_1, \theta) p_\xi (x_2, \theta) \cdot ... \cdot p_\xi (x_n, \theta)$$
    Совместное распределение $\vec{x_n}$ (элементов выборки, которая зависит от неизвестного параметра $\theta$ распределения СВ $\xi$)

ФП $L(\vec{x_n}, \theta)$ показывает, насколько правдоподобны полученные измерения $x_1, ..., x_n$ случайной величины $\xi$ при данном значении параметра $\theta$.
    $L(\vec{x_n}, \theta) = f(\vec{x_n})$ - ситуация нелувой информации в $\vec{x_n}$ по $\theta$.

## Информация Фишера
<u>Опр.</u> Кол-во информации Фишера содержащейся в наблюдениях $\vec{x_n} = \{x_1, ..., x_n\}$ определяется следующим образом.
    $$I(\theta, \vec{x_n}) = M\left[\frac{\partial \ln L(\vec{x_n}, \theta)}{\partial \theta}\right]^2 = \int_{x_1} \cdots \int_{x_n} \left[\frac{\partial \ln L(\vec{x_n}, \theta)}{\partial \theta} \right]^2 \cdot L(\vec{x_n}, \theta) \, dx_1 ... dx_n$$
    1. $I(\theta, \vec{x_n}) = n \cdot \int_{x_1}  \left[\frac{\partial \ln p_\xi(x, \theta)}{\partial \theta}\right]^2 p_\xi(x_1, \theta)\, dx_1$ - т.к. $x_1, ..., x_n$ одинаково распределены и взаимно независимы

</u>Пример 1:</u>
    $\vec{x_n} = \{x_1, ..., x_n\}$, где $x_i \sim \mathcal{N}(a, \sigma^2)$
    $$I(a, \vec{x_n}) = n \int_{-\infty}^{+\infty} \frac{\partial \ln p_\xi(x, a, \sigma^2)}{\partial a} p_\xi(x, a, \sigma^2) \, dx = (1)$$
    $$p_\xi(x, a, \sigma^2) = \frac{1}{\sqrt{2\pi}\sigma}e^{-\frac{(x-a)^2}{2 \sigma^2}}$$
    $$\frac{\partial \ln p_\xi(x, a, \sigma^2)}{\partial a} = \frac{x - a}{\sigma^2}$$
    $$(1) = n \int_{-\infty}^{+\infty} \frac{1}{\sqrt{2 \pi} \sigma} e^{- \frac{(x - a) ^ 2}{2 \sigma^2}} \cdot \frac{(x - a)^2}{\sigma^4} \, dx = \left(\frac{x - a}{\sigma} = y\right) = \frac{n}{\sqrt{2 \pi}\sigma^2}\int_{-\infty}^{+\infty} y^2 e^{-y^2/2} \, dy = \frac{n}{\sigma^2}$$

## Неравенство Рао-Крамера-Фреше
Ищем нижнюю границу $M(\hat{\theta}(\vec{x_n}) - \theta)^2$, $\theta$ - неизвестный параметр распределения $\xi$

<u>Теорема</u> (неравенство Р-К-Ф)
    Рассмотрим класс всевозможных оценок $\hat{\theta}(\vec{x_n})$ параметра $\theta$, от которого зависит плотность вероятности $p_\xi(x, \theta)$
    Пусть
    1. $M \hat{\theta} = \int \cdots \int \hat{\theta}(\vec{x_n}) L(\vec{x_n}, \theta) \, dx_1 \cdots dx_n = \theta + \delta_{\hat{\theta}}(\theta)$
    $\delta_{\hat{\theta}}(\theta)$ - смещение, $= 0$, если $\hat{\theta}$ - несмешенная
    2. Плотность $p_\xi(x, \theta)$ удовлетворяет следующим условиям регулярности в смысле ее зависимости от $\theta$.
    2.1. Область всевозможных значений $\xi$ ($p_\xi(x, \theta) \neq 0$) не щависит от $\theta$.
    2.2. В 1. и в $\int \cdots \int L(\vec{x_n}, \theta) \, dx_1 \cdots dx_n = 1$ допустимо дифференцирование под интегралом и $\exists \frac{\partial L(\vec{x_n}, \theta)}{\partial \theta}$, $L(\vec{x}, \theta) > 0$
    2.3. $I(\vec{x_n}, \theta) \neq 0$
    Тогда $\forall$ оценки $\hat{\theta}(\vec{x_n})$ параметра $\theta$ имеет место неравенство.
    $$M(\hat{\theta}(\vec{x_n}) - \theta) \geq \left[\frac{\partial M \hat{\theta}}{\partial \theta}\right]^2 / M\left[\frac{\partial ln L(\vec{x_n}, \theta)}{\partial \theta}\right]^2$$ или
    $$M(\hat{\theta}(\vec{x_n}) - \theta)^2 \geq \frac{\left[1 + \frac{\partial \delta_{\hat{\theta}}(\theta)}{\partial\theta}\right]^2}{I(\theta, \vec{x_n})} \ (\ast)$$
    Если $\hat{\theta}(\vec{x_n})$ - несмещенная $\implies D \hat{\theta}(\vec{x_n}) \geq \frac{1}{I(\theta, \vec{x_n})} = D_\min \ (\ast\ast)$
    ($\hat{\theta}(\vec{x_n})$ - эффективная) $\iff$ (в неравенстве $(\ast)$ (или $(\ast\ast)$) достигается равенство)

Мера эффективности несмещенной оценки
    $$e(\hat{\theta}) = \frac{D_\min}{D(\hat{\theta}(\vec{x_n}))} = \frac{1}{I(\vec{x_n}. \theta)} \cdot \frac{1}{D(\hat{\theta}(\vec{x_n}))}$$
    Если $e(\hat{\theta}) = 1 \implies \hat{\theta}$ - эффективная

<u>Пример 2</u> (продолжение примера 1)
    $\vec{x_n} = \{x_1, \ldots, x_n\}$, $x_i \sim \mathcal{N}(a, \sigma^2)$
    Нашли ранее: $I(a; \vec{x_n}) = \frac{n}{\sigma^2}$
    $$\bar{x} = \frac{1}{n} \sum_{i = 1}^n x_i\ \ M \bar{x} = \frac{1}{n}\sum_{i=1}^n Mx_i = M\xi = a \implies \bar{x} - несмещенная$$
    $$D \bar{x} = \frac{1}{n^2} \sum_{i=1}^n Dx_i = \frac{n D\xi}{n^2} = \frac{D\xi}{n} = \frac{\sigma^2}{n}$$
    $$e(\bar{x}) = \frac{\sigma^2}{n} \cdot \frac{n}{\sigma^2} = 1 \implies \bar{x} - эффективная\ оценка$$
