# consigna
![[Notas guía 1#^0zoswalt2cq]]

```tikz
\begin{document}
\begin{tikzpicture}
  \node (max) at (0,4) {$42$};
  \node (a) at (-2,2) {$6$};
  \node (b) at (0,2) {$14$};
  \node (c) at (2,2) {$21$};
  \node (d) at (-2,0) {$2$};
  \node (e) at (0,0) {$3$};
  \node (f) at (2,0) {$7$};
  \node (min) at (0,-2) {$1$};
  \draw (min) -- (d) -- (a) -- (max) -- (b) -- (f)
  (e) -- (min) -- (f) -- (c) -- (max)
  (d) -- (b);
  \draw[preaction={draw=white, -,line width=6pt}] (a) -- (e) -- (c);
\end{tikzpicture}
\end{document}
```



# Resolucion
los divisores de 42 son $D_{42} = \{ 1,2,3,7,6,14,21,42 \}$

Por lo tanto tenemos que los conjuntos $A$ y $B$ son:
$$
\begin{array} \\
A = \{ x \in D_{42} : \underbrace{ x \leq 3 }_{ x | 3 } \} = \{ 1,3 \}   \\
B = \{ x \in D_{42} : \underbrace{ (x+3) \leq 6 }_{ \text{mcm}(x,3)|6 } \} = \{ 1,2,3,6 \}\\
\end{array}
$$


Queremos encontrar el conjunto $S$ formado por conjuntos $X \subset S$ tales que se cumpla
$$
AB + \overline{X} = B
$$
Dado a que sabemos que $A \subset B$, sabemos que $AB = A$, por lo tanto podemos escribir la expresion como
$$
A + \overline{X} = B
$$
Vemos que
$$
\begin{align}
(A+\overline{ X})\cdot \overline{ B} = B\cdot \overline{ B} = \varnothing \\
\underbrace{ A\cdot \overline{ B} }_{ \varnothing } + \overline{ XB} = \varnothing \\
\overline{ XB} = \varnothing  &  & &{\small\mbox{: dado que } A\cdot B = A \implies A\cdot \overline{ B} = \varnothing} \\
\overline{ B} \subset X  &  & &\mbox{: definicion de } M\subset N
\end{align}
$$

podemos encontrar una expresion equivalente a esta mediante la ley de [[Algebra de Bool#leyes de DeMorgan|DeMorgan]] para 
tener una version mas simple:
$$
\begin{align}
A + \overline{X} = B  \\
\overline{(A + \overline{ X})} = \overline{ B} \\
\overline{ A} \cdot X = \overline{ B}
\end{align}
$$
De esto se desprende que 
$$
\begin{align}
\overline{ A} \cdot X \cdot B = \overline{ B}\cdot B = \varnothing \\
X\cdot \overline{(A+\overline{ B})} = \varnothing  & &  \mbox{ : ley de DeMorgan sobre } \overline{ A}B \\
X \subset (A+\overline{ B})  &  & \mbox{ : definicion de } M\subset N
\end{align}
$$

Esto nos restringe $X$ a cumplir con $\overline{ B} \subset X \subset A + \overline{ B}$
Por lo tanto, el minimo conjunto $X$ es
$$
\min\{ X : X \subset X \} = \overline{ B}
$$
y la cardinalidad de $\overline{ B}$ es $|\overline{ B}| = |I - B| = 4$

De la misma manera, el conjunto máximo de $X$ es
$$
\max\{ X : X \subset S \} = A + \overline{ B}
$$
donde $A + \overline{ B}$ tiene cardinalidad $|A + \overline{ B}| = 6$


## Conjuntos de S
para obtener todos los conjuntos de S, tenemos en cuenta que todos los $X$ que conforman $S$ cumplen la relación (arriba). 
Por lo tanto podemos ir armando esos conjuntos si partimos de $\overline{ B}$ y vamos agregando de a 1 los elementos de $A+\overline{ B}$ que 
no estan en $\overline{ B}$:[^1]
$$
\begin{align}
S_{1} = \overline{ B}  \\
S_{2} = \overline{ B} \ \cup  \{ 1 \} \\
S_{3} = \overline{ B} \ \cup  \{ 3 \} \\
S_{4} = A + \overline{ B}
\end{align}
$$
Por lo que la cardinalidad de $S$ es $|S| = 4$

[^1]: Los conjuntos $\overline{ B}$ y $A + \overline{ B}$ son conocidos y pueden ser calculados.

