#ejercicio/incompleto 
# a
$$
x_{n+2}=6x_{n+1}-8x_n 3n-4
$$
con $x_0 = 1, x_1 = 5$

## resolución
$$
\begin{align}
x_{n+2}-6x_{n+1}+8x_n=\underbrace{ 3n-4 }_{ \neq 0 } \\
\end{align}
$$
### parte homogenea
$$
\begin{align}
x_{n+2}-6x_{n+1}+8x_n =0
\end{align}
$$
propongo $x_n=c\cdot r^{n} \neq0$
$$
\begin{align}
cr^{n+2}-6cr^{n+1}+8cr^{n}=0 \\
cr^{n}\underbrace{ (r^{2}-6r+8) }_{ \tiny r_1 = 4, r=2 =2 }=0
\end{align}
$$
entonces la solucion general de la ecuacion homogenea es
$$
x_n = A(4)^{n} + B(2)^{n}
$$
### parte particular

propongo $x_n = p\cdot n+q$

y reemplazo en la ecuacion
$$
\begin{align}
p(n+2) +q -6[p(n+1)+q]+8(pn+q)=3n-4 \\
pn+2p+q-6pn-6p-6q+8pn+8q=3n-4 \\
3pn-4p+3q=3n-4 \\
\left\{ \begin{array}
3p=3 \implies p=1 \\
-4p+3q=-4 \implies q=0
\end{array} \right.
\end{align}
$$

entonces
$$
\begin{align}
x_n = (\text{homogenea}) + (\text{particular}) \\
 x_n = A 4^{n} + B 2^{n} + n
\end{align}
$$

# c

$$
x_{n+1} = x_n +2n
$$
con $x_0 =3$

## resolución

$$
x_{n+1} - x_n = 2n
$$

### parte homogenea
$$
\begin{align}
x_{n+1} - x_n =0 \\
cr^{n+1} - cr^{n}=0 \\
cr^{n}\underbrace{ (r-1) }_{ r=1 }=0
\end{align}
$$
solucion general homogenea: $x_n=A(1)^{n}=A$
### parte particular
proponemos
$$
x_n = pn^{2}+qn+2
$$

reemplazamos
$$
\begin{align}
&p(n+1)^{2}+q(n+1)+r-[p(n)^{2} + q(n)+r]=2n \\
&\vdots \\
&p=1 , q=-1
\end{align}
$$

solucion
$$
x_n=A+n^{2}-n
$$
si $x_0=3$, entonces
$$
x_0 = 3 = A +0 - 0
$$

$$
x_n = 3 + n^{2}-n
$$

# b
$$
x_{n+1}=2^{n+1}-x_n
$$
con $x_0=1$
$$
\begin{align}
x_{n+1}+x_n=2^{n}2
\end{align}
$$
## resolución
### parte homogenea
$$
\begin{align}
x_{n+1}+x_n=0 \\
cr^{n+1}+cr^{n}=0 \\
cr^{n}\underbrace{ (r+1) }_{ r\ =\ -1 } = 0\\
\end{align}
$$

solucion homogenea: $x_{n} = A(-1)^{n}$
### parte particular
$$
x_n = k 2^{n}
$$

$$
\begin{align}
k2^{n+1}+k2^{n}=2^{n}2 \\
2^{n}(2k+k)=2^{n}2 \\
3k = \frac{2^{n}2}{2^{n}} \\
\implies k = \frac{2}{3}
\end{align}
$$

solucion
$$
x_n = A(-1)^{n}+\frac{2}{3}2^{n}
$$
si $x_0=1$, entonces
$$
x_0=1=A+\frac{2}{3} \implies A = \frac{1}{3}
$$
$$
x_n = \frac{1}{3}(-1)^{n}+\frac{2}{3}2^{n}
$$

# ejemplo suelto

$$
x_{n+2}-6x_{n+1}+9x_n=f(n)\neq0
$$

## parte homogenea
proponemos $x_n=cr^{n}$

$$
\begin{align}
cr^{n}\underbrace{ (r^{2}-6r+1) }_{ \tiny r_1=r_2=3 }=0
\end{align}
$$

entonces la solucion homogenea es

$$
x_n = A 3^{n}+ B 3^{n}n
$$
donde multiplicamos por uno de los términos por $n$ dado que el polinomio característico tiene una raíz doble y necesitamos que sean términos# linealmente independientes

## parte particular

si $f(n)=n^{2}5^{n}+n3^{n}$ (??)
entonces
$$
x_n=(pn^{2}+qn+r)5^{n}+kn^{2}3^{n}
$$
si $f(n)=8+n^{2}3^{n+1}=8+n^{2}3^{n}3$
<<cosas>>


