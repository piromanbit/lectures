## §5. Кривые и области на комплексной плоскости
### п.1 Непрерывные кривые и области на комплексной плоскости
<u>Опр.1</u> Пусть $z(t): [a, b] \longrightarrow \mathbb{C}$, функция $z in C[a, b]$. Отображение $z(t)$ непрерывная кривая, параметрическая переменная $t \in [a, b]$. Точка $z(a), z(b)$ - начало и конец кривой. Если $z(a) = z(b)$, то кривая называется замкнутой (контур).
     $\gamma: x = x(t), y = y(t), t \in [a, b] \iff z = z(t) \equiv x(t) + i y(t), t \in [a, b]$. $(\gamma \subset \mathbb{C}$ непрерывная кривая $\mathbb{C})$

<u>Опр.2</u> Кривая $\gamma$ называется простой, если $\forall t_1, t_2 \in [a, b]  (t_1 \neq t_2 \implies z(t_1) \neq z(t_2))$
    Замкнутая кривая $\gamma$(контур) называется простой замкнутой кривой, если $\forall t_1, t_2 \in (a, b) (t_1 \neq t_2 \implies z(t_1) \neq z(t_2))$

<u>Опр.3</u> Кривая $\gamma$: $z = z(t), t \in [a, b]$ является объединением кривых $\gamma_1, ..., \gamma_n$ ($\gamma = \bigcup_{k=1}^n \gamma_k$), если $\exists$ разбиение $\tau = \{a=t_0 < t_1 < ... < t_n = b\}$ отрезок $[a, b]$:
    $\forall k = \overline{1, n} \gamma_k: z = z(t), t \in [t_{k-1}, t_k]$.
    Представление $\gamma = \bigcup_{k=1}^n \gamma_k$ - разбиение кривой $\gamma$
    ! $\gamma^-: z = z(-t + a + b), t \in [a, b]$ - противоположно ориентированная кривая $z(b)$ - начало, $z(a)$ - конец.

<u>Лемма 1</u> (О разбиении кривой)
    Пусть $\gamma \subset \mathbb{C}$ - непрерывная кривая: $\gamma \subset U_{j \in J} V_j$, где $V_j$ - открытое, $J$ - множество индексов. Тогда $\exists$ разбиение кривой $\gamma$
    $\gamma = \bigcup_{k=1}^n \gamma_k$ $\forall k = \overline{1, n}$ $\exists j_k \subset J$ $\gamma_k \subset V_jk$.

$\Delta$:

