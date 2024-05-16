# AFloydWarshall

Este paquete Java implementa el algoritmo de Floyd-Warshall, el cual se utiliza para encontrar los caminos más cortos en un grafo ponderado con pesos de aristas positivos o negativos (pero sin ciclos negativos).

## Clase: AFloydWarshall

Esta clase contiene la implementación del algoritmo de Floyd-Warshall.

### Campos:

- `INF`: Una constante que representa el infinito. Se utiliza para inicializar las distancias entre los nodos que no tienen un borde directo entre ellos.
- `V`: El número de vértices en el grafo.

### Métodos:

- `floydWarshall(int graph[][])`: Este método implementa el algoritmo de Floyd-Warshall. Toma una matriz 2D que representa el grafo como entrada, donde `graph[i][j]` es el peso del borde del nodo `i` al nodo `j`. Si no hay un borde entre los nodos `i` y `j`, `graph[i][j]` debe ser igual a `INF`.

- `printSolution(int dist[][])`: Este método imprime la matriz de camino más corto. Toma una matriz 2D `dist` como entrada, donde `dist[i][j]` es la distancia más corta del nodo `i` al nodo `j`.

## Uso:

El método `main` crea un grafo, crea una instancia de `AFloydWarshall`, y llama al método `floydWarshall` en el grafo. Luego, la matriz de camino más corto se imprime en la consola.

```java
public static void main (String[] args) {
    int graph[][] = { {0,   5,  INF, 10},
                      {INF, 0,   3, INF},
                      {INF, INF, 0,   1},
                      {INF, INF, INF, 0}
                    };
    AFloydWarshall a = new AFloydWarshall();
    a.floydWarshall(graph);
}
