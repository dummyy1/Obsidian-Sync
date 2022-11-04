Ejercicio: Definir una trasnformación lineal $T:\mathbb{R}² \to \mathbb{R}²$ con autovalores 3 y -1, de forma tal que $V_{3}=\{ (x,-x) \in \mathbb{R}², x \in \mathbb{R} \}$ y $V_{2}=(2,4)$ sea autovector asociado al autovalor -1.

---
Resolución: 
- Escribimos $T(x,y)=(ax+by, cx+dy)$ (equivalentemente, $[T]_{C}=\begin{bmatrix} a & b \\ c & d \end{bmatrix}$).
- El hecho de que $$V_{3}=\{ (x,-x) \in \mathbb{R}², x \in \mathbb{R} \}$$ da $$V_{\lambda}[T(\hat{v})=\lambda \hat{v}, \hat{v} \neq 0]$$
  Significa que si tenemos un elemento de $V_{3}$, escribámoslo $(x,-x)$, entonces $$T(x,-x)=3(x,-x)$$
- En particular, si tomamos el vector $(1,-1)\in V_{3}$, $$T(1,-1)=3(1,-1)=(3,-3)$$ $$T(1,-1)=(a-b, c-d)$$
  Igualando, $$a-b=3 \atop c-d=-3$$
- Sabemos además que $$T(2,4)=-1(2,4)=(-2,-4) \atop T(2,4)=(2a+4b, 2c+4d)$$
  Igualando, $$2a+4b=-2 \atop 2c+4d=-4$$
  Juntando todo, tenemos un sistema de ecuaciones lineales con 4 incógnitas $a,b,c,d$ y 4 ecuaciones: $$a=3+b, ~ luego ~ a=\frac{5}{3} \atop c=-3+d, ~ luego~ c=-\frac{2}{3}$$$$3+b+2b=-1 \implies b=-\frac{4}{3} \atop -3+d+2d=2 \implies d=\frac{1}{3}$$
- $$[T]_{C}= \begin{bmatrix}
\frac{5}{3} & -\frac{4}{3} \\
-\frac{8}{3} & \frac{1}{3}
\end{bmatrix}
$$
$$\frac{1}{3} \begin{bmatrix}5 & -4  \\
-8 & 1
\end{bmatrix}
\begin{bmatrix} 1 \\
-1
\end{bmatrix}=\frac{1}{3}\begin{bmatrix}9  \\
-9\end{bmatrix}=\begin{bmatrix}3 \\ -3\end{bmatrix}$$
$$\frac{1}{3}\begin{bmatrix}5 & -4  \\ -8 & 1\end{bmatrix} \begin{bmatrix}2 \\4\end{bmatrix}=\frac{1}{3}\begin{bmatrix}-6  \\ -12\end{bmatrix}= \begin{bmatrix}-2 \\ -4\end{bmatrix}$$
---
- Variante:
  Definir $T:\mathbb{R}² \to \mathbb{R}²$ la transformación lineal con autovalor 3 y -1, $V_{3}= \{(x,-x)\in \mathbb{R}^2, x \in\mathbb{R}\}$. ¿Es única?
- $$T(x,y)=(ax+by, cx+dy)$$
$${\begin{cases}
a-b=3  \\
c-d=ni idea
\end{cases}}$$
