# Problema de vendedor ambulante

## 1. Introducción

El problema del vendedor viajero o también conocido como TSP (por siglas en ingles). Consiste en encontrar, en un grupo finito de ciudades y sus respectivos costos de viajes entre ciudad y ciudad, el camino más económico de recorrer todas las ciudades. Dicho recorrido tiene ciertas condiciones, se debe iniciar el recorrido en una ciudad, pasar por todas las ciudades, solamente una vez, y terminar en la ciudad en la que se comenzó. Esto debe ser logrado teniendo en consideración que el resultado debe ser el recorrido que tenga el menor costo.

A lo largo de la historia, se han diversas soluciones a este problema. Por ejemplo:

> Karl Menger (Shortest Hamiltonian Path, 1930), J.B. Robinson (Hamiltonian game, 1949), G. Dantzig, R. Fulkerson, y S. Johnson (Solution of a large-scale traveling-salesman problem, 1954), M. Held and R.M. Karp (Introducción de heurísticas basadas en programación dinámica, 1962), entre otros. (Espinoza, 2006)

La principal motivación para el desarrollo del proyecto, consiste en las diferentes aplicaciones del TSP. Algunas de ellas son estudio en la secuencia de genes, diseño de chips, enrutamiento de vehículos, entre otras.

## 2. Objetivo

El presente trabajo tiene como objetivo principal encontrar una solución parcial al problema de TSP usando dos *datasets* distintas del Ministerio de Educación del Perú. Uno de ellos contiene la posición geográfica (latitud y longitud) de cada centro poblado del Perú. Mientras que, el otro contiene la posición geográfica (latitud y longitud) de cada centro educativo del país.

## 3.	Marco Teórico

El algoritmo de Prim es un algoritmo perteneciente a la teoría de los grafos. El cual comienza con un árbol de expansión vacío. La idea es mantener dos conjuntos de vértices. El primer conjunto contiene los vértices ya incluidos en el MST (minimum spanning tree), el otro conjunto contiene los vértices aún no incluidos. En cada paso, va agregando vértices cuya distancia a los vértices de los incluidos en el MST mínima. Nuesta implementación tiene una complejidad O(V ^ 2).

El algoritmo de Kruskal es un algoritmo de la teoría de grafos. El cual comienza ordenando todos los bordes en orden no decreciente de su peso. Después, elije el arco más pequeño y comprueba si forma un ciclo con el MST formado hasta el momento. Si no hay ciclo, incluye el arco al MST. Si no, lo descarta y escoge otro arco. Repite este paso hasta que haya (v – 1) arcos en el MST. Nuesta implementación tiene una complejidad O(E log E).

El recorrido en preoerden de un árbol se realiza de esta manera: se visita el nodo raíz, luego recursivamente se realiza un recorrido en preorden del subárbol izquierdo, seguido de un recorrido en preorden del subárbol derecho. Para el presente trabajo optamos por implementar un algoritmo DFS, ya que es similar a un algoritmo preorden al recorrer la estructura de datos. Nuestra implementación tiene una complejidad O(E + V).

## 4. Diseño de pruebas

**Objetivos de las pruebas:** este documento, tiene como finalidad entregar las pautas y definir la estrategia que se seguirá para llevar a cabo la certificación del software TSP. 

**Alcance de las pruebas:** mediante los siguientes cuadros se describen los requerimientos de pruebas del sistema TSP.

**Cuadro resumen de las pruebas:** 

