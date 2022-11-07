# Criterios para series de términos positivos

## **1º Criterio:**"Criterio de comparación" (básico)
Si $0 \leq a_{n},b_{n}$ y $a_{n} \leq b_{n}$, con $n>n_{0}$, entonces vale las siguientes afirmaciones:
- Si $\sum b_{n}< \infty \implies \sum a_{n}< \infty$
- Si $\sum a_{n}= +\infty \implies \sum b_{n}=+\infty$
```ad-info
Decir que la sumatoria es finita, nos indica que esta converge.

```
**Ejemplo:** $$\sum_{2}^{\infty} \frac{1}{\ln n}$$
Recordamos que $\ln(n)<n<e^n$ y $$\text{deducimos que }\frac{1}{n}< \frac{1}{\ln n}  \atop \text{y como }\sum \frac{1}{n} = +\infty $$
entonces, $\sum \frac{1}{\ln n}=+\infty$

**Ejemplo:** $$\sum \frac{n²+3n}{2n³+3n²+1}$$ 
$$\frac{n²+3n}{2n³+3n²+1}< \frac{n²+3n}{n³+3n²}=\frac{1}{n} \leftarrow \text{diverge}$$
esta acotación no es útil ¿cómo mejorar?

## 2º Criterio: "Comparación por límite"
- $0 \leq a_{n}, b_{n}$
- $\frac{a_{n}}{b_{n}} \to L \neq 0 \land L \neq +\infty$, esto implica que ambas series $\sum a_{n}$ y $\sum b_{n}$ tienen idéntica clasificación, esto significa que **ambas convergen** ó **ambas divergen**.
Equivale a obtener una expresión asintótica $a_{n} \approx L \cdot b_{n}$.

En el  ejemplo $$\frac{n²+3n}{2n³+3n²+1} a_{n} = \frac{n²\left( 1+\frac{3}{n} \right)}{2n³\left( 1+\frac{3}{2n}+\frac{1}{2n³} \right)}$$ $$=\frac{1}{2n} \cdot \frac{1+\frac{3}{n}}{1+\frac{3}{2n}+\frac{1}{2n³}}$$
Entonces$$\frac{a_{n}}{b_{n}}=\frac{1+\frac{3}{n}}{1+\frac{3}{2n}+\frac{1}{2n³}} \to \neq 0, +\infty$$
El **criterio de "comparación por límite"** asegura que $\sum \frac{n²+3n}{2n³+3n²+1}$ es equivalente a $\sum \frac{1}{2n} = \frac{1}{2} \sum \frac{1}{n}$, y como $\sum \frac{1}{n}$ diverge $\implies \sum \frac{n²+3n}{2n³+3n²+1}$ también diverge.

```ad-important
$$\text{acotadas:}sen(n),etc\ll\text{logarítmicas: }(\ln n)^q\ll \text{potencias:}n^r\mid \ll \text{exponenciales: }a^n\ll\text{factoriales: }n!\ll\text{nose: }n^n$$
El criterio del cociente tiene sentido a partir de las exponenciales, antes de estas no aporta información.

```

**Ejemplo:** $\sum \frac{n²+3n+1}{n³+2^n+5}$
C.A. "Criterio de comparación por límite"
$$\frac{n²\left( 1+\frac{3}{n}+\frac{1}{n²} \right)}{2^n\left( \frac{n³}{2^n}+1+\frac{5}{2^n} \right)}=\frac{n²}{2^n} \cdot\left(  \frac{1+\frac{3}{n}+\frac{1}{n²}}{1+\frac{n³}{2^n}+\frac{5}{2^n}} \right)$$
$$\frac{n²}{2^n} \cdot \frac{1}{1}$$Luego, aplicamos el criterio del cociente: $$\frac{(n+1)²}{2^{n+1}}\cdot \frac{2^n}{ n²}=\frac{2^n}{2^{n+1}}\cdot \frac{(n+1)²}{n²}=\frac{1}{2}$$

---
## 2º **"Criterio de la raíz"**
- $0 \leq a_{n}$, (en cocientes $0<a_{n}$)
- $^n\sqrt{ a_{n}} \longrightarrow L$
Entonces: $$\text{si }L<1, \sum a_{n}< \infty \atop \text{si }L>1, \sum a_{n} = +\infty$$
Recordar que tanto el criterio del cociente como el criterio de la raíz son iguales. $\frac{a_{n+1}}{a_{n}}\to L ~\land~ ^n\sqrt{ a_{n} } \to M \implies L=M$.

---
## 3º **"Criterio de la integral"**
- $a_{n}=f(n)$ con $f(x) \geq 0, \text{en } [M, \infty]$
En ese caso, $\sum a_{n}$ y $\int _{M}^{⁺\infty} f(x) \, dx$ se clasifican igual.

Ejemplo: $\sum \frac{1}{n \ln (n)}$
$$f(x)=\frac{1}{x \ln(x)}, \text{ con x $\geq 2$}$$
$$\int_{2}^{+\infty} \frac{1}{x \ln(x)}\, dx = \lim_{ P \to \infty }  \int_{2}^{P} \frac{1}{x \ln(x)}  \, dx $$
$$=\lim_{P \to \infty} $$

## **Proposición:**
$$\sum \frac{1}{n^P} \begin{cases}
\text{converge si } P>1 \\ \text{diverge si } P<1
\end{cases}$$
[CONCHAAA]
## **Hipótesis:**
