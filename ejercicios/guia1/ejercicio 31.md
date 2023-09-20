
$$
(B,+,*,',0,1)
$$
$$
(D_{30},\text{mcm},\text{mcd},\bar{\ },1,30) = (D_{30},+,*,\bar{\ },0,1)
$$
donde tenemos que $D_{30}$ son los divisores de $30$

$$
\forall x,y \in D_{30}: \begin{array} \\
x+y = \text{mcm}(x,y) \\
x\cdot y = \text{mcd}(x,y)
\end{array}
$$
### mcm y mcd
dados 2 números naturales, el *mcm* y el *mcd* se pueden calcular de la siguiente manera:  
* para el mcm: escribir la factorización en números primos de ambos números y tomar todos los factores de ambos que presentan una potencia mayor a 0 
ej: entre 15 y 24, $6 = 2^{0}\cdot3^{1}\cdot5^{1}\cdot 7^{0}\dots$ y $24 = 2^{3}\cdot 3^{1}\cdot 5^{0}\dots$  
entonces el $\text{mcm}(15,24) = 2^{3}\cdot 3^{1} \cdot 5^{1} = 120$ 
* para el mcd: escribir la factorización en números primos de ambos números y solo los factores que en ambos presentan exponentes mayores a 0. Escribir los de menor exponente.
ej: entre 36 y 24,  $36 = 2^{2}\cdot3^{2}\cdot5^{0}\cdot 7^{0}\dots$ y $24 = 2^{3}\cdot 3^{1}\cdot 5^{0}\dots$   
entonces el $\text{mcd}(36,24) = 2^{2}\cdot 3^{1}\cdot 5^{0}\dots = 12$

## vemos si es un algebra
### es complementada?
Ejemplo
$$
\text{mcm}(2,\bar{2}) = 30
$$
$$
\text{mcd}(2,\bar{2})=1
$$
buscamos que:
$$
\forall x \in D_{30}: \begin{array} \\
x\cdot \bar{x}=e_{+} \\
x+\bar{x}=e_{\cdot }
\end{array}
$$
$$\begin{array} \\
\text{mcm}(2,x) = 30 = 2^{1}3^{1}5^{1}  & \text{mcd}(2,x) = 1 = 2^{0}3^{0}5^{0} \\
\text{mcm}(2^{1}3^{0}5^{0},2^{a}3^{b}5^{c}) = 2^{1}3^{1}5^{1}  & \text{mcd}(2^{1}3^{0}5^{0},2^{a}3^{b}5^{c}) = 2^{0}3^{0}5^{0} \\
b,c = 1; a \leq 1 & a = 0; b,c \leq 1 
\end{array}
$$
entonces con mcm
$$
\begin{array}
\text{mcm}(2,2') =  \  3^{1}5^{1}=15 \ \vee \text{mcm}(2,2') = 2\cdot 3 \cdot 5 = 30
\end{array}
$$

y con mcd
$$
\text{mcd}(2,2') = 2^{0}3^{0}5^{0} = 1 \ \vee \ \text{mcd}(2,2') = 2^{0}3^{1}5^{1} = 15  
$$
la solución es entonces $a=0, b=1, c=1 \implies 2^{0}3^{1}5^{1}=15$

En general, si la sextupla tiene estructura de algebra de bool, los complementos se pueden calcular como $\bar{x} = \frac{\text{max\_elem}}{x}$. El elemento maximo se corresponderá con el 1 y el elemento minimo se correspondera con el 0.

## cuando hay estructura de algebra de bool?
si los factores primos del numero aparecen todos sin repetir, entonces habra algebra de bool. La sextupla va a tener que se cumplen los axiomas y que cada elemento tiene complemento unico.

## atomos
definicion de atomo:
$$
\forall a \neq 0_B \text{ es atomo si } x \cdot a=x \implies x=a \ \vee x=0_B
$$
## subalgebras
$$
es
$$
$H_3$ vale si $x,y \in H \implies x+y = \text{sup} \in H; x\cdot y = \text{inf} \in H$

### nota
no hay algebra de bool de 6 elementos. solo hay algebras o subalgebras de cardinalidad $2^{n}$ donde $n$ es el numero de atomos del algebra.

## Relacion (en un algebra de boole de divisores)
dos elementos $a,b \in D_{m}$ estan [[Algebra Proposicional#Relaciones|relacionados]] $a\text{R}b \iff a|b$ donde $a|b$ significa "a es divisor de b" o quivalentemente que "b es múltiplo de a" 