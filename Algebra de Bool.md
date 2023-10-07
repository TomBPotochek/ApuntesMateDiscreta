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
a \in B, \exists  \overline{ a} \in B: \begin{array}
 \\
a+ \overline{ a}=1 \\
a\cdot \overline{ a} =0
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
\overline{(x+y )} = \overline{x}\cdot \overline{y} \\
\overline{(x\cdot y)}=\overline{x} + \overline{y}
\end{array}
$$


> [!NOTE] Nota
> Para cada algebra de Boole, se puede asociar una [[Relaciones|relación]] de orden.  
> Dados $x$ e $y$ en un el algebra de Boole, $x \leq y \iff xy = x$

# Partes de un algebra de Boole
$P_{A}$ es el conjunto de todos los subconjuntos de A. "Partes de A"[^pot]

[^pot]: ¿no se dice "conjunto de potencia" (power set) en lugar de "partes de .."?

Ej:
dado $A = \{a,b,c\}$, entonces $P_{A} = \left\{\varnothing, \{a\}, \{ b \}, \{ c \}, \{ a,b \}, \{ a,c \}, \{ b,c \}, \{ a,b,c \}\right\}$
además, $(P_{A}, \cup, \cap, \bar{\ }, \varnothing, A)$ forma un álgebra de Boole. Tiene conjunto de átomos: $\{ \{ a \}, \{ b \}, \{ c \} \}$

Representados como diagramas de *Hasse*[^hasse]:
![[Algebra de Bool 2023-09-17 23.53.31.excalidraw]]

[^hasse]: son una representacion gráfica de un algebra de Boole donde las conexiones en el diagrama representan
    que esos 2 elementos estan relacionados entre sí con una relación de órden.

(otro ejemplo, en latex)
```tikz
\begin{document}
\begin{tikzpicture}
  \node (max) at (0,4) {$(1,1,1)$};
  \node (a) at (-2,2) {$(0,1,1)$};
  \node (b) at (0,2) {$(1,0,1)$};
  \node (c) at (2,2) {$(1,1,0)$};
  \node (d) at (-2,0) {$(0,0,1)$};
  \node (e) at (0,0) {$(0,1,0)$};
  \node (f) at (2,0) {$(1,0,0)$};
  \node (min) at (0,-2) {$(0,0,0)$};
  \draw (min) -- (d) -- (a) -- (max) -- (b) -- (f)
  (e) -- (min) -- (f) -- (c) -- (max)
  (d) -- (b);
  \draw[preaction={draw=white, -,line width=6pt}] (a) -- (e) -- (c);
\end{tikzpicture}
\end{document}
```


```tikz
\usepackage{amssymb}
\begin{document}
\begin{tikzpicture}
  \node (max) at (0,0) {$abc$};
  \node [below left of=max] (ac) {$ac$};
  \node [below right of=max] (bc) {$bc$};
  \node [below of=ac] (a) {$a$};
  \node [below of=bc] (b) {$b$};
  \node [below of=max] (ab) {$ab$};
  \node [below of=ab] (c) {$c$};
  \node [below of=c] (min) {$\varnothing$};

  \draw (max) -- (ac) -- (a) -- (min) -- (b) -- (bc) -- (max);
  \draw (max) -- (ab);
  \draw (a) -- (ab) -- (b);
  \draw (c) -- (min);
  \draw[preaction={draw=white, -,line width=6pt}] (ac) -- (c) -- (bc);
%  \draw[preaction={draw=white, -,line width=6pt}] (a) -- (e) -- (c);
\end{tikzpicture}
\end{document}
```
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
Establecen una relacion de equivalencia entre dos algebras de Boole

----------
# ejercicios tipo
[[ejercicio 31]]: algebras de divisores de un numero, atomos, etc.


