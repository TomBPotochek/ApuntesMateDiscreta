---
aliases:
  - line graph
---
El grafo arista es el grafo que se obtiene al tomar las aristas de G como vértices de L(G) y uniendo 2 de estos vértices siempre que sus correspondientes aristas en G tengan un vértice en común.

Ver ejercicio 41.


![[grafo arista 2023-10-31 19.18.59.excalidraw]]

![[grafo arista 2023-10-31 19.22.03.excalidraw]]
Si $u \in V(L_G)$ correspondiente a la arista $x y \in E(G)$
¿Cual es el grado de $u$ en funcion de los grados de $x$ e $y$?
Determinar el orden y el tamaño de $L(Kn)$

->
$$
d(u) = d(x) + d(y) - 2
$$


$$
|V(L_{Kn})| = |E_{Kn}| = \frac{n(n-1)}{2}
$$
$$
|E_{L_{Kn}}| = \frac{n(n-1)(n-2)}{2}
$$

# casos particulares
grafo arista de un camino simple ($P_n$) con $n> 2$ es otro camino simple de grado menor

$$
L(P_n) = P_{n-1}
$$

grafo arista de un Cycle ($C_n$) con $n> 2$ es otro cycle.

$$
L(C_n) = C_n
$$