![Cuadro 1](https://i.ibb.co/W58F4mr/Cuadro1.jpg)

**Cuadro resumen de las pruebas unitarias de los componentes de la solución TSP:**

![Cuadro 2](https://i.ibb.co/M5B7vb2/Cuadro2.jpg)

**Criterios de aprobación / rechazo:**

Errores Graves, información crítica presentada erróneamente, información mal registrada en la base de datos, caídas de programas, incumplimiento de objetivos en funciones principales, etc. 

Errores Medios (comunes), errores en documentos impresos que se entregan a personas ajenas a la organización, errores en presentación de datos, incumplimiento de objetivos en funciones secundarias, caídas de programas auxiliares, etc.

Errores Leves, errores en presentación de datos secundarios, no adecuación a estándares, comportamientos correctos pero diferentes en situaciones similares, dificultades de operación, etc.

![Cuadro 3](https://i.ibb.co/fQfsbxc/Cuadro3.jpg)

## 5. Diseño de experimentos

**Implementación de pruebas de acuerdo con el diseño elaborado**

*Interfaz*

![Interfaz 1](https://i.ibb.co/tQ4yKG4/Codigo1.jpg)

![Interfaz 2](https://i.ibb.co/KmtNZYh/Interfaz2.jpg)

*Calcular*

![Calcular 1](https://i.ibb.co/PgrjPjy/Calcular1.jpg)

![Calcular 2](https://i.ibb.co/VwwFkyP/Calcular2.jpg)

*Mapa*

![Mapa 1](https://i.ibb.co/D19d7hF/Mapa1.jpg)

![Mapa 2](https://i.ibb.co/zJpthqv/Mapa2.jpg)

**Implementación de pruebas unitarias de los componentes de las solución TSP**

*Leer*

![Leer 1](https://i.ibb.co/kBtqgrK/Leer1.jpg)

*Grafito*

![Grafito 1](https://i.ibb.co/XJ7qsY8/Grafito1.jpg)

*Prim*

![Prim 1](https://i.ibb.co/cgN5yVS/Prim2.jpg)

![Prim 2](https://i.ibb.co/SmRnJmQ/Prim1.jpg)

*Kruskal*

![Kruskal 1](https://i.ibb.co/0sS1MHd/Kruskal2.jpg)

![Kruskal 2](https://i.ibb.co/d6xKs2k/Kruskal1.jpg)

*DFS*

![DFS 1](https://i.ibb.co/yXBQmNq/Preorder1.jpg)

**Medir atributos de calidad del desarrollo de la solución TSP**

*Caso 1*

![Caso 1](https://i.ibb.co/V9pvHxY/Caso1.jpg)

*Caso 2*

![Caso 2](https://i.ibb.co/q7WwK0y/Caso2.jpg)

*Caso 3*

![Caso 3](https://i.ibb.co/wN3F9Rb/Caso3.jpg)

## 6. Análisis e interpretación de datos/resultados

El timpo de ejecución, de la implementación del algoritmo de Prim como solución al TSP, esta bajo la formula O(V ^ 2).
Entonces, para cada *dataset*, el tiempo sería:
* Caso 1 - n = 25 -> 25^2 = 625 µs = 0.000625‬ s teóricamente.
* Caso 2 - n = 171 -> 171^2 = 29 241‬ µs = 0.029241 s teóricamente.
* Caso 3 - n = 1678 -> 1678^2  = 2 815 684‬ µs = 2,815648 s teóricamente.
* Caso 4 - n = 143351 -> 143351^2 = 20 549 509 201‬ µs = 5.7081970002778 h teóricamente.

El timpo de ejecución, de la implementación del algoritmo de Kruskal como solución al TSP, esta bajo la formula O(E log(E)). Al momento de leer los datos del *dataset* genera de 5 a 7 arcos por nodo, en el peor caso generaría 7 arcos por nodo.
Entonces, para cada *dataset*, el tiempo sería:
* Caso 1 - n = 25 -> E = 175 -> 175(log(175)) = 1303.96 µs = 0.00130396 s teóricamente.
* Caso 2 - n = 171 -> E = 1197 -> 1197(log(1197)) = 12 239.57 µs = 0.01223957 s teóricamente.
* Caso 3 - n = 1678 -> E = 11746‬ -> 11746(log(11746)) = 158 804.53 µs = 0.15880453 s teóricamente.
* Caso 4 - n = 143351 -> E = 1 003 457‬ -> 1 003 457‬(log(1 003 457‬)) = 20 005 468.01 µs = 20.00546801 s teóricamente.

## 7. Conclusiones

Luego de hacer las pruebas debidas, hemos comprobado que se ha podido implementar una solución parcial al TSP. La eficacia de los algoritmos es óptima cuando se trabaja con *datasets* parciales, que contengan una cantidad de datos razonables. Cuando se intenta trabajar con el *dataset* completo la eficacia de los algoritmos decrece.

## Referencias

  Espinoza, D. (2006). El Problema del Vendedor Viajero (TSP) y Programación Entera (IP) [diapositivas de PowerPoint]. Recuperado de http://www.dii.uchile.cl/~daespino/PApers/TSP_and_IP_chile_050820.pdf

  Kruskal’s Minimum Spanning Tree Algorithm | Greedy Algo-2. (s.f.). Recuerpado de https://www.geeksforgeeks.org/?p=26604/

  Prim’s Minimum Spanning Tree (MST) | Greedy Algo-5. (s.f.). Recuperado de https://www.geeksforgeeks.org/prims-minimum-spanning-tree-mst-greedy-algo-5/

  Recorridos de árboles. (s.f). Recuperado de http://interactivepython.org/runestone/static/pythoned/Trees/RecorridosDeArboles.html
