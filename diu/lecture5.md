## §3. Автономные системы

Рассмотрим следующую систему, в которой $\vec{f} \in C(G)$ ($G$ - область) явно не зависит от $t$
    $(1.1)\ \dot{\vec{y}} = \vec{f}(\vec{y})$
    $(2.1)\ \dot{\vec{y}} = \vec{f}(t, \vec{y})$

<u>Опр.1</u> Системы вида $(1.1)$ бдуем называть автономными системами.
    Отметим, что любую неавтономную систему $(2.1)$ можно свести к автономной.
    Покажем это:
    $$
    \begin{cases}
        \dot{y_1} = f_1(t, y_1, \ldots, y_n)
        \\
        \cdots
        \\
        \dot{y_n} = f_n(t, y_1, \ldots, y_n)
    \end{cases}
    $$
    Полагаем, что $t = y_{n+1}$. Тогда:
    $$
    (3)
    \begin{cases}
        \dot{y_1} = f_1(y_{n+1}, y_1, \ldots, y_n) = g(y_1, \ldots, y_{n+1})
        \\
        \cdots
        \\
        \dot{y_n} = f_n(y_{n+1}, y_1, \ldots, y_n) = g_n(y_1, \ldots, y_{n+1})
        \\
        \dot{y_{n+1}} = 1
    \end{cases}
    $$
    Таким образом, неавтономная система $(2.1)$ сведена к автономной $(1.1)$
    Справедливо и обратное:
    $$
    (1.2)
    \begin{cases}
        \dot{y_1} = f_1(y_1, \ldots, y_n)
        \\
        \dot{y_n} = f_n(y_1, \ldots, y_n)
    \end{cases}
    $$
    Допустим, что в точке $(y_1^\circ, \ldots, y_n^\circ) \in G$ выполнено: $f_n(\vec{y}^\circ) \neq 0$
    Тогда:
    $$\exists\ U_\delta(\vec{y}^\circ) = \{\vec{y} \mid ||\vec{y} - \vec{y}^\circ|| < \delta\}:\ f_n(\vec{y}) \neq 0$$
    Получим:
    $$
    (2.2)
    \begin{cases}
        \frac{d y_1}{d y_n} = \frac{\dot{y_1}}{\dot{y_n}} = \frac{f_1(\vec{y})}{f_n(\vec{y})} \equiv F_1(y_1, \ldots, y_n) = \phi_1(y_n, y_1, \ldots, y_{n-1})
        \\
        \ldots
        \\
        \frac{d y_{n-1}}{d y_n} = \frac{\dot{y_{n-1}}}{\dot{y_n}} = \frac{f_{n-1}(\vec{y})}{f_n(\vec{y})} \equiv F_{n-1}(y_1, \ldots, y_n) = \phi_{n-1}(y_n, y_1, \ldots, y_{n-1})
    \end{cases}
    $$
    Таким образом, автономная система $(1.2)$ сведена к неавтономной системе $(2.2)$, которая является таковой в некоторой $U_\delta(\vec{y}^\circ)$

Далее напомним, что всякое решение $(1.1)$ в пространстве переменных $(t, \vec{y})$ задает интегральную кривую

<u>Опр.2</u> Подпространство переменных $(\vec{y})$ называется фазовым пространством, а проекция интегральной кривой на фазовое пространство называется фазовой траекторией.
![](/diu/lecture5/image1.jpg)

<u>Замечание:</u> Направление движения на фазовой траектории с возрастанием $t$ указывается стрелкой

<u>Опр.3</u> Совокупность фазовых траекторий, дающая представление об общем поведении решения, называется фазовым портретом.

<u>Опр.4</u> Точка $\vec{y} = \vec{a}$ называется точкой покоя (положением равновесия) системы $(1.1)$, если: $\vec{f}(\vec{a}) = \vec{0}$

$$
(\vec{f}(\vec{a}) = \vec{0}) \iff \left(
\begin{cases}
    f_1(a_1, \ldots, a_n) = 0
    \\
    \cdots
    \\
    f_n(a_1, \ldots, a_n) = 0
\end{cases}
\right)
$$

<u>Замечание:</u> Путем параллельного переноса $\vec{y} = \vec{\widetilde{y}} + \vec{a}$ можно добиться, чтобы точка покоя была $\vec{\widetilde{y}} = \vec{0}$

Далее будем считать, что система $(1.1)$ обладает нулевой точкой покоя: $\vec{f}(\vec{0}) = \vec{0}$

Теперь рассмотрим линейную автономную систему второго порядка:
$$
(4)\ 
\begin{cases}
    \dot{x} = a_{11} x + a_{12} y
    \\
    \dot{y} = a_{21} x + a_{22} y
\end{cases}
$$
обладающую нулевой точкой покоя.

