
![[Ejercicio 8 2023-10-24 18.17.34.excalidraw]]


$$
A(G) = \begin{pmatrix}
0 & 0 & 1 & 0 & 1 & 0 \\
0 & 0 & 0 & 1 & 0 & 1 \\
1 & 0 & 0 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 & 0 & 1 \\
1 & 0 & 1 & 0 & 0 & 0 \\
0 & 1 & 0 & 1 & 0 & 0
\end{pmatrix}
$$
vemos que sumando los elementos por fila, obtenemos el grado de cada vertice $d(v_i)$


probamos que los elementos de $A^{q}(G)$ son la cantidad de caminos de longitud $q$ que conectan el vertice $i$ con el vertice $j$
# demostracion

## paso base
$$
A(G)=(a_{ij})
$$
caminos de longitid 1 que conectan los vertices $v_i$ con $v_j$

## induccion
supongo verdadero que $A^{k}=(s_{ij})$ son los caminos de longitud k que entre $v_i$ y $v_j$
y lo mismo para $A^{k+1} = (t_{ij})$

entonces:

$$
\begin{align}
A^{k+1} = A^{k}A \\
t_{ij} = \sum_{i=1}^{l} s_{ij}a_{ij}
\end{align}
$$
donde vemos que estamos concatenando.caminos de longitud $k$ (los $t_{ij}$) con caminos de longitud 1 (los $a_{ij}$). Por lo tanto, el resultado son caminos de longitud k+1




