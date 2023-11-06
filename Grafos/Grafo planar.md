---
aliases:
  - grafo planar
  - planar graph
---
Un grafo planar admite una representación en el plano, con aristas sólo eventualmente intersecadas en vértices. 

Ver ejercicio 37 para esta definición.
![[Notas guia 3#^520ktv45n5q]]

Los grafos planares tienen o pueden tener [[Caras de un grafo|caras]]

Para los grafos planares, se cumple la [[fórmula de Euler]] y el [[Faceshaking lemma]]


# grafo dual de un grafo planar
Dado un grafo **G**, el grafo dual **G\*** es el grafo que tiene un vértice por cada cara del grafo planar, y una arista por cada arista del grafo planar, uniendo a 2 regiones vecinas.
Como observación, los duales de 2 representaciones del mismo grafo **no** necesariamente son isomorfas.

ej
![[Grafo planar 2023-10-31 18.52.54.excalidraw]]

# grafo planar simple
se cumple que es planar y simple, con $n\geq3$ *si y solo si* se cumple que
$$
m \leq 3(n-2)
$$
y si **no** tiene triangulos (o sea, usa cuadrados, pentagonos, etc), la formula queda
$$
m \leq 2(n-2)
$$

## demostracion
por [[Faceshaking lemma]], tenemos que
$$
2m = \sum d(f_i)
$$
como es simple, como minimo cada cara esta formada por triangulos, por lo tanto cada cara tiene grado 3 o mas. Entonces
$$
2m \geq 3f
$$
Luego, por formula de Euler
$$
n - m + f = 2 \implies f = 2 - n + m
$$
entonces
$$
\begin{align}
2m \geq 3 (2 - n + m) \\
-m \geq 3 (2 - n) \\
m \leq 3 (n - 2)
\end{align}
$$
si no tiene triangulos, cada cara tiene como minimo grado 4, y el razonamiento es similar.


