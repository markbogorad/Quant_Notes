up:: [[Computer Science MOC]]
tags:: #Programming  
# Graphs
- For complex relationships
	- Can be constructed with [[Dictionaries]] or [[Hash Tables]]
![[Pasted image 20240725195725.png]]
- A collection of vertices (points) and edges (connections to points)
- [[Search Trees]] are a subset of graphs
- Directed graph: can only move 1 direction (A --> B)
- Undirected graph: can move back and fourth
## Usage
- Can be useful for finding the quickest path to something (think levels of seperation from something)
	- Ex: friend list from Facebook 
	- Ex: google maps shortest paths
## Implementation C
```
#include <stdio.h>
#include <stdlib.h>

// Define a structure for the adjacency list node
typedef struct AdjListNode {
    int dest;
    struct AdjListNode* next;
} AdjListNode;

// Define a structure for the adjacency list
typedef struct AdjList {
    AdjListNode* head;
} AdjList;

// Define a structure for the graph
typedef struct Graph {
    int V;
    AdjList* array;
} Graph;

// Create a new adjacency list node
AdjListNode* newAdjListNode(int dest) {
    AdjListNode* newNode = (AdjListNode*)malloc(sizeof(AdjListNode));
    newNode->dest = dest;
    newNode->next = NULL;
    return newNode;
}

// Create a graph of V vertices
Graph* createGraph(int V) {
    Graph* graph = (Graph*)malloc(sizeof(Graph));
    graph->V = V;
    graph->array = (AdjList*)malloc(V * sizeof(AdjList));

    for (int i = 0; i < V; ++i) {
        graph->array[i].head = NULL;
    }
    return graph;
}

// Add an edge to an undirected graph
void addEdge(Graph* graph, int src, int dest) {
    // Add an edge from src to dest
    AdjListNode* newNode = newAdjListNode(dest);
    newNode->next = graph->array[src].head;
    graph->array[src].head = newNode;

    // Since graph is undirected, add an edge from dest to src
    newNode = newAdjListNode(src);
    newNode->next = graph->array[dest].head;
    graph->array[dest].head = newNode;
}

// Print the graph
void printGraph(Graph* graph) {
    for (int v = 0; v < graph->V; ++v) {
        AdjListNode* pCrawl = graph->array[v].head;
        printf("\n Adjacency list of vertex %d\n head ", v);
        while (pCrawl) {
            printf("-> %d", pCrawl->dest);
            pCrawl = pCrawl->next;
        }
        printf("\n");
    }
}

// Main function to demonstrate graph operations
int main() {
    int V = 5;
    Graph* graph = createGraph(V);
    addEdge(graph, 0, 1);
    addEdge(graph, 0, 4);
    addEdge(graph, 1, 2);
    addEdge(graph, 1, 3);
    addEdge(graph, 1, 4);
    addEdge(graph, 2, 3);
    addEdge(graph, 3, 4);

    printGraph(graph);

    return 0;
}

```