При $a_{11}x + a_{12}y \neq 0$ система $(4)$ эквивалентна уравнению:
    $$(5)\ \frac{dy}{dx} = \frac{a_{21}x + a_{22}y}{a_{11}x + a_{12}y}$$
    Заметим, что нулевая точка покоя системы $(4)$ является особой точкой уравнения $(5)$, то есть в ней нарушаются условия теоремы о $\exists!$
    Пусть $\lambda_1, \lambda_2$ - корни характеристического уравнения:
    $$
    A = 
    \begin{vmatrix} 
        a_{11} - \lambda & a_{12}
        \\
        a_{21} & a_{22} - \lambda
    \end{vmatrix}
    = 0
    $$
    $A$ - вещественная матрица
    Рассмотрим все возможные случаи:

I. Пусть $\lambda_1,\ \lambda_2 \in \mathbb{R}:\ \lambda_1 \neq \lambda_2$. Тогда:
    $\lambda_1 \sim \vec{h_1}$, $\lambda_2 \sim \vec{h_2}$ (собственные векторы)
    Перейдём в базим $\{\vec{h_1}, \vec{h_2}\}$
    Пусть $T = (\vec{h_1}, \vec{h_2})$ - матрица перехода, и 
    $$\vec{y} = \begin{pmatrix} x \\ y \end{pmatrix} = T \cdot \vec{z}$$
    Тогда:
    $$
    \Lambda = 
    \begin{pmatrix}
        \lambda_1 & 0
        \\
        0 & \lambda_2
    \end{pmatrix}
    $$
    $$
    (\vec{\dot{y}} = T \vec{\dot{z}} = A \vec{y} = AT \vec{z}) \implies
    (\vec{\dot{z}} = T^{-1}AT\vec{z}) \implies (\vec{\dot{z}} = \Lambda\vec{z}) \iff \left(
    \begin{cases}
        \dot{z_1} = \lambda_1 z_1
        \\
        \dot{z_2} = \lambda_2 z_2
    \end{cases}
    \right) \iff \left((6)\ 
    \begin{cases}
        z_1 = c_1 e^{\lambda_1 t}
        \\
        z_2 = c_2 e^{\lambda_2 t}
    \end{cases}
    \right)
    $$

1.0 Рассмотрим $\lambda_1, \lambda_2 \neq 0$
    Исключим $t$ из $(6)$:
    $$z_2 = c |z_1|^{\lambda_2 / \lambda_1}$$

1.1 Рассмотрим $\lambda_2 > \lambda_1 > 0$. Тогда:
    $$\left(\frac{\lambda_2}{\lambda_1} = \alpha > 1\right) \implies (z_2 = c |z_1|^\alpha)$$
    ![](/diu/lecture5/image2.jpg)
    Здесь мы получаем неустйчивый узел, так как все движение от точки покоя
    Заметим, что параболы в точке покоя касаются решения $z_2 = 0\ (c_2 = 0)$

1.2 Рассмотрим $\lambda_2 < \lambda_1 < 0$: ситуация, аналогичная 1.1
    $$(\alpha = \frac{\lambda_2}{\lambda_1} > 1) \implies (экспоненты\ в\ (6)\ затухают)$$
    Здесь мы получаем устойчивый узел (причем он устойчив ассимтотически).
    ![](/diu/lecture5/image3.jpg)

2.0 Вернемся к исходным переменным:
    $$\vec{y} = \begin{pmatrix} x \\ y \end{pmatrix} = T \vec{z} = (\vec{h_1}, \vec{h_2}) \cdot \left(c_1 e^{\lambda_1 t} \begin{pmatrix} 1 \\ 0 \end{pmatrix} + c_2 e^{\lambda_2 t} \begin{pmatrix} 0 \\ 1 \end{pmatrix}\right) = c_1 \vec{h_1} e^{\lambda_1 t} + c_2 \vec{h_2} e^{\lambda_2 t}$$
    Поскольку в общем случае: $\vec{h_1} \not\perp \vec{h_2}$, преобразование является косоугольным(не ортогональным). Это похоже на то, как, есои бы мы вытягивали квадратный платок по диагонали и получили бы из квадрата ромб.

2.1 Пусть $\lambda_2 > \lambda_1 > 0$
    ![](/diu/lecture5/image4.jpg)
    Параболические траекории в точке покоя касаются прямолинейной траектории с направляющим вектором $\vec{h_1}$(отвечающим по модулю меньшему собственному значению)
    Здесь: асимптотически неустойчивый узел.

2.2 Пусть $\lambda_2 < \lambda_1 < 0$
    ![](/diu/lecture5/image5.jpg)
    Здесь траектории подчинаются тому же правилу, что и в 2.1, причем это асимптотически устойчивый узел.

1.3 Пусть $\lambda_1 < 0 < \lambda_2$. Тогда:
    $z_2 = c |z_1|^{\lambda_2 / \lambda_1}$, где $\lambda_2 / \lambda_1 = \alpha < 0$
    $z_2 = c |z_1|^\alpha$ - гиперболы
    ![](/diu/lecture5/image6.jpg)
    "Поигравшись" со значением параметра $t$, получаем картину слева.
    Здесь точка покоя - седло (то есть какие-то кривый идут в точку покоя, а какие-то нет)

2.3 Пусть $\lambda_1 < 0 < \lambda_2$.
    ![](/diu/lecture5/image7.jpg)
    Здесь направляющие вектора $\vec{h_1}$ и $\vec{h_2}$ является асимптотами гиперболических траекторий. Аналогично точка покоя - седло.