> По условию $\gamma$: $z = z(t), t \in [a, b]; z(t) = z(t) + i \cdot y(t)$ - параметризация $\gamma$
> $\gamma \subset \bigcup_{j \in J} V_j \implies \forall t \in [a, b] \exists j(t) \in J: z(t) \in V_{j(t)}$.
> В силу непрерывности $z(t) \exists U(t) \subset \mathbb{R}: z(U(t) \cap [a, b]) \subset V_{j(t)}. Т.к. $[a, b] \subset \bigcup_{t \in [a, b]}U(t)$
> $z(t) \exists U(t) \subset \mathbb{R}: z(U(t) \cap[a, b]) \subset V_{j(t)}$/
> то по Лемме о числе Лебега $\exists d > 0: \forall [t', t''] \subset [a, b]$
> $(t'' - t' < d \implies [t', t''] \subset U(t_0)) \implies z([t', t'']) \subset V_{j(t_0)}$.
> Пусть разбиение $\tau = \{a = t_0 < t_1 < ... < t_n = b\}, diam \tau < d$.
> Рассмотрим дуги $\gamma_k: z = z(t), t \in [t_{k-1}, t_k]; \forall k = \overline{1, n} \exists j_k \in J: z([t_{k-1}, t_k]) \subset V_{j_k}$, поэтому $\gamma = \bigcup_{k=1}^n \gamma_k \subset \bigcup_{k=1}^n V_{j_k}, \gamma_k \subset V_{j_k}$

□

<u>Опр.4</u> $D \subset \mathbb{C}$ называется линейно-связным, если $\forall z_0, z_1 \in D \exists$ непрерывная кривая $\gamma \subset D$ с началом в точка $z_0$ и концом в точке $z_1$.
    Открытое линейно-связное множество $D \subset \mathbb{C}$ называется областью.

<u>Лемма 2</u>
    Пусть $D \subset \mathbb{C}, D$ область. Тогда $\forall z_0, z_1 \in D$ $z_0 \neq z_1 \exists$ ломаная с конечным числом вершин (звеньев) целиком лежат в $D$, с началом в $z_0$ и концом в $z_1$.

$\Delta$:

> Пусть $z_0, z_1 \in D$ $z_0 \neq z_1$ $D$ - линейное связное $\implies \exists \gamma: z = z(t) \in D, t \in [a, b]$, $z(a) = z_0$, $z(b) = z_1$
> Т.к. $D$ - открытое, то $\forall c \in [a, b]$ $z(c) \in D$ вместе с некоторой окрестностью (кругом) $V_C$. По Л.1 о разбиении кривой, т.к. $\gamma \subset \bigcup_{c \in [a, b]} V_C$,
> $\exists$ разбиение $\tau = \{a = t_0 < ... < t_n = b\}$ отрезка $[a, b]$ и набор кругов $V_{C_1}, ..., V_{C_n}$ $\forall k = \overline{1, n}$
> $z([t_{k-1}, t_k]) \subset V_{C_k} \implies \mathbb{C} \supset [z(t_{k-1}), z(t_k)] \subset V_{C_k} \subset D \implies$ ломаная с вершинами $z(t_0), z(t_1), ..., z(t_n)$ лежит в $D$, является искомой.

□

<u>Опр.5</u> Кривая $\gamma$: $z(t) = x(t) + i y(t)$ называется гладкой, если $x(t), y(t) \in C^1[a,b]$ и $\dot{x}^2 + \dot{y}^2 \neq 0$. Кусочно-гладкая кривая может быть разбита на конечное число гладких кусков.

# Глава 2. Дифференцируемость функций комплексного переменного. Условия Коши-Римана. Голоморфная функция. Геометрический смысл производной.

## §1. Определение производной и дифференциала функции комплексного переменного. Свойства операции дифференцирования.

<u>Опр.1</u> Пусть $f: U(z_0) \longrightarrow \mathbb{C}, z_0 \in \mathbb{C}, \forall z \in U(z_0)$ $\Delta f = f(z) - f(z_0)$, $\Delta z = z - z_0$.
    Если $\exists \lim_{\Delta z \to 0} \frac{\Delta f}{\Delta z} \in \mathbb{C}$, то он называется комплексной производной функции $f$ в точке $z_0$, обозначается $f'(z_0)$
    $f$ называется дифференцируемой в точке $z_0$ ($\mathbb{C}$ - дифференцируемой), если $\exists C \in \mathbb{C} \forall z \in U(z_0)$
    $\Delta f(z_0; \Delta z) \equiv f(z_0 + \Delta z) - f(z_0) = C \cdot \Delta z + o(|\Delta z|)$. $(1)$
    $\iff$ $\frac{\Delta d}{\Delta z} = C + o(1) \implies C = f'(z_0)$
    $\lim_{\Delta z \to 0} \frac{o(|\Delta z|)}{|\Delta z|} = 0$

Пример: Пусть $n in \mathbb{N}, z \in \mathbb{C}, f(z) = z^n$. Тогда
    $f'(z) = (z^n)' = \lim_{t \to z} \frac{t^n - z^n}{t - z} = \lim_{t \to z} (t^{n - 1} + z \cdot t^{n - 2} + ... + z^{n - 1}) = n \cdot z^{n - 1}$

Свойства дифференцируемых функций:
    1. Пусть $f$ и $g$ определены в $U(x)$ и дифференцируемы в точке $z$. Тогда $\exists (f(z) + g(z))' = f'(z) + g'(z)$, $\exists (f(z) \cdot g(z))' = f'(z) g(z) + f(z) g'(z)$ и если $g\neq 0$ в $U(z)$, то $\exists (f(z) g(z))' = \frac{f'(z) g(z) - g'(z) f(z)}{g^2(z)}$
    2. Дифференцируемость сложной фнкции (суперпозиции)
    Пусть $f$ дифференцируема в точке $z$, а $g$ дифференцируема в точке $f(z)$. Тогда $(g \circ f)'(z) \equiv (g(f(t)))' = g'(f(z)) \cdot f'(z)$
    3. Дифференцируемость обратной функции
    Пусть $f: U(z_0) \longrightarrow f(U)$ $f$ - взаимно однозначно и взаимно непрерывно, т.е. $f \in C(U), f^{-1} \in C(V), V = f(U)$ $w_0 = f(z_0) \in V$ - окружность $w_0$.
    $f^{-1} \equiv g: V \longrightarrow U$ $\forall w \in V \longrightarrow z = g(w): z \in U \wedge f(z) = w$. Если функция $f$ дифференцируема в точке $z_0$ и $f'(z_0) \neq 0$, то функция $g$ дифференцируема в точке $w_0$ и $g'(w_0) = \frac{1}{f'(z_0)}$, $z_0 = g(w_0)$

$\Delta$:

> $\forall w \in V \setminus \{w_0\}$ рассмотрим $z = g(w) \implies z \in U \setminus \{z_0\}$
> $\frac{g(w) - g(w_0)}{w - w_0} = \frac{z - z_0}{f(z) - f(z_0)}$. Т.к. $w = f(z)$ взаимно однозначное $U \leftrightarrow V$ и вызаимно непрерывное, то $(w \to w_0) \iff (z \to z_0)$
> $$\implies g'(w_0) = \lim_{w \to w_0} \frac{g(w) - g(w_0)}{w - w_0} = \lim_{z \to z_0} \frac{z - z_0}{f(z) - f(z_0)} = \frac{1}{f'(z_0)}$$

□

### Условия Коши-Римана
Пусть $f$ определена в окрестности точки $z_0 = x_0 + i y_0$, $u(x, y) = Re f(z)$, $v(x, y) = Im f(z)$, $\Delta x = x - x_0$, $\Delta y = y - y_0$, $\Delta u = u(x, y) - u(x_0, y_0)$, $\Delta v = v(x, y) - v(x_0, y_0)$
    $u$, $v$ - дифференцируемы в точке $(x_0, y_0)$ по определению означает $\exists A_i, B_i \in \mathbb{R}$, $i = 1, 2$
    $\Delta u = A_1 \Delta x + B_1 \Delta y + \alpha_1$ $\wedge$ $\Delta v = A_2 \Delta x + B_2 \Delta y + \alpha_2$, где $\alpha_j = o_j(\rho)$, т.е. $\lim_{\rho \to 0} \frac{\alpha_j}{\rho} = 0$, $j = 1, 2 \implies A_1 = \frac{\partial u}{\partial x}, B_1 = \frac{\partial u}{\partial y}, A_2 = \frac{\partial v}{\partial x}, B_2 = \frac{\partial v}{\partial y}$ в точке $(x_0, y_0) \leftrightarrow z_0$.

! $\rho = \sqrt{(\Delta x)^2 + (\Delta y)^2} \equiv |\Delta z|$ ! $o(\rho) = o(|\Delta z|)$.

<u>Т1</u>
    Пусть $f$ определена в $U(z_0)$.
    $(f$ $\mathbb{C}$-дифференцируема в точке $z_0) \iff ((u, v$ дифференцируемы в точке $(x_0, y_0)$ как функции 2-ух переменных$) \wedge (\frac{\partial u}{\partial x} = \frac{\partial v}{\partial y}, \frac{\partial u}{\partial y} = - \frac{\partial v}{\partial x}$ в точке $(x_0, y_0))$

$\Delta$:

> $\implies$ пусть $f(z)$ дифференцируема в точке $z_0$, т.е. $\exists c \in \mathbb{C}: \Delta f = c \cdot \Delta z + o(|\Delta z|)$
> $\Delta f \equiv \Delta u + i \Delta v$, $\Delta z \equiv \Delta x + i\Delta y$, $c = c_1 + i c_2$, $o(|\Delta z|) = o_1(|\Delta z|) + i o_2(|\Delta z|)$.
> Тогда $\Delta f = \Delta u + i \Delta v = (c_1 + i c_2) (\Delta x + i \Delta y) + o_1(|\Delta z|) + i o_2 (|\Delta z|) \implies$
> $(2)$ $\Delta u = c_1 \cdot \Delta x - c_2 \cdot \Delta y + o_1(|\Delta z|) + i \cdot o_2(|\Delta z|)$ $\wedge$
> $\wedge$ $\Delta v = c_2 \cdot \Delta x + c_1 \cdot \Delta y + o_2(|\Delta z|)$
> ! $i = 1, 2$ $\frac{o_i(|\Delta z|)}{|\Delta z|} \to 0, \Delta z \to 0 \iff$
> $\iff \frac{o(|\Delta z|)}{|\Delta z|} \to 0, \Delta z \to 0$

# To be continued...
