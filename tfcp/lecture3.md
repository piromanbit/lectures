<u>Т2</u> (Критерий Коши сходимости последовательности к.ч.)

$$(\{z_n\} сходится) \iff (\{z_n\} - фундаментальная)$$

$\Delta$:

> $\max(|x_{n+p} - x_n|, |y_{n + p} - y_n|) \leq |z_{n + p} - z_n| \leq |x_{n + p} - x_n| + |y_{n + p} - y_n|$

□

### Ряды комплексных чисел
Рассмотрим $\{w_n\} \subset \mathbb{C} \longrightarrow w_1 + ... + w_n + ... = \sum_{k = 1}^\infty w_k$ $(1)$
    $\forall n \in \mathbb{N}$ $S_n = w_1 + ... + 2_n$, $\{S_n\}$
    Если $\exists \lim_{n \to \infty} S_n = S \in \mathbb{C}$, то ряд $(1)$ называется сходящимся, а $S$ называется суммой.
    Если сходится ряд $|w_1| + |w_2| + ... + |w_n| + ... = \sum_{k = 1}^\infty |w_k|$, то ряд $(1)$ называется абсолютно сходящимся.

<u>Т3</u> (Критерий Коши для числовых рядов)
    ($(1)$ - сходится) $\iff$ ($\forall \epsilon > 0 \exists N \in \mathbb{N} \forall n, p \in \mathbb{N}$)
    $\sum_{k = n + 1}^{n + p} = S_{n + p} - S_n$

Если к критерию Коши "добавим" неравенство $\bigtriangleup \implies$ Если $(1)$ сходится абсолютно $\implies (1)$ сходится

<u>Следствие</u> из критерия Коши (необходимое условие)
    Если $(1)$ сходится, то $w_n \longrightarrow 0$, $n \longrightarrow \infty$

$\Delta$:

> Критерий Коши $p = 1$ $|w_{n + 1}| < \epsilon$

□

<u>Свойства</u>:
    1. Пусть $(1)$ с $w_n = u_n + i v_n$
        ($(1)$ сходится к $S = S_1 + i S_2$) $\iff$ ($\sum_{n=1}^\infty u_n = S_1 \wedge \sum_{n=1}^\infty v_n = S_2$)
    2. $\sum_{k=1}^\infty w_k = S'$, $\sum_{k=1}^\infty S''$. Тогда $\forall \lambda, \mu \in \mathbb{C}$ $\sum_{k=1}^\infty (\lambda w_k + \mu z_k) = \lambda S' + \mu S''$

### Расширенная комплексная плоскость. Стереографическая проекция. Сфера Римана.
<u>Опр.5</u> $\{z_n\} \in \mathbb{C}$ называется сходящейся к $\infty$, если $\lim_{n \to \infty} |z_n| = +\infty$, т.е.
    $$\forall E > 0 \exists N \in \mathbb{N} \forall n in \mathbb{N} (n \geq N \implies |z_n| > E)$$
    $$z_n \longrightarrow \infty, n \longrightarrow \infty; \lim_{n \to \infty} z_n = \infty$$
    !$\{z_n\}$ является неограниченной, если $\forall C > 0 \exists n(C) \in \mathbb{N} \mid z_{n(C)} > C$
    $\{z_n\}$ не является ограниченной $\implies \exists \{z_{n_k}\}: z_{n_k} \longrightarrow \infty, k \longrightarrow \infty$

<u>Опр.6</u> Расширенной комплексной плоскостью назовем комплексную плоскость $\mathbb{C}$ с добавлением к ней идеальным элементом $\infty$
    Обозначение: $\bar{\mathbb{C}} = \mathbb{C} \cup \{\infty\}$
    $\forall \epsilon > 0$
    $\dot{U_\epsilon}(\infty) = \{z \in \mathbb{C} \mid |z| > \epsilon\}$ - проколотая окрестность $\infty$
    $U_\epsilon(\infty) = \dot{U_\epsilon}(\infty) \cup \{\infty\}$ - окрестность $\infty$

<u>Опр.7</u>
    $\{z_n\} \subset \bar{\mathbb{C}}$ называется сходящейся к $z_0 \in \bar{\mathbb{C}}$, если $\forall \epsilon > 0 \exists N \in \mathbb{N} (n \geq N \implies z_n \in U_\epsilon(z_0))$
    $\forall \{z_n\} \subset \bar{\mathbb{C}} \exists \{z_{n_k}\}$ сходится к $z_0 \in \bar{\mathbb{C}}$

