# relacion de recurrencia lineal homogenea
## orden de una relacion de recurrencia
cuando una relacion de recurrencia depende de $k$ terminos anteriores, es de orden $k$.
ej: $x_n -2x_{n-1} = 0$ es de orden 1
## linealidad
es lineal si los exponentes de todos los términos de recurrencia son 1.

## homogeneidad
es homogénea una relación de recurrencia $f(n) = c$ si se expresa como
$$
f(k) = 0
$$
-------
# recurrencias de primer orden
## ejemplo
dado
$$
x_n -2x_{n-1} =0
$$

se puede ver haciendo algunos ejemplos que la expresion pareceria ser $x_n=2^{n}\cdot x_0$ con $x_0$ siendo el termino inicial
### caso base
vemos para $n=1$
$$
\begin{align}
x=1 = 2^{1}x_0 = 2x_0
\end{align}
$$

### induccion
asumiendo que vale
$$
x_n = 2^{n}x_0
$$

probamos que
$$
\begin{align}
x_{n+1} = 2\cdot x_n &= \\
2\cdot x_n \stackrel{\mathclap{\tiny\mbox{hip}}}{=} 2\cdot 2^{n}x_0 &= 2^{n+1}x_0 
\end{align}
$$
----------
# recurrencias de segundo orden
dado
$$
x_{n+2} + x_{n+1} - 2x_n = 0
$$
con
$$
\begin{array} \\
x_0 = 1 \\
x_1 = 2
\end{array}
$$
## proponemos solucion
asumimos 
$$
x_n = c r^{n}
$$
$$
\begin{align}
c r^{n+2} + c r^{n+1} -2cr^{n} =0 \\
\underbrace{ c r^{n} }_{ \neq0 }\cdot \underbrace{ (r^{2}+r - 2) }_{ \tiny \mbox{ polinomio caracteristico } } = 0
\end{align}
$$

>[!NOTE] Nota
>siempre que tengamos una recurrencia de orden $k$
, tendremos un *polinomio caracteristico* de orden $k$.

si el polinomio caracteristico es 0, entonces la relacion se cumple.

para este caso, el polinomio tiene raices
$$
r^{2}+r-2 = \left\{ \begin{array} \\
r = 1 \\
r=-2
\end{array} \right.
$$
por lo tanto
$$
x_n = c_1 1^{n} + c_2 (-2)^{n}
$$
## encontramos los coeficientes
los coeficientes dependen de los valores iniciales.

%% TODO: hacer%%

