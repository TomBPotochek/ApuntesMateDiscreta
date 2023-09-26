# Principio de induccion matematica
Sea $S(n)$ un enunciado con valor de verdad, $n \in \mathbb{N}$, es verdadero para todo $n$ si se cumple que:
1. $S(1)$ es verdadero
2. si $S(k)$ es verdadero con $k>1$, $S(k+1)$ es verdadero.

## ejemplo
Demostrar que $\sum_{i=1}^{n} i = \frac{n(n+1)}{2}$

### caso base
Demostramos la proposicion para $n=1$
$$
\begin{align}
\sum_{i=1}^{1} i &= 1 \\
\frac{1(1+1)}{2} = \frac{2}{2} &= 1
\end{align}
$$
Por lo tanto es verdadero para $n=1$

### induccion
Suponiendo que $S(k)$ es verdadero, demostramos que $S(k+1)$ es verdadero
$$
\begin{align}
S(k) = \sum_{i=1}^{k} i &= \frac{k(k+1)}{2}  &  & \mbox{ : hipótesis } \\
S(k+1) = \sum_{i=1}^{k+1} i &= k+1 + \sum_{i=1}^{k} i  &  & \mbox{: definicion sumatoria } \\
&= k + 1 + \textcolor{green}{ \frac{k(k+1)}{2} }  &  & \mbox{ : por hipotesis }  \\
= \frac{k+1}{2}(2+k) &= \frac{(k+1)(k+2)}{2} 
\end{align}
$$

$\implies S(n)$ es verdadero $\forall n \in \mathbb{N}$ por inducción 