**Created:** Friday 11, November 2022, at 12:23.
**Status:** #fleet-note 
**Tags:** [[TL a partir de CL]]

# Encontrar la Transformación Lineal de un vector a partir de la TL otros dos vectores

Es posible obtener el vector transformado $(T(\vec{u}))$ al que se le aplicó una Transformación Lineal sin conocer la propia TL. Los únicos requisitos son conocer dos vectores $(\vec{v_{1}}, \vec{v_{2}})$ y sus respectivas componentes luego de aplicarse dicha TL $(T(\vec{v_{1}}), T(\vec{v_{2}}))$, además, es necesario que el vector objetivo se pueda escribir como Combinación Lineal de los otros dos vectores, o lo que es lo mismo de manera general, si el conjunto conformado por ellos es una Base $\mathbb{R}^n, n \in \mathbb{N}$. Esto lo podemos verificar por medio de la determinante, la cual debe dar distinta de cero para que sea considerado una Base, a continuación trabajamos con un ejemplo en $\mathbb{R}^2$ $$\det(\begin{bmatrix}v_{1_{a}} & v_{1_{b}} \\ v_{2_{a}} &  v_{2_{b}} \end{bmatrix}) \neq 0$$

---
- El siguiente paso sería plantear la combinación lineal $$(u_{1}, u_{2})=\lambda(v_{1_{a}}, v_{1_{b}})+ \beta(v_{2_{a}}, v_{2_{b}}), \text{ con } \lambda, \beta \in \mathbb{R}$$
- Conseguimos el sistema lineal $$\begin{cases}
u_{1}=\lambda v_{1_{a}}+\beta v_{2_{a}}  \\
u_{2}=\lambda v_{1_{b}}+\beta v_{2_{b}}
\end{cases}$$
- Luego, gracias a la definición de TL, llegamos a que $$T(u_{1},u_{2})=\lambda T(v_{1_{a}},v_{1_{b}})+\beta T(v_{2_{a}},v_{2_{b}})$$
- Pero, ya conocemos $T(\vec{v_{1}})$ y $T(\vec{v_{2}})$, por lo que podemos resolver la ecuación y obtener $T(\vec{u})$! 
---
## References:
- 00:17:55
- <iframe src="https://drive.google.com/file/d/1MFUTYT-6myQSW7HbKNa6aaebORWREKQg/view" allow="fullscreen" allowfullscreen="" style="height:100%;width:100%; aspect-ratio: 16 / 9; "></iframe> 