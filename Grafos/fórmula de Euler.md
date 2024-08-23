
$$
n - m + f = 2
$$
O sea, el número de vertices ($n$) menos el número de aristas ($m$) más el número de caras ($f$) es siempre igual a 2.
 demostracion

Tenemos que cualquier grafo conexo se construye a partir de un [[árbol generador]].

Entonces si $n = 1$, el grafo es un punto y hay 1 cara. Entonces la fórmula de Euler vale para $n=1$.

Si tenemos un árbol generador, por ser árbol se tiene que  
$n=n$  
$m= n-1$
$f = 1$
Por lo tanto la fórmula vale
$$n-n+1+1=2$$
Luego, por cada arista que agrego sin agregar un vertice (o sea, se crea un ciclo), se agrega una cara ademas de una arista.  
Como por cada arista, se resta 1 y por cada cara se suma 1, la fórmula sigue valiendo al agregar esas aristas.
