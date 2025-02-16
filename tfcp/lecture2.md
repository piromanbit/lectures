## §2. Множества на комплексной плоскости.
$\mathbb{C}$ как множество упорядоченных пар совпадает с $\mathbb{R}^2$

Точки $M_1 \left(x_1, y_1\right)$; $M_2 \left(x_2, y_2\right) \in \mathbb{R}^2$
    $\rho\left(M_1, M_2\right) = \sqrt{\left(x_1 - x_2\right)^2 + \left(y_1 - y_2\right)^2}$
    $z_1 = x_1 + y_1 i$, $z_2 = x_2 + y_2 i \in \mathbb{C}$
    $|z_1 - z_2| = \sqrt{\left(x_1 - x_2\right)^2 + \left(y_1 - y_2\right)^2} = dist\left(z_1, z_2\right)$
    $U_\delta\left(z_0\right) = \left\{z \in \mathbb{C} \mid |z - z_0| < \delta\right\}$ - дельта-окрестность
    $\delta>0$, $z_0 \in \mathbb{C}$
    $\mathring{U}_\delta\left(z_0\right) = U_\delta\left(z_0\right) \setminus \left\{z_0\right\} = \left\{z \in \mathbb{C} \mid 0 < |z - z_0| < \delta\right\}$ - проколотая дельта-окрестность

<u>Опр.1</u> Точка $z_0 \in E \subset \mathbb{C}$ называется внутренней точкой множества $E$, если
    $\exists \delta > 0$ $U_\delta\left(z_0\right) \subset E$
    Множество $E$ называется открытым, если все его точки - внутренние.
    Окрестностью точки $z_0$ $U\left(z_0\right)$ называется любое открытое множество, содержащее точку $z_0$
    Окрестностью множества $E \subset \mathbb{C}$ называется любое открытое множество, содержащее $E$.

<u>Лемма 1</u> (О числе Лебега). Пусть $m \in \mathbb{N}$, $K \subset \mathbb{R}^m$, $K$ - ограничено и замкнутое в $\mathbb{R}^m$:
    $K \subset \bigcup V_j$, где $j \in J$, $V_j$ - открытое множество $\mathbb{R}^m$, $J$ - множество индексов
    Тогда $\exists d > 0$: $\forall Q \subset K$ $(diam Q < d \implies \exists j_0 \in J$ $Q \subset V_{j_0})$
    $d$ - число Лебега.

$\Delta$:
> Предположим противное $\forall n \in \mathbb{N}$ $\exists Q_n \subset K$ $diam Q_n < \frac{1}{n}$, а $Q_n$ не содержится целиком ни в одном $V_j$ ($Q_n \neq \emptyset$)
> Рассмотрим точку $M_n \in Q_n \rightarrow \left\{M_n\right\} \subset K$ - ограниченное и замкнутое.
> $\implies \left\{M_n\right\}_{n \in \mathbb{N}}$ - огр. $\implies \exists \left\{M_{n_k}\right\}$ $\exists M_0 \in \mathbb{R}^m$ $M_{n_k} \to M_0 \in K$, $k \to \infty$ $\implies \exists j_0 \in J \left(M_0 \in V_{j_0} \implies \exists \delta > 0 U_\delta\left(M_0\right) \subset V_{j_0}\right)$
> $\exists N \in \mathbb{N}$ $\forall k > N$ $(diam Q_{n_k} < \frac{\delta}{2} \wedge \rho\left(M_0, M_{n_k}\right) < \frac{\delta}{2})$
>
> Рассмотрим $\forall M \in Q_{n_k}$ справедливо $\rho\left(M, M_0\right) \leq \rho\left(M, M_{n_k}\right) + \rho\left(M_{n_k}, M_0\right) < \frac{\delta}{2} + \frac{\delta}{2} = \delta$
>
> Т.е. $Q_{n_k} \subset U_\delta\left(M_0\right) \subset V_{j_0}$
> Противоречие.

□

<u>Лемма 2</u> (Гейне-Бореля)
    Пусть $K \subset  \mathbb{R}^m$, $K$ - ограниченное, замкнутое множество в $\mathbb{R}^m$ и $K \subset \bigcup V_j$, где $V_j$ - открытое множество в $\mathbb{R}^m$
    Тогда $\exists \left\{j_1, ..., j_n\right\} \subset J$ $K \subset \bigcup_{k=1}^n V_{j_k}$

$\Delta$:

> Пусть $d > 0$ из Леммы 1. $K$ - ограниченное множество.
> $\Pi$ - куб в $\mathbb{R}^m$ со сторонами, параллельными осям координат и равными $a$.
> $\frac{a}{N} \leq \frac{d}{2 \sqrt{m}}$, $n = N^m$ частичных кубиков.
> $\bigcup_{k=1}^n \Pi_k = \Pi$, $diam \Pi_k \leq \frac{d}{2}$; $K \subset \Pi$, $Q_k = K \cap \Pi_k \implies K = \bigcup_{k=1}^N Q_k$
> $\forall k = 1, ..., n$ $\left(diam Q_k \leq diam \Pi_k \leq \frac{d}{2} < d\right)$
> $\forall k = 1, ..., n$ $\exists V_{j_k} \supset Q_k \implies K = \bigcup_{k=1}^n Q_k \subset \bigcup_{k=1}^n V_{j_k}$

□

<u>Опр.2</u>
    Пусть $K \subset \mathbb{R}^m$, $\left\{V_j\right\}_{j \in J}$ - система открытых множеств в $\mathbb{R}^m$ называется (открытым) покрытием множества $K$, если $K \subset \bigcup V_j$

