# Problema de vendedor ambulante

## 1. Introducción

El problema del vendedor viajero o también conocido como TSP (por siglas en ingles). Consiste en encontrar, en un grupo finito de ciudades y sus respectivos costos de viajes entre ciudad y ciudad, el camino más económico de recorrer todas las ciudades. Dicho recorrido tiene ciertas condiciones, se debe iniciar el recorrido en una ciudad, pasar por todas las ciudades, solamente una vez, y terminar en la ciudad en la que se comenzó. Esto debe ser logrado teniendo en consideración que el resultado debe ser el recorrido que tenga el menor costo.

A lo largo de la historia, se han diversas soluciones a este problema. Por ejemplo:

> Karl Menger (Shortest Hamiltonian Path, 1930), J.B. Robinson (Hamiltonian game, 1949), G. Dantzig, R. Fulkerson, y S. Johnson (Solution of a large-scale traveling-salesman problem, 1954), M. Held and R.M. Karp (Introducción de heurísticas basadas en programación dinámica, 1962), entre otros. (Espinoza, 2006)

La principal motivación para el desarrollo del proyecto, consiste en las diferentes aplicaciones del TSP. Algunas de ellas son estudio en la secuencia de genes, diseño de chips, enrutamiento de vehículos, entre otras.

## 2. Objetivo

El presente trabajo tiene como objetivo principal encontrar una solución parcial al problema de TSP usando una dataset del Ministerio de Educación del Perú. La cual contiene la posición geográfica (latitud y longitud) de cada centro poblado del Perú.

## 3.	Marco Teórico

El algoritmo de Prim es un algoritmo perteneciente a la teoría de los grafos. El cual comienza con un árbol de expansión vacío. La idea es mantener dos conjuntos de vértices. El primer conjunto contiene los vértices ya incluidos en el MST (minimum spanning tree), el otro conjunto contiene los vértices aún no incluidos. En cada paso, va agregando vértices cuya distancia a los vértices de los incluidos en el MST mínima.

El algoritmo de Kruskal es un algoritmo de la teoría de grafos. El cual comienza ordenando todos los bordes en orden no decreciente de su peso. Después, elije el arco más pequeño y comprueba si forma un ciclo con el MST formado hasta el momento. Si no hay ciclo, incluye el arco al MST. Si no, lo descarta y escoge otro arco. Repite este paso hasta que haya (v – 1) arcos en el MST.

El recorrido en preoerden de un árbol se realiza de esta manera: se visita el nodo raíz, luego recursivamente se realiza un recorrido en preorden del subárbol izquierdo, seguido de un recorrido en preorden del subárbol derecho.

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

![Prim 1](https://i.ibb.co/m5RgsP2/Prim1.jpg)

*Kruskal*

![Kruskal 1](https://i.ibb.co/ThPvm09/Kruskal1.jpg)

![Kruskal 2](https://i.ibb.co/mNjNQwT/Kruskal2.jpg)

![Kruskal 3](https://i.ibb.co/qRkGXz9/Kruskal3.jpg)

*Preorder*

![Preorder 1](https://i.ibb.co/1b3HSSb/Preorder1.jpg)

**Medir atributos de calidad del desarrollo de la solución TSP**

*Caso 1*

![Caso 1](https://i.ibb.co/V9pvHxY/Caso1.jpg)

*Caso 2*

![Caso 2](https://i.ibb.co/q7WwK0y/Caso2.jpg)

*Caso 3*

![Caso 3](https://i.ibb.co/wN3F9Rb/Caso3.jpg)

## Referencias

Espinoza, D. (2006). El Problema del Vendedor Viajero (TSP) y Programación Entera (IP) [diapositivas de PowerPoint]. Recuperado de: http://www.dii.uchile.cl/~daespino/PApers/TSP_and_IP_chile_050820.pdf

Prim’s Minimum Spanning Tree (MST) | Greedy Algo-5. (s.f.). Recuperado de: https://www.geeksforgeeks.org/prims-minimum-spanning-tree-mst-greedy-algo-5/

Kruskal’s Minimum Spanning Tree Algorithm | Greedy Algo-2. (s.f.). Recuerpado de: https://www.geeksforgeeks.org/?p=26604/

Recorridos de árboles. (s.f). Recuperado de: http://interactivepython.org/runestone/static/pythoned/Trees/RecorridosDeArboles.html
