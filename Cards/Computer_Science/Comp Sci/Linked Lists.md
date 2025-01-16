up:: [[Computer Science MOC]]
tags:: #Programming  
## Linked List
- List structure with **a flexible data size**, an alternative to [[Arrays]] given flexible structure (no fixed size)
- Works by *packaging data into nodes*, and using a [[Pointers]] to *point to each next node*. List ends when it points to `null`
- End up wasting time on search because you can't run [[Binary Search]] (need to start at the beginning each time)
## Doubly Linked List
- **Doubly Linked List**
	- When a linked list loops back from the final node back to the starting node
		- Ex: A -> B -> C -> A
- ![[Pasted image 20240725164604.png]]
## Implementing
### Single
- Uses a single pointer to point to each memory node
```
#include <stdio.h>
#include <stdlib.h>

// Define the structure for a node
typedef struct Node {
    int data;
    struct Node* next;
} Node;

// Function to create a new node
Node* createNode(int data) {
    Node* newNode = (Node*)malloc(sizeof(Node));
    newNode->data = data;
    newNode->next = NULL;
    return newNode;
}

// Function to insert a node at the end
void insertEnd(Node** head, int data) {
    Node* newNode = createNode(data);
    if (*head == NULL) {
        *head = newNode;
        return;
    }
    Node* temp = *head;
    while (temp->next != NULL) {
        temp = temp->next;
    }
    temp->next = newNode;
}

// Function to print the linked list
void printList(Node* head) {
    Node* temp = head;
    while (temp != NULL) {
        printf("%d -> ", temp->data);
        temp = temp->next;
    }
    printf("NULL\n");
}

// Function to free the linked list
void freeList(Node* head) {
    Node* temp;
    while (head != NULL) {
        temp = head;
        head = head->next;
        free(temp);
    }
}

int main() {
    Node* head = NULL;

    // Inserting elements
    insertEnd(&head, 1);
    insertEnd(&head, 2);
    insertEnd(&head, 3);

    // Printing the list
    printList(head);

    // Freeing the list
    freeList(head);

    return 0;
}
`


```
### Double
```
#include <stdio.h>
#include <stdlib.h>

// Define the structure for a node
typedef struct DoublyNode {
    int data;
    struct DoublyNode* next;
    struct DoublyNode* prev;
} DoublyNode;

// Function to create a new node
DoublyNode* createDoublyNode(int data) {
    DoublyNode* newNode = (DoublyNode*)malloc(sizeof(DoublyNode));
    newNode->data = data;
    newNode->next = NULL;
    newNode->prev = NULL;
    return newNode;
}

// Function to insert a node at the end
void insertEndDoubly(DoublyNode** head, int data) {
    DoublyNode* newNode = createDoublyNode(data);
    if (*head == NULL) {
        *head = newNode;
        return;
    }
    DoublyNode* temp = *head;
    while (temp->next != NULL) {
        temp = temp->next;
    }
    temp->next = newNode;
    newNode->prev = temp;
}

// Function to print the doubly linked list
void printDoublyList(DoublyNode* head) {
    DoublyNode* temp = head;
    while (temp != NULL) {
        printf("%d <-> ", temp->data);
        temp = temp->next;
    }
    printf("NULL\n");
}

// Function to free the doubly linked list
void freeDoublyList(DoublyNode* head) {
    DoublyNode* temp;
    while (head != NULL) {
        temp = head;
        head = head->next;
        free(temp);
    }
}

int main() {
    DoublyNode* head = NULL;

    // Inserting elements
    insertEndDoubly(&head, 1);
    insertEndDoubly(&head, 2);
    insertEndDoubly(&head, 3);

    // Printing the list
    printDoublyList(head);

    // Freeing the list
    freeDoublyList(head);

    return 0;
}
```