Компактом $K$ в $\mathbb{R}^m$ называется множество, из любого покрытия которого открытыми множествами $V_j$ можно выбрать (извлечь) конечное подпокрытие, т.е. $\exists \left\{j_1, ..., j_n\right\} \subset J$ $K \subset \bigcup_{k=1}^n V_{j_k}$

<u>Т1</u> (Критерий компактности в $\mathbb{R}^m$)
    Пусть $K \subset \mathbb{R}^m$, $m \in \mathbb{N}$ $(K$ - компакт в $\mathbb{R}^m) \iff (K$ - ограниченно и замкнуто в $\mathbb{R}^m)$

$\Delta$:

> $\Longleftarrow$ смотри Лемму Гейне-Бореля
> $\Longrightarrow \forall M \in K$ $U_\delta\left(M\right)$, где $\delta = 1$, $U_1\left(M\right)$
> $K \subset \bigcup_{M \in K} U_1\left(M\right) \implies \exists \left\{M_1, ..., M_n\right\} \subset K$:
> $K \subset \bigcup_{k=1}^n U_1\left(M_k\right)$ - ограниченное множество, как объединение конечного числа ограниченных множеств
> Докажем замкнутость $K = \bar{K} \iff (\mathbb{R}^m \setminus K$ - открыто$)$
> $\forall M_0 \in \left(\mathbb{R}^m \setminus K\right)$ $\exists U\left(M_0\right) \subset \left(\mathbb{R}^m \setminus K\right)$ ($U\left(M_0\right) \cap K \neq \emptyset$)
> $\forall M \in K$ рассмотрим $V_M = \left\{P \in \mathbb{R}^m \mid \rho\left(P, M\right) < \frac{1}{2}\rho\left(M, M_0\right)\right\}$ - открытое множество
> $K \subset \bigcup_{M \in K} V_M \implies \exists M_1, ..., M_n \in K$: $K \subset \bigcup_{k=1}^n V_{M_k} = W$
> точка $M_0 \in \overline{V_{M_k}} \implies \left(\mathbb{R}^m \setminus W\right)$ - открытое, как дополнение к замкнутому $\implies \exists U_\delta\left(M_0\right) \subset \left(\mathbb{R}^m \setminus W\right)$ $U_\delta\left(M_0\right) \cap K \neq \emptyset$

□

## §3. Последовательности и ряды комплексных чисел. Расширенная комплексная плоскость.

$\forall n \in \mathbb{N} \rightarrow z_n \in \mathbb{C}$, $\left\{z_n\right\}_{n=1}^{\infty}$, $\left\{z_n\right\}_{n \in \mathbb{N}}$, $\left\{z_n\right\}$
    $z_n =x_n + i y_n$, $\left\{x_n\right\}$, $\left\{y_n\right\}$

<u>Опр.1</u>
    Пусть $\left\{z_n\right\}_{n \in \mathbb{N}}$, $z_0 \in \mathbb{C}$. Говорят, что $\left\{z_n\right\}$ стремится к $z_0$ при $n \rightarrow \infty$, если
    $\forall \epsilon > 0$ $\exists N \in \mathbb{N}$ $\forall n \in \mathbb{N}$ $\left(n \geq N \implies |z_n - z_0| < \epsilon\right)$
    $\lim_{n \to \infty} z_n = z_0$; $z_n \rightarrow z_0$, $n \rightarrow \infty$
    $M_0\left(x_0, y_0\right)$, $M_n\left(x_n, y_n\right)$, $\rho\left(M_n, M_0\right) = |z_n - z_0|$
    $(z_n \rightarrow z_0$, $n \rightarrow \infty) \iff (\rho(M_n, M_0) \rightarrow 0$, $n \rightarrow \infty) \iff (x_n \rightarrow x_0 \wedge y_n \rightarrow y_0$, $n \rightarrow \infty)$
    $\max(|x_n - x_0|$, $|y_n - y_0|) \leq |z_n - z_0| \leq |x_n - x_0| + |y_n - y_0|$

Арифметические свойства.
$z_n \rightarrow z_0$, $w_n \rightarrow w_0$, $n \rightarrow \infty$
    1. $\exists \lim_{n \to \infty} \left(z_n + w_n\right) = z_0 + w_0$; $\forall \alpha \in \mathbb{C}$ $\exists \lim_{n \to \infty} (\alpha \cdot z_n)$
    2. $\exists \lim_{n \to \infty} (z_n \cdot w_n) = z_0 \cdot w_0$
    3. Если $\forall n \in \mathbb{N} \cup \left\{0\right\}$ $w_n \neq 0$, то $\exists \lim_{n \to \infty} \frac{z_n}{w_n} = \frac{z_0}{w_0}$ 

<u>Опр.2</u>
    $\left\{z_n\right\}$ называется ограниченной, если $\exists c > 0$ $\forall n \in \mathbb{N}$ $|z_n| \leq c$

<u>Т1</u> (Больцано-Вейерштрасса)
    Если последовательность комплексных чисел $\left\{z_n\right\}$ ограничена, то из нее можно извлечь сходящуюся подпоследовательность.

<u>Опр.3</u>
    $\left\{z_n\right\} \subset \mathbb{C}$ называется фундаментальной, если $\forall \epsilon > 0$ $\exists N \in \mathbb{N}$ $\forall n, p \in \mathbb{N}$ $\left(n \geq N \implies |z_{n+p} - z_n| < \epsilon\right)$
