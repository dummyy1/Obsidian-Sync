**Created:** Tuesday 15, November 2022, at 08:49.
**Status:** #school-note 
**Tags:** [[Elementos de Álgebra y Geometría]]

# Cambio de Base, Diagonalización

## Transformaciones lineales simétricas: 
Sea $T:\mathbb{R}^{N}\to \mathbb{R}^N$ una TL. Si $\begin{bmatrix}T\end{bmatrix}_{C}$ es una matriz simétrica, es decir, $\begin{bmatrix}T\end{bmatrix}^{T}_{C}= \begin{bmatrix}T\end{bmatrix}_{C}$, diremos que $T$ es una TL simétrica.

```ad-note
Se puede probar que si $B$ es una BON (base orto-normal) cualquiera, T es simétrica si y sólo si $\begin{bmatrix}T\end{bmatrix}_{B}$ es matriz simétrica. Es decir que $\begin{bmatrix}T\end{bmatrix}_{B}$ nos da la información definitiva sobre si $T$ es TL simétrica.

```

```ad-important

Si la matriz de $T$ es simétrica en alguna BON, lo es también en cualquier otra BON. Y por lo tanto si no es simétrica en una BON, no lo será en ninguna otra BON.
```

Para comprobar si una base es ortogonal, basta con simplemente realizar el módulo de cada uno de sus elementos sea igual a 1, y sean ortogonales.

## Diagonalización de matrices
Sea $M$ una matriz de orden $n$. Diagonalizar a $M$ consiste en:
- Encontrar (si es que existe) una base $B$ de $\mathbb{R}^n$ formada por autovectores de $M$,
- formar la matriz de cambio de base $[B]_{C}$ como siempre,
- escribir una matriz diagonal $D$ con los correspondientes autovalores (lo que antes llamábamos $[T]_{B}$).
Si se puede encontrar una base de autovectores, $M$ se dice diagonalizable. En ese caso se verifica que $$M=[B]_{C} D[B]^{-1}_{C}$$
---
## References:
- 
