# grafo 12
![[Ejercicio 15 2023-10-30 18.18.27.excalidraw]]

orden = $|V| = 6$
tamaño = $|E| = 7$
grados de los vertices

| vi  | d(vi) |
| --- | ----- |
| v1  | 2     |
| v2  | 2     |
| v3  | 4     |
| v4  | 3     |
| v5  | 2     |
| v6  | 1      |

degree sequence = $d(v) = (1,2,2,2,3,4)$

promedio grados = $\frac{\sum p(v)}{n} = \frac{14}{6} = \frac{7}{3}$

grado minimo = $\delta(G_{12})=1$

grado maximo = $\Delta(G_{12}) = 4$

distancias minimas:

|     | v1  | v2  | v3  | v4  | v5  | v6  |
| --- | --- | --- | --- | --- | --- | --- |
| v1  | -   | 1   | 1   | 2   | 2   | 3   |
| v2  | 1   | -   | 1   | 2   | 2   | 3   |
| v3  | 1   | 1   | -   | 1   | 1   | 2   |
| v4  | 2   | 2   | 1   | -   | 1   | 1   |
| v5  | 2   | 2   | 1   | 1   | -   | 2   |
| v6  | 3   | 3   | 2   | 1   | 2   | -   | 


excentricidad

| vi  | ex(vi) |
| --- | ------ |
| v1  | 3      |
| v2  | 3      |
| v3  | 2      |
| v4  | 2      |
| v5  | 2      |
| v6  | 3       |

radio = $r(G_{12})=2$
diametro = $\phi(G_{12}) = 3$
centro = $C(G_{12})=\{ v3;v4;v5 \}$
Periferia = $P(G_{12})=\{ v1;v2;v6 \}$


# G1

![[Ejercicio 15 2023-10-30 18.35.57.excalidraw]]

orden = n = 3

aristas = m = 1

degree sequence = $(0,1,1)$

promedio = $\frac{2}{3}$

distancias minimas

|     | v1       | v2       | v3       |
| --- | -------- | -------- | -------- |
| v1  | -        | 1        | $\infty$ |
| v2  | 1        | -        | $\infty$ |
| v3  | $\infty$ | $\infty$ | -        | 

excentricidad = $\infty$
radio = $\infty$
centro = $\{ v1;v2;v3 \}$
