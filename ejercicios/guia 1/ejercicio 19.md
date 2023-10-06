#ejercicio/completo
# consigna
[[Notas guía 1#^56ve5roujst|en la guia]]

Probar que dados $A$ y $B$ en $I$ la ecuación en la incógnita X dada por $AX + B\overline{ X} = \varnothing$ tiene solución *sii* $B \subset \overline{ A}$ (o lo que es equivalente $AB = \varnothing$) y es cualquier conjunto $X$ en $I$ que satisfaga $B \subset X \subset \overline{ A}$ (a $B$ se le llama solución minimal y a $\overline{ A}$ solución maximal). Si, cumpliendo $AB = \varnothing$, es $n_a = |A|,n_{b} = |B|,n_{i} = |I|$, determinar el cardinal del conjunto $S = \{ X \subset I : AX + B\overline{ X} = \varnothing \}$ 
¿Bajo qué condiciones la solución es única? ¿Qué soluciones tiene la ecuación $(A + \overline{ A})X + \overline{ X} = \varnothing$?
# resolución

Usando las propiedades [[Propiedades útiles de Algebra de Conjuntos#Equivalencia|esta]] y [[Propiedades útiles de Algebra de Conjuntos#subconjunto|esta]] de algebra de conjuntos, sabemos que podemos escribir la relación $AX + B\overline{ X} = \varnothing$ como:
$$
\begin{align}
AX + B\overline{ X} = \varnothing  \\
AX = \varnothing \ \wedge B\overline{ X}=\varnothing  \\
(X \subset \overline{ A}) \ \wedge (B \subset X) \\
B \subset X \subset \overline{ A}
\end{align}
$$

Por lo tanto, tenemos que cualquier conjunto $X \subset I$ que cumpla con $B \subset X \subset \overline{ A}$ deberia satisfacer la ecuación, y que ademas (por transitividad) se cumple sii $B \subset \overline{ A}$

## cardinal de $S$

$S$ es el conjunto formado por todos los conjuntos que cumplen con la ecuación de la consigna.  
Tenemos al menos 2 soluciones, correspondientes con la solución minimal y maximal, o sea $X_{1} = B$ y $X_{2} = \overline{ A}$  
Los otros conjuntos son conjuntos entre $B$ y $\overline{ A}$, o sea que contienen Todos los elementos de $B$ y algunos de $\overline{ A}$.

Como $A$ tiene cardinalidad $n_{a}$ , tenemos que $|\overline{ A}| = |I| - |A| = n_{i} - n_{a}$
Como estas otras soluciones son conjuntos entre $B$ y $\overline{ A}$, para "armarlos" debemos agregar elementos de $\overline{ A}$ a $B$ hasta llegar a $\overline{ A}$, encontrando todos los posibles conjuntos en el camino. Entonces sabemos que tenemos $n_{i}-n_{a}-n_{b}$ elementos para agregar a $B$.

Si agregamos 1 elemento a B, tenemos $\binom{n_{i}-n_{a}-n_{b}}{ 1} = n_{i}-n_{a}-n_{b}$ posibles opciones. Si agregamos 2, tenemos $\binom{n_{i}-n_{a}-n_{b}}{2}$ posibles opciones. Debemos hacer esto hasta alcanzar a agregar todos los elementos de $\overline{ A}$ que no estaban en $B$. Por lo tanto la cardinalidad de S será:
$$
|S| = \sum_{k = 0}^{n_{i}-n_{a}-n_{b}} \binom{n_{i}-n_{a}-n_{b}}{k}
$$
Pero no tengo idea como reducir eso. Así que lo pensamos de esta otra manera:
Si pensamos en esos $n_{i}-n_{a}-n_{b}$ elementos como un vector binario donde cada posición representa si se incluye ese elemento de $\overline{ A}\cdot \overline{ B}$ o no, 
podemos asociar cada posible conjunto solución $X_{k}$ con un número binario.
$$
\begin{align}
X_{0} \to &\begin{bmatrix}
0 \\
0 \\
0 \\
\vdots \\
0
\end{bmatrix} = 0
\to B \\
X_{1} \to &\begin{bmatrix}
1 \\
0 \\
0 \\
\vdots \\
0
\end{bmatrix} = 1 \to B \cup \{ e_{1} \} : e_{1} \in \overline{ A}\cdot \overline{ B} = \overline{ A+B} \\
\vdots \\
X_{n_{i}-n_{a}-n_{b}} \to &\begin{bmatrix}
1 \\
1 \\
\vdots \\
1
\end{bmatrix} = 2^{n_{i}-n_{a}-n_{b}} - 1 \to \overline{ A}
\end{align}
$$
De esta manera vemos que tenemos $2^{n_{i}-n_{a}-n_{b}}$ posibles vectores y por lo tanto, $2^{n_{i}-n_{a}-n_{b}}$ posibles subconjuntos de $S$.

Por lo tanto, la cardinalidad de $S$ es $|S| = 2^{n_{i}-n_{a}-n_{b}}$



## solucion unica
La solucion es única sii $B = \overline{ A}$

## otra ecuacion

soluciones de $(A + \overline{ A})X + \overline{ X} = \varnothing$

$$
\begin{align}
\underbrace{ (A + \overline{ A}) }_{ I }X + \overline{ X} &= \\
IX + \overline{ X} = X + \overline{ X} &= I\\
I \neq \varnothing &\implies \mbox{ no existen soluciones }
\end{align}
$$