# Bases
Una base de un espacio vectorial $V$ es un subconjunto $B \subset V$ tal que todo elemento de $V$ puede escribirse en forma única como combinación lineal de elementos de $B$.
Destacamos que estamos pidiendo dos cosas: 
1. que cualquiera sea el vector de V que consideremos, este se pueda escribir como CL de los vectores de B, y
2. que dicha $CL$ sea única, es decir, que haya una sola elección posible de coeficientes.
Si tenemos, digamos, los vectores $i = (1, 0, 0)$ y $k = (0, 0, 1)$ en $\mathbb{R}^3$ , no podemos escribir por ejemplo $(1, 2, 3)$ como $CL$ de $i$ y $k$, ya que no podemos lograr el 2 central; **por lo tanto ${i, k}$ no es una base** (según la definición 1). Por otro lado, si consideramos los vectores $i = (1, 0, 0), j = (0, 1, 0), k = (0, 0, 1)$ y además un cuarto vector $w = (2, 2, 2)$, entonces el vector $(1, 2, 3)$ se puede escribir al menos de las dos formas siguientes como $CL$ de estos cuatro:
$$(1, 2, 3) = 1(1, 0, 0) + 2(0, 1, 0) + 3(0, 0, 1) + 0(2, 2, 2)$$
$$(1, 2, 3) = 21(1, 0, 0) + 22(0, 1, 0) + 23(0, 0, 1) − 10(2, 2, 2)$$
No hay una sola elección posible de coeficientes y por lo tanto $\{i, j, k, w\}$ no es una base de $\mathbb{R}^3$ . Tı́picamente, nos interesará considerar a los vectores de una base en un cierto orden. Es decir, habrá uno de los vectores que tendrá el rol de primer vector, otro será el segundo, etc.

---
Decimos entonces que tenemos una base ordenada de $V$. Usaremos de todos modos la notación de conjuntos, por ejemplo $B = {(0, 1, 2), (0, 1, 1), (1, 1, 0)}$, aunque ahora se trate en realidad de una lista ordenada de vectores.

```ad-info
Comentario. Se puede probar que todo espacio vectorial posee una base, y que todas las bases de un espacio vectorial tienen la misma cantidad de elementos. Esta cantidad recibe el nombre de dimensión del espacio vectorial. Ası́, por ejemplo, $E_3$ tiene dimensión 3 y $R^n$ tiene dimensión n. Existen espacios vectoriales de dimensión infinita, pero los que estudiaremos en la materia son todos de dimensión finita.

```

---
# Bases ortogonales
**En los espacios vectoriales que estamos considerando existe la noción de norma (longitud) de vectores.**
- Si $(x,y,z) \in \mathbb{R}^2$,  entonces $|(x, y, z)| =  \sqrt{ x^2 + y² + z² }$ es la distancia de $(x, y, z)$ al origen. Una fórmula análoga vale en $\mathbb{R}²$ .
- En general, para $(x_{}1,\dots , x_{}n ) ∈ \mathbb{R}^n$, se define la norma $|(x_{1}, \dots , x_{n})| = \sqrt{x_{1}² +\dots+x_{n}^2}$.
- En $E^2$ y $E^3$ , la norma de un vector es su longitud. Si elegimos ejes perpendiculares entre sı́, con la misma unidad de medida en todos los ejes, la fórmula de la longitud en términos de las componentes es la misma que la de $\mathbb{R}^2$ y $\mathbb{R}^3$ , y queda expresada en la unidad de medida tomada para los ejes.
**También existe la noción de perpendicularidad en estos espacios vectoriales.**
- 

---
# Componentes y cambio de base
Dada una base ordenada $B \subset V$, sabemos que todo vector $v \in V$ se escribe como la $CL$ mencionada en la definición de base. Es decir, si $B= \{b_{1}, b_{2},\dots,b_{n}\}$ es una base ordenada de $V$, y $$v=\lambda_{1}b_{1}+\lambda_{2}b_{2}+\dots+\lambda_{n}b_{n}$$
entonces los coeficientes $\lambda_{1}, \lambda_{2},\dots,\lambda_{n}$ se llaman componentes de $v$ en la base $B$. Con las componentes formamos una matriz columna con la siguiente notación: $$[v]_{B}=\begin{bmatrix}\lambda_{1} \\ \lambda_{2} \\ \vdots \\ \lambda_{n}\end{bmatrix}$$
Decimos que esta matriz columna es el vector v escrito en la base B. Notemos que a ningún vector le pueden corresponder dos matrices columna diferentes, precisamente por la unicidad mencionada en la definición de base.

