## Ejemplos:

1. 

1. Sean B y B' las del ejemplo anterior, y sea $v=(1,1) \in \mathbb{R}²$. Escribamos $v$ en las bases B, B' y C.
	- Lo más inmediato es escribir $$[v]_{C}= \begin{bmatrix}1 \\ 1\end{bmatrix}$$
	Después tenemos $$[v]_{B}=[C]_{B}[v]_{C}=[B]_{C}^{⁻1}[v]_{C}=\begin{bmatrix}0 & 2  \\ 1 & 3 \end{bmatrix}^{-1} \begin{bmatrix}1 \\ 1\end{bmatrix}$$

3. Sea $B'= \{ (-1,1),(5,-2) \}$ como en el ejemplo anterior, y sea $w=2(-1,1)-(5,-2)$. Escribamos $[w]_{B'}$
   Una opción podría ser escribir $w=2(-1,1)-(5,2)=(-7,4)$, y así obtener fácilmente $[w]_{C}$, para luego usar la fórmula de cambio de base$[w]_{B'}=[B']_{C}^{-1} [w]_{C}$.

4. Sea $B= \{ b_{1}, b_{2}, b_{3}\}$ una base de $E_{3}$ y sea $B'=\{2b_{1}+b_{2}, -b_{3}, b_{2}+b_{3}\}$. Comprobar que $B'$ también es una base de $E_{3}$ y encontrar las dos matrices de cambio de base $[B]_{B'}$ y $[B']_{B}$.
   Para resolver esto, observemos que podemos escribir fácilmente a los vectores de $B'$ en la base $B$. Y les asignamos un nombre a estos mismos: $$\begin{cases}
u_{1}=2b_{1}+b_{2} \\ u_{2}=-b_{3} \\ u_{3}=b_{2}+b_{3}
\end{cases}$$
$[u_{1}]_{B}=\begin{bmatrix}2 \\1 \\0\end{bmatrix}$, $[u_{2}]_{B}=\begin{bmatrix}0 \\ 0\\-1\end{bmatrix}$, $[u_{3}]_{B}=\begin{bmatrix}0 \\1 \\1\end{bmatrix}$

