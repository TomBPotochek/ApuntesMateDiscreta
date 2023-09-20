## definición 
$$
\text{dado } (B,+,\cdot \ ,', 0,1)
$$
se deben cumplir (ejercicio 28): ![[Notas guía 1#^td14lx4k08]]

# Identidades

## axiomas
estas definen al algebra de boole. Si no se cumplen, no es algebra de Boole

### conmutatividad

$$
\forall a,b \in B: \begin{array} \\

a + b = b +a  \\
a \cdot b = b \cdot a
\end{array} \\
$$

### distributividad
$$
\forall a,b,c \in B: \begin{array} \\

a + bc=(a+b)(a+c) \\
a(b+c)=ab+ac
\end{array} \\
$$
### neutros
$$

\begin{array} \\

a +0 = a \\
a\cdot 1=a
\end{array} \\
$$
### complementos
$$
a \in B, \exists a' \in B: \begin{array}
 \\
a+ a'=1 \\
a\cdot a' =0
\end{array} \\
$$

## Corolarios/Propiedades
### idempotencia
$$
\begin{array} \\
x+x =x \\
x\cdot x = x
\end{array}
$$

### acotacion
$$ 
\begin{array} \\
1+x=1 \\
0\cdot x=0
\end{array}
$$

### absorcion
$$
\begin{array} \\
x+xy =x \\
x(x+y)=x
\end{array}
$$
#### demostracion
$$
x +xy = 1\cdot x +xy = x(1+y)=x\cdot 1=x
$$
### leyes de DeMorgan
$$
\begin{array}  \\
(x+y )' = x'\cdot y' \\
(x\cdot y)'=x'+y'
\end{array}
$$


> [!NOTE]
> Para cada algebra de Boole, se puede asociar una Relacion de orden.  

# Partes de un algebra de Boole
$P_{A}$ es el conjunto de todos los subconjuntos de A. "Partes de A"

Ej:
dado $A = \{a,b,c\}$, entonces $P_{A} = \{\varnothing, \{a\}, \{ b \}, \{ c \}, \{ a,b \}, \{ a,c \}, \{ b,c \}, \{ a,b,c \}\}$
además, $(P_{A}, \cup, \cap, \bar{\ }, \varnothing, A)$ forma un álgebra de Boole. Tiene conjunto de átomos: $\{ \{ a \}, \{ b \}, \{ c \} \}$
![[Algebra de Bool 2023-09-17 23.53.31.excalidraw]]

# atomos
un elemento $a$ de un algebra de Boole es un átomo si[^1]:  
$$
\begin{array} \\
a \neq 0  \\
(x \cdot a = x \implies x = a) \ \vee (x = 0)
\end{array}
$$
[^1]: a esta definicion le falta algo. No se qué esta diciendo.

# subalgebras de Boole
$H$ es un subalgebra de $B$ si $H \subset B$ y $H$ es álgebra de Boole. 


# [[Isomorfismos de algebra de Boole]]

----------
# ejercicios tipo
[[ejercicio 31]]: algebras de divisores de un numero, atomos, etc.


