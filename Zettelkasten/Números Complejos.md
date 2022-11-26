**Created:** Tuesday 15, November 2022, at 09:09.
**Status:** #school-note 
**Tags:** [[Elementos de Álgebra y Geometría]]

# Números Complejos

## Definición: 
Sea $\mathbb{C}= \mathbb{R} \times \mathbb{R}$ el conjunto de todos los pares ordenados $(a,b)$ de números reales sobre el cual definimos las siguientes operaciones:
1. **Suma:** Dados $(a,b) ~y~ (c,d) \in \mathbb{C}$, $(a,b)+(c,d)=(a+c,b+d)$
2. **Producto:** Dados $(a,b)$ y $(c,d) \in \mathbb{C}$, $(a,b) \cdot (c,d)= (ac-bd, ad+bc)$.

## Propiedades:
**($S_{1}$)** $(z+u)+w=z(u+w)$, para todo $z,u,w \in \mathbb{C}$.
**($S_{2}$)** $z+w=w+z$, para todo $z,w \in \mathbb{C}$.
**($S_{3}$)** Existe un único elemento $0=(0,0) \in \mathbb{C}$, tal que $z+0=z$, para todo $z\in \mathbb{C}$.
**($S_{4}$)** Para cada $z=(a,b) \in \mathbb{C}$, existe un único elemento $-z=(-a,-b)$ tal que $z+(-z)=0$.
**($M_{1}$)** $(z \cdot u)\cdot w= z \cdot (u \cdot w)$, para todo $z,u,w \in \mathbb{C}$.
**($M_{2}$)** $z\cdot w=w \cdot z$, para todo $z,w \in \mathbb{C}$.
**($M_{3}$)** Existe un único elemento $1=(1,0) \in \mathbb{C}$, tal que $z\cdot 1=z$, para todo $z\in \mathbb{C}$.
**($M_{4}$)** Para cada $z=(a,b) \in \mathbb{C}$, $z \neq 0$, existe un único elemento $z^{-1}= \left( \frac{a}{a²+b²}, \frac{-b}{a²+b²} \right)$, tal que $z \cdot z^{-1}=1$.
**($D$)** $z\cdot(u+w)=z \cdot u+ z \cdot w$, para todo $z,u,w \in \mathbb{C}$.

---
La función f : R → C definida por: f (a) = (a, 0), para todo a ∈ R, es inyectiva, como es inmediato de verificar. Además verifica que f (a + b) = f (a) + f (b) y f (a · b) = f (a) · f (b), para todo a, b ∈ R, es decir, preserva las operaciones de suma y multiplicación. En efecto, $$\begin{cases}f (a + b) = (a + b, 0) = (a, 0) + (b, 0) = f (a) + f (b),  
\\
f (a · b) = (a · b, 0) = (a, 0) · (b, 0) = f (a) · f (b).
\end{cases}$$Esto significa que los números de la forma (a, 0) se comportan, respecto de las operaciones de suma y multiplicación, como los números reales a. Esto permite identificar el complejo (a, 0) con el número real a.

---
## Representación geométrica de los números complejos
Teniendo en cuenta que los números complejos se han definido como pares ordenados de números reales, es natural representarlos en un sistema de coordenadas cartesianas ortogonales.
![[Pasted image 20221115093153.png]]
Si z es un complejo real, entonces su afijo está sobre el eje de las abscisas, que por esta razón se llama eje real. Si z es imaginario puro, entonces su afijo está sobre el eje de las ordenadas, que recibe el nombre de eje imaginario.

### Unidad imaginaria
Veamos ahora que en $\mathbb{C}$ tiene solución la ecuación $x²+1=0$, o sea, $x²=-1$, y que la solución está dada por el número complejo $(0,1)$.
Recordemos que la unidad real 1 la podemos escribir como el número complejo $(1,0)$. Por otro lado, si $x=(0,1)$ se tiene: $$x²=(0,1) \cdot (0,1) \atop x²=(0 \cdot 0 - 1\cdot 1, 0 \cdot 1 +1 \cdot 0)= (-1,0)$$
Entonces, si en la ecuación $x²+1=0$ reemplazamos $x=(0,1)$, se tiene: $$(-1,0)+(1,0)=(0,0)=0$$
### Definición 7.2:
*El número complejo $(0,1)$ recibe el nombre de unidad imaginaria y se nota $i=(0,1)$.*

---
## Forma binómica
Vamos a ver ahora que todo número complejo $z=(a,b)$ puede escribirse en la forma $a+bi$.
Es claro que $(a,b)=(a,0)+(0,b)$. Pero $(0,b)$ puede escribirse $(0,b)=(b,0)\cdot(0,1)$, reemplazando tenemos que $$(a,b)=(a,0)+(b,0\cdot (0,1))$$
Luego, identificando $(a,0)$ con $a ~y~ (b,0)$ con $b$, $$(a,b)=a+bi$$
```ad-important

La forma binómica nos permite aplicar para la suma y el producto de números complejos todas las propiedades válidas en $\mathbb{R}$, con sólo tener en cuenta que $i²=-1$.
```

Ejemplos: 
1. **Suma:** $z+z'=(a+bi)+(c+di)=(a+c)+(b+d)i$
2. **Diferencia:** $z-z'=(a+bi)-(c+di)=(a-c)+(b-d)i$
3. **Producto:** $z\cdot z'=(a+bi)\cdot(c+di)=(ac-bd)+(ad+bc)i$
4. **Cociente:** $\frac{z}{z'}=\frac{a+bi}{c+di}, z'\neq_{0}$.

---

### Conjugado de un número complejo:
#### Definición 7.3
```ad-info

Dado el número complejo $z=(a,b)$, ó en su forma binómica $z=a+bi$, llamaremos conjugado de $z$ al número complejo $\overline{z}=(a,-b)$ ó, en su forma binómica, $\overline{z}=(a-bi)$.
```

### Propiedades del conjugado
Sea $z=a+bi$, entonces:
1. $\overline{z}= z$
2. $z+ \overline{z}=2~Re~z$, ($z+ \overline{z}=2a$)
3. $z- \overline{z}=2~Im~z~i$, ($z-\overline{z}=2b~i$)
4. $z \cdot \overline{z}= |z|² =a²+b²$
5. $z=\overline{z} \iff z \in \mathbb{R}$
6. $z=-\overline{z} \iff z$ es imaginario puro, ó $z=0$
7. $\overline{z+z'}=\overline{z}+\overline{z'}$
8. $\overline{z-z'}=\overline{z}-\overline{z'}$
9. $\overline{z \cdot z'}= \overline{z} \cdot \overline{z'}$
10. $\overline{\left( \frac{z}{z'} \right)}=\frac{\overline{z}}{\overline{z'}}$, si $z' \neq 0$

---
## Propiedades del módulo
Sea $z=a+b~i$, entonces:
1. $|z| \geq 0$
2. $|z| \geq a \land |z| \geq b$
3. $|z|²=z\cdot \overline{z}$
4. $|z|=|\overline{z}|=|-z|$, $(\sqrt{ a²+b² }=\sqrt{ a²+(-b)² }= \sqrt{ (-a)²+(-b)² })$
5. $|z\cdot z'|=|z|\cdot|z'|$
6. $|\frac{z}{z'}|=\frac{|z|}{|z'|}$, si $z'\neq 0$
7. $|z+z'| \leq |z| + |z'|$
8. $| |z|-|z'| | \leq |z-z'|$

la puta madre quiero las notas nomás


---
## References:
- 