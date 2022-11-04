## "Sumar una cantidad infinita de términos"
**Escenario:** 
	Tenemos una sucesión (dato): $$\{ x_1,x_2,x_3, \dots\}$$
	Fabricamos una sucesión auxiliar: 
	$S_1=x_1$, $S_2=x_2$, $S_3=x_3$ $S_4=x_4$ $S_5=x_5$ $S_6=x_6$ ...
## "Sucesión recursiva", Sucesión de sumas parciales.
$$S_{N+1}=S_{N}+X_{N+1} \atop
S_1=X_1$$
**Ejemplo 1:** "Serie geométrica" (Paradoja de Zenón)
**Dato:** Sucesión geométrica $q=\frac{1}{2}$ $$\{1, \frac{1}{2}, \frac{1}{4}, \frac{1}{8}, \frac{1}{16}, \dots \}= \{ \frac{1}{2^n}, n \in \mathbb{Z}\}$$
## Problemas:
1. Decidir si existe límite de la sucesión $S_N$.
2. Hallarlo.
	1. Hallar la suma:
		- Geométrica.
		- Telescópica.

1. Cuando exista el límite y sea un número, diremos que la serie es *"convergente"*.
   Puede pasar que el límite exista y sea $\infty$, en tal caso, diremos que la serie es *"divergente"*.
### El problema 1 es "analizar la convergencia".

---
Veamos luego qué condiciones sobre la razón "$q$" la serie geométrica es *convergente*.
$$\{ 1, q, q², q³, q⁴, \dots \}$$
$S_1=1$, $S_2=1+q¹$, $S_3=1+q¹+q²$, $S_4=1+q¹+q²+q³$, 

