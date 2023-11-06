---
aliases:
  - grafo
  - graph
  - graphs
---
# definición
$$
G=(V,E, \Psi_G)
$$
donde
$$
\Psi_G: E_{(G)}\to \{ u,v | uv \in V \}
$$
es la *función de incidencia* que asigna a cada arista un conjunto de 2 (o 1) vértices del grafo.
![[Grafos 2023-10-17 18.35.26.excalidraw]]
## aristas
las aristas representan la coneccion entre 2 vertices
* si una arista *incide* en 1 solo vertice, es un **bucle o lazo**
* si una arista *incide* en 2, es una arista (comun)
* si para un par de vertices inciden muchas aristas, el grafo **no es simple** y esas aristas son *paralelas*.

Si no es un digrafo (grafo con aristas con direccion), entonces se suele representar cada arista como un conjunto de vertices. En los digrafos, son pares ordenados.

### grado de una arista
??

## Orden de un grafo
es la cardinalidad del conjunto de vertices
$$
n(G) = |V|
$$
## tamaño de un grafo
es la cardinalidad del conjunto de aristas
$$
m(G) = |E|
$$
# vértices
## grado de un vertice
numero de aristas que inciden en el vertice
en el caso de lazo o bucle, se cuenta doble.

$$
d(v) = \mbox{ num de aristas que inciden en } v
$$
si todos tienen el mismo grado, es un *grafo regular*

![[Hamshaking lemma]]
### cantidad vertices grado impar
la cantidad de vertices de grado impar es **par**


### grafo completo
Si para un grafo de orden $n$, se tiene que todos los vértices tienen grado $n-1$, el grafo es un **grafo completo**.

## degree sequence
sucesion no decreciente de los grados de todos los vertices de un grafo $G$.  
Se escribe $d(G)$

## otras definiciones

### grado minimo
$\delta(G) =$ minimo $d(v)$ = $\min\{ d(v) : v\in V_{(G)} \}$
### grado maximo
$\Delta(G) =$ maximo $d(v)$ = $\max\{ d(v):v\in V_{(G)} \}$
### excentricidad
$e(v) = \max_u d(v,u)$
### diametro
$\phi_{(G)} = \min_u \max_v d(u,v)$
### radio
$\Omega(G)= \min_u \max_v d(u,v)$ 
### centro
$C(G) =$ conjunto de vertices de excentricidad minima
### periferia
$P(G)=$ conjunto de vertices de excentricidad maxima

## matriz de adyacenciaa
es la matriz cuadrada con vertices en las filas y vertices en las columnas. Indica con un 1 si el vertice de la fila $i$ inincide sobre el vertice de la columna $j$, sino 0

## matriz de indicencias
es la matriz (no cuadrada) con vertices en las filas y *aristas* en las columnas. Indica si el vertice de la fila $i$ incide sobre la arista de la columna $j$

Si una arista es un bucle, se indica con un aristerisco en la matriz \*

otras

![[Notas guia 3#^fgcbh9kdybb]] ^394351


Bipartito:
Ejercicio 21