---
Ejemplo:
![[Pasted image 20221103093808.png]]

---
```ad-important
Recalcamos lo siguiente: Las componentes de un vector dependen de la base elegida. Si cambia la base, cambian las componentes (salvo para algunos vectores, pero hablando general- mente podemos esperar que cambien las componentes). En lo que sigue, estudiaremos cómo es ese cambio.

```
---
# Fórmulas de cambio de base
Mirando detenidamente el último ejemplo, veremos que la matriz de coeficientes del sistema de ecuaciones lineales guarda una relación con la base $B$. Efectivamente, dicha matriz se obtiene si ponemos los vectores de $B$ como columnas. Llamamos a esta matriz $[B]_{C}$ (leemos “B en C”):
$$[B]_{C}= \begin{bmatrix}0 & 0 & 1  \\ 1 & 1 & 1 \\ 2 & 1 & 0\end{bmatrix}$$
**Esta se llama la matriz de cambio de base de $B$ en $C$.** El sistema de ecuaciones lineales se puede escribir en forma matricial como $$[B]_{C}[V]_{B}=[V]_{C}, \longrightarrow(1)$$
**Al ser $[B]_{C}$ una matriz inversible**, tenemos la siguiente forma de obtener la solución (que será única): $$[V]_{B}=[B]_{C}^{-1}[V]_{C} \longrightarrow (2)$$
Si aplicáramos $(2)$ al último ejemplo, darı́a el mismo resultado para $[v]_{B}$ que hallamos “a mano”, es decir, planteando el sistema de ecuaciones lineales y resolviéndolo. 
**Las fórmulas $(1)$ y $(2)$ relacionan las componentes de un mismo vector $v$ en las dos bases $B$ y $C$**. Podemos interpretar estas fórmulas pensando que $[v]_{C}$ y $[v]_{B}$ son formas de expresar un mismo vector $v$ en dos “idiomas” distintos (las bases) y las matrices “traducen” de un idioma al otro. Por ejemplo, **en $(1)$ la matriz $[B]_{C}$ traduce de la base $B$ a la canónica**, y **en $(2)$ la matriz $[B]_{C}^−1$  traduce en sentido contrario, de la base canónica a** $B$. Denotamos entonces esta última matriz como $$[C]_{B}=[B]_{C}⁻1$$
ya que es la matriz de cambio de base de $C$ en $B$.
```ad-important
Importante: estas matrices (que son matrices cuadradas) reciben su entrada en forma de matriz columna multiplicando por la derecha, es decir, matriz cuadrada por matriz columna, en ese orden.

```
---
## Definición general:
Si se tienen dos bases ordenadas $B$ y $B_{0}$ de un mismo espacio vectorial $V$ de dimensión $n$, definimos la matriz de cambio de base de $B$ en $B_0$, denotada $[B]_{B_{0}}$ , escribiendo como columnas sucesivas a los vectores de $B$ escritos en la base $B_{0}$ . Es decir, si $B = {b_{1},\dots , b_{n}}$, entonces $$[B]_{B'}=\begin{bmatrix}[\vec{b}_{1}]_{B'} & \dots & [\vec{b}_{n}]_{B'}\end{bmatrix}$$
Aquí, $[\vec{b_{1}}]_{B'}$, etc. son matrices columna de $n \times 1$, por lo que la notación de arriba representa una matriz de $n \times n$.
	Esta matriz representa la siguiente propiedad fundamental: $$[\vec{v}]_{B'}=[B]_{B'}[\vec{v}_{B}]$$
	para todo $\vec{v} \in V$. Es decir, "traduce" vectores de la base $B$ a la base $B'$.
- Propiedades:
	1. $[B']_{B}=[B]_{B'}^{⁻1}$ (es decir, la traducción en sentido contrario se realiza con la matriz inversa).
	2. Si se tienen  tres base, denotémoslas $A$, $B$ y $D$, entonces  $$[A]_{D}=[B]_{D}[A]_{B}$$
	- Recordemos que estas matrices reciben su entrada como matriz columna por la derecha. La expresión $[B]_{D}[A]_{B}$ espera recibir un vector (por  la derecha) escrito en la base $A$, ya que la primera matriz que actúa es $[A]_{B}$, que traduce de $A$ a $B$.
	  Una vez que ya actuó $[A]_{B}$ , la siguiente matriz $[B]_{C}$ recibe ese resultado intermedio (otra vez por la derecha) y lo traduce a la base $D$. Lo que estamos diciendo entonces es que es lo mismo traducir de $A$ a $D$ directamente que traducir pasando por una etapa intermedia correspondiente a la base $B$.