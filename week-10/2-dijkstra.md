# Today, I understand about dijkstra for presentation and I implemented the algorithm in C.

## Here is the PROOF OF BUILD:
```C
#include <stdio.h>
#include <limits.h>
#define V 4

int main()
{
    int graph[V][V] = {
        {-1, 2, 5, -1},
        {2, -1, 1, 7},
        {5, 1, -1, 2},
        {-1, 7, 2, -1}};

    int visited[V] = {0};

    int dist[V] = {INT_MAX, INT_MAX, INT_MAX, INT_MAX};

    dist[0] = 0;

    while (1)
    {
        int current = -1;
        int minDistance = INT_MAX;

        // 1. Find the cheapest unvisited node
        for (int i = 0; i < V; i++)
        {
            if (visited[i] == 0 && dist[i] < minDistance)
            {
                minDistance = dist[i];
                current = i;
            }
        }

        // 2. Stop if no reachable node exists
        if (current == -1)
        {
            break;
        }

        // 3. Relax the edges to its neighbors
        for (int neighbor = 0; neighbor < V; neighbor++)
        {
            if (graph[current][neighbor] != -1 && visited[neighbor] == 0)
            {

                int newCost = dist[current] + graph[current][neighbor];

                if (newCost < dist[neighbor])
                {
                    dist[neighbor] = newCost;
                }
            }
        }

        // 4. Finalize this node
        visited[current] = 1;
    }

    for (int i = 0; i < V; i++)
    {
        printf("%d ", dist[i]);
    }
}
```