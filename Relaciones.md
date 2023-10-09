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

## Oeraciones sobre Relaciones
Sean las relaciones binarias $R$ y $S$ definidas sobre $X$ e $Y$:
### Conjunción
$$
R\ \cap S = R\cdot S= \{ (a,b) | (a,b) \in R\ \wedge (a,b) \in S \}
$$
### Disyunción
$$
R \ \cup S = R + S = \{ (a,b) | (a,b) \in R\ \vee  (a,b) \in S \}
$$

### Composición
se lee de izquierda a derecho, no como composición de funciones.
$$
R \circ S = RS = \{ (a,c) | \exists b / (a,b) \in R \ \wedge (b,c) \in S \}
$$

### Relación inversa
$$
R^{-1} = \{ (b,a) | (a,b) \in R \}
$$


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
#### clausura transitiva
Es una extensión de la relación que incluye a los pares necesarios para que una Relación que no es transitiva, sea transitiva.
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

#### propiedades de la matriz
* Si la diagonal de la matriz de relacion son todos 1s, es reflexiva.   
* Si $M_{R}= (M_{R})^{t}$ entonces la relacion es simetrica.
* Si $M_{R} \odot (M_{R})^{t} \leq I_{d}$ entonces la relacion es antisimetrica.[^odot][^leq]  
* si $(M_{R})^{2} \leq M_{R}$ entonces la relacion es transitiva.[^mat][^leq]

[^odot]: el operador $\odot$ denota el producto de matrices elemento a elemento. En este caso usando el producto 
    booleano elemento a elemento.

[^leq]: una matriz es $\leq$ a otra sii cada elemento de la primera es $\leq$ a cada elemento correspondiente de la otra. 
    O sea, $A \leq B \iff \forall a \in A, b\in B : a_{ij} \leq b_{ij}$

[^mat]: Esta multiplicacion de matrices $(M_{R})^{2} = M_{R} M_{R}$ denota la multiplicación (booleana) de matrices, que delega a la multiplicación y suma booleana
    para la multiplicación y suma de los 0s y 1s pero opera igual que la multiplicación tradicional de matrices 
    más alla de ese detalle.

* La inversa de una matriz booleana no siempre existe, pero si existe, es igual a la transpuesta de la matriz
$$
\exists A^{-1} \iff A \cdot A^{t} = I
$$

#### operaciones usando forma matricial
$$
\begin{align}
R \cdot S &= M_{R} \odot M_{S}  \\
R + S &= M_{R} \oplus M_{S}  \\
R \circ S &= RS  \\
R^{-1} &= (M_{R})^{t}
\end{align}
$$

## Relacion de equivalencia
Una relacion $R$ que es **R,S,T** (reflexiva, simetrica y transitiva) es una relación **de equivalencia**.


## Relacion de orden (parcial)
Si $R$ (relacion) es **R,A,T** (reflexiva, antisimetrica y transitiva), es una relacion **de orden** (parcial).  
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

En otras palabras, el conjunto cociente equivale a
$$
A/R = \{ [a] \ | \  a \in A \}
$$

> [!info] Teorema
> Dada una relación de equivalencia $R$ sobre un conjunto $A$, el conjunto cociente de $A$ por $R$ ($A/R$) es una *Partición* de $A$

Asimismo, de este teorema tambien se desprende que dada una partición de un conjunto, existe una relación de equivalencia sobre ese conjunto de forma que los conjuntos de la partición forman clases de equivalencias.

