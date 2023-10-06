Ver [relaciones en wikipedia](https://en.wikipedia.org/wiki/Relation_(mathematics))

Cualquier subconjunto de un producto cartesiano es una relacion. Si no existe subconjunto, no hay relacion.
$$
\begin{array} \\
C_R \subset A \times B \\
\text{R}: A \times B \to C_R \\
A \times B = \{(a,b)/a\in A, b\in B\}
\end{array}
$$
Se escribe $a\text{R}b$ para decir que existe una relación entre $a$ y $b$ (importa el orden). Se podria decir que "$a$ esta relacionado con $b$" (pero no necesariamente 
vale al revés).
Para toda relación se cumple que 2 elementos estan relacionados, o no lo están. 



> [!WARNING] Ojo
> Las funciones son relaciones pero *no todas* las relaciones son funciones (las relaciones pueden tener multiples imágenes para un mismo elemento del dominio)

## Tipos de Relaciones
### Reflexiva
Relaciones donde cada elemento del dominio, todos esta relacionado con sí mismo
$$
\forall a \in A: a\text{R}a
$$
### Simetrica
Relaciones donde para cada par de elementos $(a,b)$ que estan relacionados, tambien estan relacionados $(b,a)$
$$
\forall a,b \in A: a\text{R}b \implies b\text{R}a
$$
### Antisimetrica
Relaciones donde dos elementos estan relacionados simétricamente solamente si son el mismo elemento.
$$
\forall a,b \in A: a\text{R}b,b\text{R}a \implies a=b
$$
### Transitiva

$$
\forall a,b,c \in A: a\text{R}b, b\text{R}c \implies a\text{R}c
$$
## Representaciones
Ej:
$$
\begin{array} \\
A = \{1,2,3,4\}  \\
\text{R} = \{(1,1),(2,2),(3,3),(4,4),(1,2),(2,1)\}
\end{array}
$$
## grafica
digrafo de la relación
El diagrama muestra la relación entre elementos. 

![[Algebra Proposicional 2023-09-17 19.56.36.excalidraw]]
otro:
Dada la relacion sobre $R^{2}$: $\mathbf{R}: \mathbb{R}^{2} \to \mathbb{R}^{2}.\ \mathbf{R} = \{ x,y \in \mathbb{R} | x^{2} + y^{2} = 4 \}$
Se puede representar como

![[circulo.excalidraw]]

### Matricial

|     | **1**   | **2**   | **3**   | **4**   |
| --- | --- | --- | --- | --- |
| **1**   | 1   | 1   | 0   | 0   |
| **2**   | 1   | 1   | 0   | 0   |
| **3**   | 0   | 0   | 1   | 0   |
| **4**   | 0   | 0   | 0   | 1   |

Si la diagonal de la matriz de relacion son todos 1s, es reflexiva.   
Si $M_{R}= M_{R}^{t}$ entonces la relacion es simetrica.
Si $M_{R}M_{R}^{t} \leq I_{d}$ entonces la relacion es antisimetrica.  
si $M_{R}M_{R} \leq M_{R}$ entonces la relacion es transitiva.




## Relacion de equivalencia
Una relacion $R$ que es **R,S,T** (reflexiva, simetrica y transitiva) es una relación **de equivalencia**.


## Relacion de orden
Si $R$ (relacion) es **R,A,T** (reflexiva, antisimetrica y transitiva), es una relacion **de orden**.  
Una relacion donde podemos decir que $x$ precede a $y$ (o es igual?)
$$
x \leq y
$$
En un algebra de boole, esto lo podemos escribir de varias maneras equivalentes:
$$
\begin{align}
x \leq y &\equiv  \\
&\equiv xy = x  \\
&\equiv x+y = y  \\
&\equiv x\bar{y} = 0 \\
&\equiv \bar{x}+y=1
\end{align}
$$
En un algebra de conjuntos, esto tambien se puede escribir como $x \subseteq y$ 
### condiciones

si $x \leq x$ entonces la relacion es **reflexiva** 
si $(x \leq y, y \leq x) \implies (x=y)$ entonces la relacion es **antisimetrica**  
si $(x \leq y, y \leq x) \implies (x \leq z)$ entonces la relacion es **transitiva**


> [!NOTE] Nota
> La unica relacion de orden y equivalencia es la identidad.

## Clases de equivalencias

La relacion debe ser RST. 

* Clase del elemento "$a$" $= Cl(a) = [a] = \{ x \in \text{Conjunto } | \ x\text{R}a \}$
* las clases nunca son vacías porque $a \subset [a]$
* $[a] \cap [b] = \varnothing$ si **no** son elementos de la misma clase.
* $[a] = [b]$ si son elementos de la misma clase.

### Conjunto cociente
dado $A$ el conjunto dado (universo) y $R$ una relacion de equivalencia,  $A/R = \{ [a], [b], [c] \}$ es el "conjunto cociente" de A,R. 
El conjunto cociente esta formado por todas las clases distintas de $A$ dado la relación $R$. 