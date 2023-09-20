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

> [!WARNING]
> Las funciones son relaciones pero *no todas* las relaciones son funciones (las relaciones pueden tener multiples imágenes para un mismo elemento del dominio

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
digrafo de la relación
El diagrama muestra la relación entre elementos. 

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
x \leq y \mbox{ ``x precede a y'' } &\equiv xy = x \equiv \\
\equiv x+y = y \equiv x\bar{y} = 0 &\equiv \bar{x}+y=1
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