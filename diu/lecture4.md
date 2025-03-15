# Глава 2. Теория устойчивостию

### Теория устойчивости занимается исследованием достоверности измерений, то есть исследует идеальную систему на реалистичность.

## §1. Устойчивость по Ляпунову. Асимптотическая устойчивость.
Исследуемые системы можно описать нормальной системой обыкновенных дифференциальных уравнений:
$$
(1)
\begin{cases}
    \dot{y_1} = f_1(t, y_1, ..., y_n)
    \\
    ...
    \\
    \dot{y_n} = f_n(t, y_1, ..., y_n),
\end{cases}
$$
где $f_i \in C(G)$, $G = [t_0; +\infty) \times D$, $D \in \mathbb{E}^n$

В векторной форме (можно и столбцами):
$\vec{y} = (y_1, ..., y_n)$
$\vec{f} = (f_1(t, \vec{y}), ..., f_n(t, \vec{y}))$
$(1) \sim \dot{\vec{y}} = \vec{f}(t, \vec{y})$
Пусть при $t = t_0$:
$$
\begin{pmatrix}
y_1 = y_1^\circ \\
... \\
y_n = y_n^\circ
\end{pmatrix}
\iff (\vec{y} = \vec{y}^\circ)
$$
Рассмотрим задачу Коши:
$$
\begin{cases}
    \dot{\vec{y}} = \vec{f}(t, \vec{y}) (1)
    \\
    \vec{y}(t_0) = \widetilde{\vec{y}}^\circ (2)
\end{cases}
$$
Считаем, что выполнены условия <u>Т</u> о существовании и единственности и выполнены условия задачи Коши $(1)$, $(2)$, причем решение $\exists!$ при $t = t_0$.

Изменим начальные условия (НУ):
$$
\begin{cases}
    \dot{\vec{y}} = \vec{f}(t, \vec{y}) (1)
    \\
    \vec{y}(t_0) = \widetilde{\vec{y}}^\circ (3)
\end{cases}
$$

Решения ЗК $(1)$, $(2)$ будем далее обозначать: $\vec{y} = \vec{y}(t, \vec{y}^\circ)$

Тогда решение ЗК $(1)$, $(3)$ это: $\vec{y} = \vec{y}(t, \widetilde{\vec{y}}^\circ)$

<u>Опр.1</u> Решение $\vec{y}(t, \vec{y}^\circ)$ называется устойчивым по Ляпунову, если:
    1. $\exists \delta_0 > 0$: $\forall \widetilde{\vec{y}}^\circ \in U_{\delta_0}(\vec{y}^\circ)$: решение ЗК $(1), (3)$ $\exists!$ при всех $t \geq t_0$ $(\widetilde{\vec{y}}^\circ \in U_{\delta_0}(\vec{y}^\circ) \iff \widetilde{\vec{y}}^\circ: ||\widetilde{\vec{y}}^\circ - \vec{y}^\circ|| < \delta_0)$
    2. $\forall \epsilon > 0 \exists \delta \in (0; \delta_0)$: $\forall \widetilde{\vec{y}}^\circ$: $||\widetilde{\vec{y}}^\circ - \vec{y}^\circ|| < \delta \implies ||\vec{y}(t, \widetilde{\vec{y}}^\circ) - \vec{y}(t, \vec{y}^\circ)|| < \epsilon$ (при всех $t \geq t_0$)

<u>Замечание:</u> Устойчивость может быть и у одного дифференциального уравнения (система необязательна)
    $($ 1. из <u>Опр.1</u> выполнено, при этом: $\exists \epsilon_0 > 0 \forall \delta > 0 \exists \widetilde{\vec{y}}^\circ, \exists t\ast > t_0: ||\widetilde{\vec{y}}^\circ - \vec{y}^\circ|| < \delta \wedge ||\vec{y}(t\ast, \widetilde{\vec{y}}) - \vec{y}(t\ast, \vec{y}^\circ)|| \geq \epsilon_0) \implies ($ решение - неустойчивое$)$
    $($ 1. из <u>Опр.1</u> не выполнено $) \implies ($ вообще ничего не можем сказать об устойчивости$)$

