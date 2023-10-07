Densidad $\delta(p)$ de una proposición $p$  es la cantidad de filas de la tabla de verdad donde la proposición es verdadera dividida el total de filas (de la tabla de verdad). Una especie de medida del tamaño del "conjunto de positivad" de la proposición.  

También aplican las [[Relaciones|relaciones]] entre conjuntos que forman un álgebra (en este caso proposicional).
# Básico
## Propiedades

Ídem algebra de Boole, pero con $+ \equiv \cap$ , $\cdot \equiv \cup$ , $1 \equiv \text{I}$ , $0 \equiv \varnothing$  :
![[Algebra de Bool#Identidades]]

Ver también: [[Relaciones]]

## Formas Normales

se puede escribir una funcion proposicional en su forma normal. Es una suma o producto de terminos completos. Un termino completo es un termino donde aparecen todas las variables de la función. Se pueden numerar los terminos en base a la cantidad posible de terminos. O sea, numeros de $0$ hasta $2^{n}-1$ donde $n$ es el numero de variables de la funcion.

### Forma normal disyuntiva

es la suma de minterminos. Un mintermino es un producto de todas las variables de la función.
ej de función proposicional. 
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