Esto significa que puedo armar la matriz $$[B']_{B}=\begin{bmatrix}2 & 0 & 0 \\1 & 0 & 1 \\0 & -1 & 1\end{bmatrix}$$
A esto podrı́amos objetar lo siguiente: todavı́a no sé si B 0 es una base, ¿cómo puedo hablar entonces de matriz de cambio de base? Esto es cierto, pero nada nos impide armar esta matriz con estos 9 números, aunque todavı́a no sabemos si podemos atribuirle el significado de “matriz de cambio de base”. Por ahora es sólo una matriz que armamos y que denotamos con el sı́mbolo $[B']_{B}$ .
En nuestro caso, $det[B']B = 2 \neq 0$, por lo que $[B']_{B}$ es inversible y $B'$ es efectivamente una base de $E_{3}$ . La otra matriz de cambio de base es $$$$
Observemos que pudimos escribir estas matrices sin conocer cuáles son concretamente los vectores b1, b2 , b3 .

---
## Bases ortonormales
Si $B$ y $B'$ son $BON$ (página 2), ocurre algo que es de muchísima utilidad al momento de trabajar con cambios de base: 

En particular, como $C$ es una $BON$ de $\mathbb{R}^n$, $$[B]_{C}^{-1}=[B]_{C}^{T}, \text{ (si B es BON)}$$

---
## Cambio de coordenadas para puntos, rectas y planos
Hasta ahora pusimos énfasis en la interpretación de las matrices columna como componentes de un vector, pero de la misma forma podemos pensar en elementos de R2 o R3 como puntos del plano o del espacio, y almacenar sus coordenadas en matrices columna. Por ejemplo, el punto (x, y) se representa con la matriz columna $\begin{bmatrix}x \\y\end{bmatrix}$.
Diremos que x, y, son las coordenadas del punto en la base canónica. Si se tiene otra base B, podemos pensar que tenemos otros ejes coordenados adaptados a dicha base. Llamaremos x0, y0 a estos los ejes. Si un punto P tiene coordenadas (x, y) en la base canónica, en la base B tendrá otras coordenadas que llamaremos (x0 , y 0 ). Las fórmulas de cambio de base también sirven para cambiar las coordenadas de P de una base a otra. $$\begin{bmatrix}x \\y\end{bmatrix}=[B]_{C}\begin{bmatrix}x' \\y'\end{bmatrix}\atop \begin{bmatrix}x' \\y'\end{bmatrix}=[C]_{B}\begin{bmatrix}x \\y\end{bmatrix}$$De hecho, las coordenadas de P coinciden con las componentes del vector OP , donde O es el origen de coordenadas.

---
A continuación se ilustra el hecho de que un punto dado P tendrá coordenadas que cambiarán según la base elegida. En esta figura, se denotan como $(x,y)$ a las coordenadas en $B$ y como $(x',y')$ a las coordenadas de $B'$. La conversión se puede realizar con la matriz de cambio de base.
![[Pasted image 20221108091849.png]]

---
## Rectas
Sea $$L:\begin{cases}
x=1-\lambda \\
y=4+\lambda
\end{cases}, ~\lambda \in \mathbb{R}$$
Recordemos que esta fórmula es una especie de "receta" para generar puntos de $\mathbb{R}²$ que trazan la recta $L$. Para cada $\lambda$, obtenemos las coordenadas $(x,y)$ de un punto de la recta. Lo que queremos es una receta similar pero que genere las coordenadas de los puntos de $L$ pero escritos en otra base $B$. Como antes, llamamos $(x',y')$ a dichas coordenadas.
Tomemos para este ejemplo $B= \{ (0,1), (2,3)\}$, la misma que en los ejemplos de antes. Lo que haremos será cambiar de base el vector director $d_{L}=(-1,1)$ y el punto $(x_{0}, y_{0})=(1,4)$ por el que pasa la recta cuando $\lambda=0$.

---
## Planos
Consideremos un plano $\pi: ax+by+cz+d=0$. Esto significa que los puntos del plano $\pi$ son aquellos tales que sus coordenadas $(x,y,z)$ **(que corresponden  a la base canónica!)** verifican la ecuación dada. Escribir la ecuación del plano en otra base $B$ significa hallar la ecuación que deben verificar las coordenadas $(x',y',z')$ de los puntos del plano, donde ahora estamos refiriéndonos a las coordenadas en la base B. Para ello, utilizamos la fórmula $$\begin{bmatrix}x \\y \\z\end{bmatrix}=[B]_{C}\begin{bmatrix}x' \\y' \\z'\end{bmatrix}$$
que es la misma que tenı́amos antes solo que con una componente más ya que estamos trabajando en $\mathbb{R}^3$ . Esta fórmula nos permite escribir $x, y, z$ en función de $x' , y', z'$. Reemplazando estas expresiones en la ecuación de $π$ en la base canónica, obtenemos la ecuación de $π$ en la base $B$.
**Ejemplo:** Sea $\pi:2x-y+z+3=0,$ y sea $B=\{(1,0,1),(0,1,0),(1,2,2)\}$ una base de $\mathbb{R}³$. Entonces $$\begin{bmatrix}x \\y \\z\end{bmatrix}=\begin{bmatrix}1 & 0&1 \\0&1&2 \\1&0&2\end{bmatrix} \begin{bmatrix}x' \\y' \\z'\end{bmatrix}=\begin{bmatrix}x'+z' \\y' +2z' \\x'+2z'\end{bmatrix}$$
Sustituyendo esto en la ecuación del plano, queda $\pi:2(x'+z')-(y'+2z')+(x'+2z')+3=0 \longrightarrow$ $\pi:3x'-y'+2z'+3=0.$

```ad-warning
¡Importante! No sirve cambiar de base al vector normal. Este es un error habitual. En el caso de recién, eso darı́a $3x' + y' − z' + 3 = 0$, que no es la respuesta correcta. La razón, informalmente hablando, es que cambiar de base distorsiona la medición de ángulos. Lo que “parece perpendicular” en una base no lo parecerá en otra. Y el vector normal describe a un plano a través de una relación de perpendicularidad.

```

---
## Cambio de base para transformaciones lineales
Cuando vimos transformaciones lineales $T: \mathbb{R}^n \to \mathbb{R}^m$ hablamos de la matriz asociada $[T]_{C_{n}C_{m}}$, donde $C_{n}$ y $C_{m}$ eran las respectivas bases canónicas. La idea es que esta matriz representa a la TL de la siguiente forma: $$\begin{bmatrix}\text{salida}\end{bmatrix}=[\text{matriz de T}]\begin{bmatrix}\text{entrada}\end{bmatrix}$$