<u>Опр.2</u> Если $\vec{y}(t, \vec{y}^\circ)$:
    1. устойчиво по Ляпунову;
    2. $\exists \delta_1 > 0: \forall \widetilde{\vec{y}}^\circ: ||\widetilde{\vec{y}}^\circ - \vec{y}^\circ|| < \delta_1 \implies \lim_{t \to +\infty} ||\vec{y}(t, \widetilde{\vec{y}}^\circ - \vec{y}(t, \vec{y}^\circ)|| = 0$, тогда $\vec{y}(t, \widetilde{\vec{y}}^\circ)$ называется асимптотически устойчивым.

<u>Замечание:</u> Далее будем считать, что $t_0 = 0$ (достигается сдвигом по $t$, т.к. устойчивость системы не зависит от $t$).
    Исследование устойчивости ненулевого (нетривиального) решения ЗК $(1)$, $(2)$, можно свести к исследованию устойчивости тривиального решения другой систему ОДУ (нормальной).
    В самом деле: пусть $\vec{\phi}(t) = \vec{y}(t, \vec{y}^\circ)$ - решение ЗК $(1)$, $(2)$.
    Рассмотрим $\vec{x}(t) = \vec{y}(t) - \vec{\phi}(t)$. Тогда:
    $\dot{\vec{x}} = \dot{\vec{y}} - \dot{\vec{\phi}}(t) = \vec{f}(t, \vec{y}) - \dot{\vec{\phi}}(t) = \vec{f}(t, \vec{x}) + \vec{\phi}(t) - \dot{\vec{\phi}}(t) = \vec{g}(t, \vec{x})$
    $\vec{x}(0) = \dot{\vec{y}}(0) - \vec{\phi}(0) = \vec{y}^\circ - \vec{y}^\circ = \vec{0}$
    $\vec{g}(t, \vec{0}) = \vec{f}(t, \vec{\phi}(t)) - \dot{\vec{\phi}} = \vec{0}$
$$
\begin{cases}
    \dot{\vec{x}} = g(t, \vec{x}) (4)
    \\
    \vec{x}(0) = \vec{0} (5)
\end{cases}
$$
То есть при замене $\vec{x}(t) = \vec{y}(t) + \vec{\phi}(t)$ ЗК $(1)$, $(2)$ переходит в ЗК $(4)$, $(5)$, имеющую тривиальное решение.
<u>Опр.3</u> тривиальное решение системы $(4)$ называется устойчивым по Ляпунову, если:
    1. $\exists \delta_0: \forall \vec{x}^\circ: ||\vec{x}^\circ|| < \delta_0 \implies$ решение ЗК
    $$
    \begin{cases}
        \dot{\vec{x}} = g(t, \vec{x})
        \\
        \vec{x}(0) = \vec{x}^\circ,
    \end{cases}
    $$
    (которое обозначается $\vec{x}(t, \vec{x}^\circ)$) $\exists!$ при всех $t \geq 0$
    2. $\forall \epsilon > 0 \exists \delta \in (0; \delta_0): \forall \vec{x}^\circ: ||\vec{x}^\circ|| < \delta \implies ||\vec{x}(t, \vec{x}^\circ)|| < \epsilon$ при всех $t \geq 0$

<u>Опр.4</u> Тривиальное решение системы называется асимптотически устойчивым, если оно удовлетворяет:
    1. Устойчиво по Ляпунову
    2. $\exists \delta_1 > 0: \forall \vec{x}^\circ: ||\vec{x}^\circ|| < \delta_1 \implies \lim_{t \to +\infty} ||\vec{x}(t, \vec{x}^\circ)|| = 0$
    3. (пункт 1. из <u>Опр.3</u>) $\exists \delta_0: \forall \vec{x}^\circ: ||\vec{x}^\circ|| < \delta_0 \implies$ решение ЗК
    $$
    \begin{cases}
        \dot{\vec{x}} = g(t, \vec{x})
        \\
        \vec{x}(0) = \vec{x}^\circ,
    \end{cases}
    $$
    (которое обозначается $\vec{x}(t, \vec{x}^\circ)$) $\exists!$ при всех $t \geq 0$

Далее будем исследовать тривиальные решения на устойчивость, потому что любое решение можно свести к тривильному.

## §2. Устойчивость и асимптотическая устойчивость линейной системы ОДУ с постоянными коэффициентами
Рассмотрим систему, обладающую тривиальным решением:
$$
(1)
\begin{cases}
    \dot{y_1} = a_{11} y_1 + ... + a_{1n} y_n
    \\
    ...
    \\
    \dot{y_n} = a_{n1} y_1 + ... + a_{nn} y_n
\end{cases}
$$

Ее мы и будем исследовать на устойчивость в векторной форме: $\dot{\vec{y}} = A \vec{y}$ $(1)$

<u>Т1</u>
    Пусть мы имеем $(1)$, тогда:
    1. (Тривиальное решение СЛОДУ асимптотически устойчиво) $\iff$ ($\forall \lambda \implies Re \lambda < 0$)
    2. ($\exists \lambda: Re \lambda > 0$) $\implies$ (тривиальное решение СЛОДУ неустойчиво)
    3. ($\forall \lambda Re \lambda \leq 0 \wedge \forall \lambda Re \lambda = 0 \implies AK(\lambda) = \Gamma K(\lambda)$) => (тривиальное решение СЛОДУ устойчиво по Ляпунову, но не асимптотически)

<u>Замечание:</u>
    $AK(\lambda)$ - алгебраическая кратность $\lambda$;
    $\Gamma K(\lambda)$ - геометрическая кратность $\lambda$.
    ($AK(\lambda) > \Gamma K(\lambda)$) $\implies$ (тривиальное решение СЛОДУ неустойчиво)