3.1 Пусть $\lambda_1 = 0,\ \lambda_2 > 0$. Тогда:
    $$
    (\ast)\ (\det A = 0) \implies (строки\ A\ пропорциональны) \implies \left(\dfrac{dy}{dx} = \dfrac{a_{21} x + a_{22} y}{a_{11}x + a_{12}y} = k\right) \implies (y = kx + c)
    $$
    $$
    (\ast\ast)\ (\det A = 0) \implies \left(
    \begin{cases}
        a_{11} x + a_{12} y = 0
        \\
        a_{21} x + a_{22} y = 0
    \end{cases}
    \right) \implies (система\ имеет\ нетривиальные\ решения)
    $$
    $$
    \begin{pmatrix} x \\ y \end{pmatrix} = c \cdot \vec{h_1},\ \vec{h_1} \sim \lambda_1 = 0
    $$
    $$
    \begin{pmatrix} x \\ y \end{pmatrix} = c \cdot \vec{h_1} + c_2 \vec{h_2} e^{\lambda_2 t}
    $$
    ![](/diu/lecture5/image8.jpg)
    $$
    \begin{cases}
        x = c_1 h_{11} + c_2 h_{12} e^{\lambda_2 t}
        \\
        y = c_1 h_{21} + c_2 h_{22} e^{\lambda_2 t}
    \end{cases}
    $$
    $$
    \dfrac{x - c_1 h_{11}}{\not{c_2} h_{12}} = \dfrac{y - c_1 h_{21}}{\not{c_2} h_{22}}
    $$
    Здесь все точки покоя(в том числе нулевая) неустйчивы.

3.2 Пусть $\lambda_1 = 0,\ \lambda_2 < 0$
    ![](/diu/lecture5/image9.jpg)
    Здесь выкладки аналогичны 3.1, но тут нулевая точка покоя - устойчива, но не асимптотически (потому что при $t \to +\infty$ мы попадем в точку 0, находясь на определенной траектории а в остльных случаях мы будем сколь угодно близко).

II. Пусть $\lambda_{1,2} = \alpha \pm i \beta$
    $\vec{h_{1,2}} = \vec{u} \pm i \vec{v}$
    $$\begin{pmatrix} x \\ y \end{pmatrix} = c_1\, Re((\vec{u} + i \vec{v}) e^{(\alpha + i \beta)t}) + c_2\, Im((\vec{u} + i \vec{v}) e^{(\alpha + i \beta)t})$$
    $$\begin{pmatrix} z_1 \\ z_2 \end{pmatrix} = c_1\, Re\left(\left(\begin{pmatrix}1 \\ 0 \end{pmatrix} + i \begin{pmatrix} 0 \\ -1 \end{pmatrix}\right)e^{(\alpha + i \beta)t}\right) + c_2\, Im\left(\left(\begin{pmatrix}1 \\ 0 \end{pmatrix} + i \begin{pmatrix} 0 \\ -1 \end{pmatrix}\right)e^{(\alpha + i \beta)t}\right) =$$
    $$= c_1 e^{\alpha t}\, Re\left(\begin{pmatrix}1 \\ -i\end{pmatrix}(\cos\beta t + i \sin\beta t)\right) + c_2\, Im\left(\left(\begin{pmatrix}1 \\ 0\end{pmatrix} + i \begin{pmatrix} 0 \\ -1 \end{pmatrix}\right)e^{(\alpha + i \beta t)}\right) =$$
    $$= c_1 e^{\alpha t}\begin{pmatrix}\cos\beta t \\ \sin\beta t\end{pmatrix} + c_2 e^{\alpha t} \begin{pmatrix} \sin\beta t \\ - \cos\beta t \end{pmatrix} = e^{\alpha t} \begin{pmatrix}c_1 \cos\beta t + c_2 \sin\beta t \\ c_1 \sin\beta t - c_2 \cos\beta t\end{pmatrix}\ (=)$$
    Введем следующую замену: $\rho = \sqrt{c_1^2 + c_2^2}$
    В таком случае:
    $$
    \begin{cases}
        \cos\phi = \dfrac{c_1}{\rho}
        \\
        \sin\phi = \dfrac{c_2}{\rho}
    \end{cases}
    $$
    $$(=)\ \rho e^{\alpha t} \begin{pmatrix}\cos(\beta t - \phi) \\ \sin(\beta t - \phi)\end{pmatrix}\ \ \ \ \ 
    \begin{cases}
        z_1 = \rho e^{\alpha t} \cdot \cos(\beta t - \phi)
        \\
        z_2 = \rho e^{\alpha t} \cdot \sin(\beta t - \phi)
    \end{cases}
    $$
    Значит, возможны следующие случаи:
    $$(\alpha = 0) \implies (траекториями\ являются\ окружности) \implies (точка\ покоя\ является\ их\ центром)$$
    $$(\alpha \neq 0) \implies (траекториями\ являются\ логарифмические\ спирали) \implies (точки\ покоя\ устойчивы\ либо\ неустойчивы)$$

# To be continued...

