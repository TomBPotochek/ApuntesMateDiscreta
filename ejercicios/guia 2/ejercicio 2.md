# b
Probar $\forall n \in \mathbb{N} \equiv n \geq 1$ la expresión:
Usamos el [[Inducción#Principio de induccion matematica|principio de induccion]]
$$
\sum_{k=1}^{k=n} k^{2} = \frac{1}{6}n(n+1)(2n+1)
$$
caso base $k=1$:
$$
\sum_{k=1}^{1} k^{2} = 1^{2} \\
\frac{1}{6}1(1+1)(2+1) = \\
\frac{1}{6}6 = 1
$$
Luego hacemos el paso de inducción:

asumiendo que vale para $n$, 
$$
\sum_{k=1}^{n+1}
$$
%% TODO: falta terminarlo %%

# e
probar
$$
P(n) = \sum_{i=0}^{n-1} a^{i}=\frac{a^{n}-1}{a-1}, a \neq 1
$$

## caso base
probamos para $i = 0$
$$
\begin{align}
P(1) = \sum_{k=0}^{0} a^{i} = a^{0} &= 1 \\
\frac{a^{1}-1}{a-1} &= 1
\end{align}
$$

## induccion
asumiendo que vale $P(t) = \sum_{k=0}^{t-1} a^{k} = \frac{a^{k}-1}{a-1}$

$$
\begin{align}
P(t+1) = \sum_{k=0}^{t} a^{k} &= \sum_{k=0}^{t-1} + a^{t}  \\
= \frac{a^{t+1}-1}{a-1} + a^{t} &=  & \mbox{ : por hipotesis } \\
= \frac{a^{t+1} -1 + a^{t+1}+ a^{t}}{a-1} &= \frac{a^{t}-1}{a-1}
\end{align}
$$


# ñ
Probar $\forall n \geq 1$ 
$$
(1+\alpha)^{n} \geq (1 +n \alpha), \alpha \geq -1
$$
## caso base
$n=1$
entonces
$$
\begin{align}
(1+\alpha)^{1} \geq (1 + 1\alpha) \\
(1+\alpha) \geq (1+\alpha)
\end{align}
$$

## induccion
Asumiendo $(1+\alpha)^{n}\geq(1+n\alpha)$
Si $n := n+1$
$$
\begin{align}
(1+\alpha)^{n+1} &\stackrel{\mathclap{\tiny\mbox{?}}}{\geq}  (1+(n+1)\alpha)  \\
(1+\alpha)^{n+1} = (1+\alpha)^{n}(1+\alpha) &\geq (1+n\alpha)(1+\alpha) = (1+(n+1)\alpha)\\
(1+\alpha)^{n}\cancel{ (1+\alpha)  }&\geq (1+n\alpha)\cancel{ (1+\alpha) }  & {\tiny\text{: } \alpha>-1\implies 1+\alpha>0 \implies \mbox{ desigualdad se mantiene }} \\
(1+\alpha)^{n} &\geq (1+n\alpha)  &  {\tiny \mbox{: por hipostesis es verdad }}
\end{align}
$$


# l
para $n\geq1$
$$
133 | (11^{n+2} + 12^{2n+1})
$$
## caso base
si $n=1$:
$$
\begin{align}
11^{2} + 12^{2\cdot 1+1} &= \\
1331 + 1728 &= k \cdot 133,k \in \mathbb{N} \\
3059 &= k\cdot 133 
\end{align}
$$
esto vale para $k=23$  
## induccion
si asumimos que vale para $n$:

entonces cuando $n := n+1$

$$
\begin{align}
11^{n+1 +2} + 12^{2(n+1)+1} &= k\cdot 133 \\
11^{n+1+2} + 12^{2n+1 +2} &= 11^{n+2}\cdot 11 + 12^{2n+1}\cdot 12^{2}
\end{align}
$$
%% TODO: terminarlo %%


# v
probar $n! \geq 2^{n-1}$

nota: en los casos de desiguladades, es probable que sea util 
en algun momento acotar algun termino

## caso base
$$
\begin{align}
P(1) = 1! \geq 2^{1-1}
\end{align}
$$

## induccion
hipotesis
$$
P(k) = (k)! \geq 2^{k-1}
$$

$$
P(k+1) = (k+1)! = (k+1)\cdot k!
(k+1)\cdot k! \stackrel{\mathclap{\tiny\mbox{hip}}}{\geq} (k+1) 2^{k-1}
$$
como sabemos en esta situacion que $k>1$
, tambien sabemos que $k+1>2$
entonces:
$$
\begin{align}
(k+1) 2^{k-1} > 2 2^{k-1} = 2^{k} \\
(k+1)! \geq 2^{k}
\end{align}
$$