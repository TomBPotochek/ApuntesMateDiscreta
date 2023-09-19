Densidad $\delta(p)$ de una proposicion $p$  es la cantidad de filas de la tabla de verdad donde la proposicion es verdadera dividida el total de filas (de la tabla de verdad).

# Basico
## Propiedades

Ídem algebra de Boole:
![[Algebra de Bool#Identidades]]

## Formas Normales

se puede escribir una funcion proposicional en su forma normal. Es una suma o producto de terminos completos. Un termino completo es un termino donde aparecen todas las variables de la función. Se pueden numerar los terminos en base a la cantidad posible de terminos. O sea, numeros de $0$ hasta $2^{n}-1$ donde $n$ es el numero de variables de la funcion.

### Forma normal disyuntiva

es la suma de minterminos. Un mintermino es un producto de todas las variables de la funcion.
ej de funcion proposicional. 
$$
f(p,q,r) = p\bar{q}r + p\bar{r} + pq
$$


$$
\begin{array} \\
f(p,q,r) = p\bar{q}r + pq\bar{r} + p\bar{q}\bar{r} + pqr + pq\bar{r}  \\
f(p,q,r) = \underbrace{ p\bar{q}r }_{ 101 } + \underbrace{ pq\bar{r} }_{ 110 } + \underbrace{ p\bar{q}\bar{r} }_{ 100 } + \underbrace{ pqr }_{ 111 } + \underbrace{ pq\bar{r} }_{ 110 } \\
f(p,q,r) = \sum_{m} (4,5,6,7) \\
\end{array}
$$

### Forma Normal Conjuntiva
es el producto de maxterminos. Un maxtermino es una suma donde aparecen todas las variables de la funcion.
ej de funcion proposicional. 
$$
f(p,q,r) = (p+\bar{q}) \cdot (\bar{p}+r)
$$



$$
\begin{array}
f(p,q,r) = (p+\bar{q}+r) \cdot (p+\bar{q}+\bar{r}) \cdot (\bar{p}+q+r) \cdot (\bar{p}+\bar{q}+r) \\
f(p,q,r) = \underbrace{ (p+\bar{q}+r) }_{ 010 } \cdot \underbrace{ (p+\bar{q}+\bar{r}) }_{ 011 } \cdot \underbrace{ (\bar{p}+q+r) }_{ 100 } \cdot \underbrace{ (\bar{p}+\bar{q}+r) }_{ 110 }  \\
f(p,q,r) = \prod_{M} (2,3,4,6)
\end{array}
$$
## Operaciones
### Resta
$$
p - q = p\cdot \bar{q}
$$
### Suma Directa (O exclusivo)
$$
p \oplus q = p\cdot \bar{q}+\bar{p}\cdot q
$$
# Relaciones
Cualquier subconjunto de un producto cartesiano es una relacion. Si no existe subconjunto, no hay relacion.
$$
\begin{array}
\text{R}: A \to A  \\
A \times B = \{(a,b)/a\in A, b\in B\}
\end{array}
$$
cardinal de un conjunto es la cantidad de elementos en el conjunto.
$$
|A| = \mbox{cantidad de elementos de } A
$$
$$
|A \times B| = |A| \cdot |B|
$$

Las funciones son relaciones pero no todas las relaciones son funciones (las relaciones pueden tener multiples imagenes para un mismo elemento del dominio

## Propiedades
### Reflexiva
$$
\forall a \in A: a\text{R}a
$$
### Simetrica
$$
\forall a,b \in A: a\text{R}b \to b\text{R}a
$$
### Antisimetrica
$$
\forall a,b \in A: a\text{R}b,b\text{R}a \to a=b
$$
### Transitiva
$$
\forall a,b,c \in A: a\text{R}b, b\text{R}c \to a\text{R}c
$$
## Representaciones
Ej:
$$
\begin{array}
A = \{1,2,3,4\}  \\
\text{R} = \{(1,1),(2,2),(3,3),(4,4),(1,2),(2,1)\}
\end{array}
$$
## grafica
digrafo de la realacion
El diagrama muestra la relacion entre elementos. 

![[Algebra Proposicional 2023-09-17 19.56.36.excalidraw]]

### Matricial
$$
\text{M}_{\text{R}} = \begin{pmatrix}
1 & 1 & 0 & 0 \\
1 & 1 & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1 \\
\end{pmatrix}
$$
Si la diagonal de la matriz de relacion son todos 1s, es reflexiva.   
Si $M_{R}= M_{R}^{t}$ entonces la relacion es simetrica.
Si $M_{R}M_{R}^{t} \leq I_{d}$ entonces la relacion es antisimetrica.  
si $M_{R}M_{R} \leq M_{R}$ entonces la relacion es transitiva.

Si $R$ (relacion) es **R,A,T** (reflexiva, antisimetrica y transitiva), es una relacion **de orden**.  
Si $R$ es **R,S,T** entonces es una relacion **de equivalencia**.

La unica relacion de orden y equivalencia es la identidad.

## Relacion de orden
$$
\begin{split}
x \leq y \mbox{ "x precede a y" } &\equiv xy = x \equiv \\
\equiv x+y = y &\equiv x\bar{y} = 0 \equiv \bar{x}+y=1
\end{split}
$$
### condiciones

si $x \leq x$ entonces la relacion es **reflexiva** 
si $(x \leq y, y \leq x) \implies (x=y)$ entonces la relacion es **antisimetrica**  
si $(x \leq y, y \leq x) \implies (x \leq z)$ entonces la relacion es **transitiva**
## Clases de equivalencias
La relacion debe ser RST. 

* Clase del elemento "$a$" $= Cl(a) = [a] = \{ x \in \text{Conj } / x\text{R}a \}$
* las clases nunca son vacias porque $a \subset [a]$
* $[a] \cap [b] = \varnothing$ si **no** son elementos de la misma clase.
* $[a] = [b]$ si son elementos de la misma clase.

dado $A$ el conjunto dado (universo) y $R$ una relacion de equivalencia,  $A/R = \{ [a], [b], [c] \}$ es el "conjunto cociente" de A,R. El conjunto cociente formado por todas las clases distintas de $A$ dado $R$. 