Llegamos a $$S_{N+1}=S_N+q^N$$Remplazo en XX
$$1=S_N+q^N-qS_N$$
$$1-q^N=S_N($$
$$\frac{1-q^n}{1-q}=S_N$$
**6º Caso de Factoreo!**
$$1+\dots+q^{N-1}=\frac{1-q^n}{1-q}$$
## Notación:
$$x_1+x_2+x_3=\sum_{n=1}^{3}x_n$$

---
Nota: $$q⁵+q⁶+\dots+q^{58}=\sum_{j=5}^{58}q^{j}$$
$$=\frac{q⁵(1-q^{58-5+1})}{1-q}$$
De forma general:
$$q^{r_0}+q^{r_0+1}+\dots +q^{r_1}=\frac{q⁵(1-q^{58-5+1})}{1-q}$$

---
Condiciones:FOTO

---
Para $|q|<1$, $$S_N=\frac{1-q^N}{1-q} \longrightarrow \frac{1}{1-q}$$
**La serie geométrica es *convergente* y su límite es $\frac{1}{1-q}$.**

Para $q>1$, $$S_N= \frac{1-q^N}{1-q}=\frac{q^N-1}{q-1}\longrightarrow +\infty$$
**La serie es *divergente*.**

---
Notación: $$\lim S_N= \sum_{k=1}^{+\infty}x_k$$

---
Para $q \leq -1$, la serie $\sum_{k=0}^{+\infty}q^k$ no es convergente ni divergente.

---
Serie "Telescópica"
Dato: $\{ x_1, x_2, x_3, x_4, \dots \}$. Cuando la sucesión general puede escribirse como $x_n=d_{n+1}-d_n$, donde $d_n$ es una sucesión auxiliar.

**Ejemplo:** $\rightarrow d_n= -\frac{1}{n}$ 
$$d_{n+1}-d_n=-\frac{1}{n+1}-(-\frac{1}{n})=\frac{1}{n}-\frac{1}{n+1}$$
$$S_{20}=1-\frac{1}{21}=1+d_{21}=d_{21}-d_1$$
Por lo que la serie será, $$S_N=1-\frac{1}{N+1}=d_{N+1}-d_1$$
y su límite cuando $N$ tiende a infinito $$\lim_{N\rightarrow +\infty} S_N= \lim_{N \rightarrow +\infty} d_{n+1}-d_1$$
Si la sucesión auxiliar tiene límite ($d_N \rightarrow d\in \mathbb{R}$) entonces la serie telescópica $$\sum_{k=1}^{+\infty}x_k=\sum_{k=1}^{+\infty}d_{k+1}-d_k=d-d_1$$
$$\sum_{n=1}^{\infty} \frac{1}{n}-\frac{1}{n+1}=0-d_1=-(-1)=1$$

---
## Criterio de convergencia
Buscamos condiciones (suficientes) sobre el término general de tal manera que la serie $\sum_{n=1}^{+\infty}x_{n}$ sea convergente.
Si $x_{1}+\dots +x_{n}+ \dots= S\in \mathbb{R}$
la "convergencia" se juega en los últimos términos. Por tal motivo, escribiremos $$\sum X_{n}=x_{1}+x_{2}+\dots$$
```ad-help
Modificar una cantidad finita de términos *NO* modifica la clasificación.
```
---
## Criterio básico I
Si $\sum a_{n}$ es convergente $\implies a_{n} \rightarrow 0$

> [!caution] Warning
> **Si $a_{n} \nrightarrow 0 \implies \sum a_{n}$ NO converge.**
> Ojito, la recíproca NO vale. Veamos el siguiente ejemplo.
> 

### Serie armónica: 
$$1+\frac{1}{2}+\frac{1}{3}+\frac{1}{4}+\frac{1}{5}+\dots$$
La sucesión será $$a_{n}=\frac{1}{n}$$
$$a_{n} \longrightarrow 0$$
Analizar la convergencia de la serie armónica $$\sum_{1}$^{\infty} \frac{1}{n}=1+\frac{1}{2}+\frac{1}{3}+\frac{1}{4}+\dots$$
*Cálculo auxiliar $\frac{1}{n} \rightarrow 0$*

El criterio básico *no dice nada*...  sin embargo,
$$1+\frac{1}{2}+\frac{1}{3}+\frac{1}{4}+\frac{1}{5}+\frac{1}{6}+\frac{1}{7}+\frac{1}{8}=S_{8=2³}> \atop 1+\frac{1}{2}+\frac{1}{4}+\frac{1}{4}+\frac{1}{8}+\frac{1}{8}+\frac{1}{8}+\frac{1}{8}=1+\frac{3}{2}$$
podemos remplazar el denominador por el techo de la potencia de dos más cercana.

---
### Criterio 2
Si $\sum |a_{n}|$ es convergente, entonces $\sum a_{n}$ es convergente.
> [!warning]
> NO vale para la recíproca! 

Diremos que $\sum a_{n}$ es condicionalmente convergente cuando 
	- $\sum a_{n}$ converge,
	- $\sum |a_{n}|= +\infty$ (diverge).
Ejemplo: $1-\frac{1}{2}+\frac{1}{3}-\frac{1}{4}+\frac{1}{5}\dots=\sum_{k=1}^{+\infty} \frac{(-1)^{n+1}}{n}$
$$\frac{-1^{n+1}}{n} \longrightarrow 0$$
$$|\frac{(-1)^{n+1}}{n}|=\frac{1}{n} \implies \sum \frac{1}{n}~ diverge$$
---
## Proposición
-  Si $a_{n} \geq 0$ (de términos positivos), entonces $\sum a_{n}$ siempre tiene límite (2 clasificaciones):
	- $\sum_{n=1}^{\infty}a_{n}<\infty$ **CONVERGE.**
	- $\sum_{n=1}^{\infty} a_{n}> \infty$ **no llegué concha**
---
```ad-info
Notación: Para series de términos positivos notaremos **$\sum a_{n}⁺< \infty$** para indicar **"convergencia"**.

```

Nota: Si $\sum |a_{n}| < \infty$ (converge), entonces la suma es invariante bajo permutaciones de sus términos.
$$a_{1}+a_{2}+a_{3}+a_{4}+\dots=S \atop a_{2}+a_{5}+a_{84}+a_{3}+a_{975}+a_{11}+\dots=S$$
Nota: Si $\sum |a_{n}| = +\infty$ y $\sum a_{n}$ es convergente, entonces:
	**1º.** #$\{ n:a_{n}>0\}$ infinita
	**2º.** #$\{ n: a_{n} <0\}$ infinita
	**3º.** Si $M \in \mathbb{R} \implies $ existe permutación $b:\mathbb{N} \to \mathbb{N}$ tal que $a_{b(1)}+a_{b(2)}+\dots=M$. 