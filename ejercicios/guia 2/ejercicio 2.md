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
