> Determinar el complemento de cada uno y el 0 y 1 de $B$ para que sea un algebra de Boole

Tomamos $\alpha = 0_B$ y $\omega = 1_B$

Luego usamos un isomorfismo a los divisores de 42 para determinar facilmente los complementos, ya que sabemos que ambos tienen la misma cardinalidad y ambos son algebras de Boole.
En los divisores de 42, el complemento de $x$ se calcula como $\bar{x}=\frac{42}{x}$ por lo tanto es facil saber el complemento si miramos la preimagen de ese numero en el isomorfismo.

Del diagrama de Hasse, sabemos que
$$
\begin{array} \\
a + f = \omega \\
a \cdot f = \alpha \\
\dots
\end{array}
$$
entonces definimos un isomorfismo $\text{f}$ (cualquiera, mientras sea isomorfismo) ej: $\text{f}(a) = 2, \text{f}(b) = 7,$ etc. Entonces sabemos que $\bar{b} = \text{f}(\ \overline{ \text{f}(b)}\ )^{-1} = \text{f}(\bar{7})^{-1} = \text{f}(\frac{42}{7})^{-1}$ y asi.


## subalgebras
Todas las subalgebras de boole deben tener cardinalidad $2^{n}$, ademas sabemos que por cada elemento, debe estar su complemento (ley del complemento) y ademas su suma y producto.

$$
\begin{array} \\
H_1 = B \\
H_2 = \{ \alpha, \omega \}  \\
H_3 = \{ \alpha, \omega, a, d \} \\
H_4 = \dots  \\
H_5 = \dots 
\end{array}
$$

## resolver sistema
dado la relacion de orden $A\leq B$ tenemos que
$$
\begin{array} \\
A\cdot B = A \\
A+B=B
\end{array}
$$



