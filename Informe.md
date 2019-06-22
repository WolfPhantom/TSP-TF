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

## 4. Diseño de pruebas

**Objetivos de las pruebas:** este documento, tiene como finalidad entregar las pautas y definir la estrategia que se seguirá para llevar a cabo la certificación del software TSP. 

**Alcance de las pruebas:** mediante los siguientes cuadros se describen los requerimientos de pruebas del sistema TSP.

**Cuadro resumen de las pruebas:** 
| :-------- | :-------- |
| Módulos del Sistema Sencillito a ser probados | * Módulos: * interfaz * calcular * mapa | 
| Objetivos de las pruebas | * En estos Módulos se realizarán pruebas para validar: * La visualización de los datos, ingresados o modificados. * La graficación en un mapa topográfico de las solución. * La visualización de la resolución del Problema. * La respuesta y realización de las transacciones de cada módulo. | 
| Detalle del orden de ejecución de los módulos	| * Los módulos se deben ejecutar en forma independiente, pero consecutivos en el orden siguiente:

* interfaz
* calcular
* mapa | 
| Responsabilidad de la prueba | Las pruebas son responsabilidad del Testing Operacional del equipo de proyecto. |