### Стереографическая проекция. Сфера Римана.
Рассмотрим в $\mathbb{R}^3$ - ЕП сферу $\xi^2 + \eta^2 + \zeta^2 = \zeta$
    $\vec{q} = \{x, y, -1\}$ - направляющий вектор $\overrightarrow{N M}$
    [здесь могла бы быть ваша ре... картинка]()
    Плоскость $\zeta = 0$ отождествляем с $\mathbb{C}$
    $\xi = x \cdot t$ $\wedge$ $\eta = y \cdot t$ $\wedge$ $\zeta = 1 - t \mid$ $M - ?, M \in S \implies (x^2 + y^2)t^2 + 1 - 2t + t^2 = 1 - t \iff t((x^2 + y^2 + 1)t - 1) = 0$
$$
t = 0 \vee t = \frac{1}{x^2 + y^2 + 1} = \frac{1}{|z|^2 + 1} \longrightarrow M:
\begin{cases}
    \xi = \frac{x}{1 + |z|^2}
    \\
    \eta = \frac{y}{1 + |z|^2}
    \\
    \zeta = \frac{|z|^2}{1 + |z|^2}
\end{cases}
$$

$$t = 1 - \zeta \longrightarrow z? x = \frac{\xi}{1 - \zeta}; y = \frac{\eta}{1 - \zeta}$$
Отображение $S \setminus \{N\} \longrightarrow z = x + iy$ называется стереографической проекцией. Это взаимно однозначное и взаимно непрерывное отображение $S \setminus \{N\}$ на $\mathbb{C}$. Поставим соответствие:
    $N \leftrightarrow \infty$ и получим $S$ на $\bar{\mathbb{C}}$
    Такая модель называется сферой Римана.

### Функции комплексной переменной. Предел. Непрерывность.
Пусть $E \subset \bar{\mathbb{C}}$, $f: E \longrightarrow \bar{\mathbb{C}}$. $f(z) \longrightarrow w_0$, $z \longrightarrow z_0$, $z \in E$
    $z_0, w_0 \in \mathbb{C}$, $z$ - предельная точка $E$. $\forall \epsilon > 0 \exists \delta > 0 f(\dot{U_\delta}(z_0) \cap E) \subset U_\epsilon (w_0)$

Пусть $v \subset E$ $f(v) = \{w \in \bar{\mathbb{C}} \mid \exists z \in V f(z) = w\}$ - образ множества $V$ при отображении $f$.

Пусть, например, $z_0 \in \mathbb{C}$, $z_0$ - предельная точка $E$, $w_0 = \infty$
    $f(E) \subset \mathbb{C}$
    $f(z) \longrightarrow \infty$, $E \ni z \longrightarrow z_0 \iff \forall E > 0 \exists \delta > 0 \forall z \in E$ $(0 < |z - z_0| < \delta \implies |f(z)| > E)$

Остальные частные случаи аналогично.

Рассмотрим далее основной случай: $E \in \mathbb{C}, f(E) \subset \mathbb{C}$ - конечные значения, т.к. $\in \mathbb{C}$ (не $\in \bar{\mathbb{C}}$)

$\forall z = x + iy \in E \longrightarrow f(z) \in \mathbb{C}$
    $f(z) = u(x, y) + iv(x, y)$; $u = Re f(z)$; $v = Im f(z)$;
    $\forall (x, y) \in E \longrightarrow (u(x, y), v(x, y)) \in \mathbb{R}^2$

<u>Утв.1</u>
    Пусть $f: E \longrightarrow \mathbb{C}$, $E \subset \mathbb{C}$, $z_0$ - предельная точка $E$
    $z_0 = x_0 + iy_0$, $w_0 = u_0 + iv_0$
    $$(f(z) \longrightarrow w_0, E \ni z \longrightarrow z_0) \iff (\exists \lim_{E \ni (x, y) \to (x_0, y_0)} u(x, y) = u \wedge \exists \lim_{E \ni (x, y) \to (x_0, y_0)} v(x, y) = v_0)$$

$\Delta$:

