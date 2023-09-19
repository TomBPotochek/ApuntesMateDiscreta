ver [[ejercicio 38]]


$$
\begin{array} \\
(B_1, +_1,\cdot_1 ,\bar{\ }_{1},0_1,1_1) AB (\mbox{ algebra de boole}) \\
(B_2, +, \cdot_2 ,\bar{\ }_{2},0,1) AB \\
f:B_1 \to B_2 \mbox{ es biyectiva sii } \\
\begin{array}
\forall x,y \in B_1 f(x+_1y) = f(x) +_2 f(y) \\
\forall x,y \in B1 f(x\cdot_1 y) = f(x) \cdot_2 f(y) \\
\forall x f(\bar{x}) = \bar{f(x)} \\
\end{array}
\end{array}
$$
claramente, ambas algebras deben tener la misma cantidad de elementos
## propiedades

$$
\begin{array} \\
 f(0_1) = 0_2 \\
f(1_1) = 1_2 \\
\forall x,y\ \  x\leq_{1} y \implies f(x) \leq_{2} f(y) \\
a \mbox{ es atomo en } B_1 \implies f(a) \mbox{ es atomo en } B_2
\end{array}
$$

Basta con definir la funcion sobre el 0, el 1 y los atomos para definirla de forma unica.

### 1
$$
\begin{split}
f(0_1) &= f(x\cdot_1 \bar{x}) = f(x) \cdot_2 f(\bar{x}) = \\
&= f(x) \cdot_2 \bar{f(x)} = 0_2 \\
\end{split}
$$
### 2
$$
\begin{split}
f(1_1) &= f(x+_1 \bar{x}) = f(x) +t_2 f(\bar{x}) = \\
&= f(x) +_2 \bar{f(x)} = 1_2
\end{split}
$$

### 3
$$
\begin{split}
x \leq_1 y \to x \cdot_1 y = x \to \dots
\end{split}
$$

### 4







