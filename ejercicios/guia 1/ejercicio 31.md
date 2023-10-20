#ejercicio/completo 
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
* para el mcm: escribir la factorización en números primos de ambos números y tomar todos los factores de ambos donde alguno presenta una potencia mayor a 0 (tomando los de menor exponente)
ej: entre 15 y 24, $6 = 2^{0}\cdot3^{1}\cdot5^{1}\cdot 7^{0}\dots$ y $24 = 2^{3}\cdot 3^{1}\cdot 5^{0}\dots$  
entonces el $\text{mcm}(15,24) = 2^{3}\cdot 3^{1} \cdot 5^{1} = 120$ 
* para el mcd: escribir la factorización en números primos de ambos números y solo los factores que en ambos presentan exponentes mayores a 0 (Tomando los de menor exponente).
ej: entre 36 y 24,  $36 = 2^{2}\cdot3^{2}\cdot5^{0}\cdot 7^{0}\dots$ y $24 = 2^{3}\cdot 3^{1}\cdot 5^{0}\dots$   
entonces el $\text{mcd}(36,24) = 2^{2}\cdot 3^{1}\cdot 5^{0}\dots = 12$

#### en algebras de boole
en otras palabras, si estamos trabajando con los divisores de un numero $N$ y forman un algebra de boole, podemos calcular el mcm y mcd de 2 numeros $a,b$ del algebra de divisores de $N$ como:
$$
\begin{align}
N &= n_{1} n_{2} \dots n_{k}  & \mbox{ : factores primos de } N \\
a &= n_{1}^{a_{1}} n_{2}^{a_{2}}\dots n_{k}^{a_{k}}  & \mbox{ : } a_{i} \in  \{ 0,1 \} \\
b &= n_{1}^{b_{1}} n_{2}^{b_{2}}\dots n_{k}^{b_{k}}  & \mbox{ : } b_{i} \in  \{ 0,1 \} \\
\\
\text{mcm}(a,b) &= n_{1}^{(a_{1}\ +_{\tiny B} \ b_{1})} n_{2}^{(a_{2}\ +_{\tiny B} \ b_{2})}\dots n_{k}^{(a_{k}\ +_{\tiny B} \ b_{k})}  & : +_{\tiny B} \equiv + \mbox{ de boole } \\
\text{mcd}(a,b) &= n_{1}^{(a_{1}\ \cdot_{\tiny B} \ b_{1})} n_{2}^{(a_{2}\ \cdot_{\tiny B} \ b_{2})}\dots n_{k}^{(a_{k}\ \cdot_{\tiny B} \ b_{k})}  & : \cdot_{\tiny B} \equiv \cdot \mbox{ de boole } \\
 
\end{align}
$$

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
x\cdot \bar{x}=e_{+}  \mbox{ \small (neutro suma } \equiv 0)\\
x+\bar{x}=e_{\cdot } \mbox{\small  (neutro producto } \equiv 1)
\end{array}
$$
$$\begin{array} \\
\text{mcm}(2,x) = 30 = 2^{1}3^{1}5^{1}  & \text{mcd}(2,x) = 1 = 2^{0}3^{0}5^{0} \\
\text{mcm}(2^{1}3^{0}5^{0},2^{a}3^{b}5^{c}) = 2^{1}3^{1}5^{1}  & \text{mcd}(2^{1}3^{0}5^{0},2^{a}3^{b}5^{c}) = 2^{0}3^{0}5^{0} \\
\left\{ \begin{array} \\
1 +_{\tiny B} a = 1 \\
0 +_{\tiny B} b = 1 \\
0 +_{\tiny B} c = 1
\end{array} \right.  & \left\{ \begin{array} \\
1 \cdot_{\tiny B} a = 0 \\
0 \cdot_{\tiny B} b = 0 \\
0 \cdot_{\tiny B} c = 0
\end{array} \right. \\
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


> [!info] Teorema
> si los factores primos del numero que define al conjunto de divisores aparecen todos sin repetir, entonces habrá algebra de boole. La sextupla va a tener que se cumplen los axiomas y que cada elemento tiene complemento unico.

## atomos
definicion de atomo:
$$
\forall a \neq 0_B, a \text{ es atomo si } x \cdot_{\tiny B} a=x \implies x=a \ \vee x=0_B
$$
Esto traducido a lenguaje natural significa que de todos los elementos del algebra de boole que *no* son $0_{B}$, los que son átomos del algebra son los que cumplen la proposición:

> *"si $x \cdot a$ es $x$ (o equivalentemente $x \leq a)$, entonces $x$ es $a$ o $x$ es $0_{B}$"*.  

O sea, son los números que son los "más chicos" sin ser nulos. Si existe otro numero menor o igual a (alguno de) ellos, ese otro número es 0 o es sí mismo (y no hay otra opción). 

## subalgebras

$H_{sub} \subset H$ es subalgebra de $H$ si: 

$$
\begin{align}
x,y \in H_{sub} \implies x+y \in H_{sub}; x\cdot y \in H_{sub} \\
x \in H_{sub} \implies \overline{x} \in H_{sub} \\
0_{B},1_{B} \in H \implies 0_{B},1_{B} \in H_{sub}
\end{align}
$$
En otras palabras, debe cumplir con los axiomas de un algebra de boole "sin salirse" del subconjunto, y además el $0$ y $1$ del subalgebra deben ser los mismos $0$ y $1$ del algebra original. 

### nota
no hay algebra de bool de 6 elementos. solo hay algebras o subalgebras de cardinalidad $2^{n}$ donde $n$ es el numero de átomos del algebra.

## Relacion (en un algebra de boole de divisores)
dos elementos $a,b \in D_{m}$ estan [[Algebra Proposicional#Relaciones|relacionados]] $a\text{R}b \iff a|b$ donde $a|b$ significa "a es divisor de b" o quivalentemente que "b es múltiplo de a" 