> $(f(z) \longrightarrow w_0, E \ni z \longrightarrow z_0) \iff (\forall \epsilon > 0 \exists \delta > 0 \forall z \in E (0 < |z - z_0| < \delta \implies |f(z) - w_0| < \epsilon))$
> $(1) \max(|u(x, y) - x_0|, |v(x, y) - v_0|) \leq |u(x, y) - u_0| + |v(x, y) - v_0|$
> $\implies$ Из $(1)$ и определения $\implies \forall (x, y) \in E$: $0 < \sqrt{(x- x_0)^2 + (y - y_0)^2} < \delta$ $|u(x, y) - u_0| < \epsilon \wedge |v(x, y) - v_0| < \epsilon$
> $\Longleftarrow$ по $\frac{\epsilon}{2}$ $\exists \delta_1 > 0$ $|u(x, y) - u_0| < \epsilon / 2$ $\forall (x, y) \in E \cap \dot{U_{\delta_1}}(x_0, y_0)$
> $\exists \delta_2 > 0$ $|v(x, y) - v_0| < \epsilon / 2$ $\forall (x, y) \in E \cap \dot{U_{\delta_2}}(x_0, y_0)$
> Рассмотрим $\delta = \min(\delta_1, \delta_2)$

□

Арифметические свойства пределов:
    (Борисыч устно проговорил, так что не совсем точно)
    $\lim (f + g) = \lim f + \lim g$
    $\lim cf = c \lim f$
    $\lim f \cdot g = \lim f \cdot \lim g$
    $\lim \frac{f}{g} = \frac{\lim f}{\lim g}$, $g \neq 0$

### Непрерывность функции комплексных переменных
<u>Опр.2</u>
    Пусть $E \subset \mathbb{C}$, $f: E \longrightarrow \mathbb{C}$, $z_0 \in E$
    Функция $f(z)$ называется непрерывной в точке $z_0$ по множеству $E$, если
    $\forall \epsilon > 0 \exists \delta_\epsilon > 0 \forall z \in E$ $(|z - z_0| < \delta \implies |f(z) - f(z_0)| < \epsilon)$
    а) Если точка $z_0$ - это изолированная точка $E$, то $f(z)$ непрерывна в точке $z_0$.
    б) Если точка $z_0$ - предельная точка $E$, то непрерывность означает, что $\exists \lim_{E \ni z \to 0} f(z) = f(z_0)$

$f \in C(E)$ - множество непрерывных функций на $E$
$C(E; \mathbb{C})$

Свойства непрерывных функций:
    Пусть $f_1, f_2 \in C(E)$. Тогда:
    1. $f_1 \pm f_2 \in C(E)$
    2. $f_1 \cdot f_2 \in C(E)$
    3. $\forall z \in E f(z) = 0$, то $\frac{f_1}{f_2} in C(E)$

<u>Утв.2</u>
    Пусть $f: E \longrightarrow \mathbb{C}$, $E \subset \mathbb{C}$, $u(x, y) = Re f(z)$, $v(x, y) = Im f(z)$.
    Тогда $(f \in C(E)) \iff (u \in C(E) \wedge v \in C(E))$

<u>Следствие 1</u> (непрерывность сложной функции)
    Пусть $f: E \longrightarrow \mathbb{C}$, $E \subset \mathbb{C}$; $f \in C(E)$ и $f(E) \subset D \subset \mathbb{C}$, а $g: D \longrightarrow \mathbb{C}$, $g \in C(D)$. Тогда $\forall z \in E$ определена сложная функция $g(f(z)) \equiv (g \circ f)(z)$ и $g \circ f \in C(E)$.

<u>Следствие 2</u> (ограниченность непрерывной на компакте функции)
    Пусть $f \in C(E)$, $E$ - компакт. Тогда функция $f$ - ограничена на $E$.

<u>Опр.3</u> (равномерно непрерывная функция комплексного переменного)
    Пусть $f: E \longrightarrow \mathbb{C}$, $E \subset \mathbb{C}$. Функция $f$ называется равномерно непрерывной на $E$, если $\forall \epsilon > 0 \exists \delta > 0 \forall z_1, z_2 \in E (|z_1 - z_2| < \delta \implies |f(z_1) - f(z_2)| < \epsilon)$
    ! $(f$ - равномерно непрерывна на $E) \iff (u$ - равномерно непрерывна $\wedge$ $v$ - равномерно непрерывна на $E)$
    Пусть $E$ - компакт в $\mathbb{C}$($\mathbb{R}^2$). Тогда $(f \in C(E)) \iff (f$ - равномерно непрерывна на $E)$.

[продолжение читайте в источнике...](/tfcp/lecture4.md)
