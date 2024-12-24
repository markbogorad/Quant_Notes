up:: [[Computer Science MOC]]
tags:: #Programming  
# Hash Maps
- A data structure built on top of an [[Arrays]] to store key-value pairs (in [[Containers]] in C++ MOC), combined with [[Linked Lists]] traversing
	- Uses a hash function
	- Faster than [[Dictionaries]]
		- Goes at O(n) [[Program Running Time (Big O)]] if large enough it can be O(1)
- How it works
	- It sorts key-value pairs into groups, making it faster to find
	- Think of it as sorting a deck of cards by their symbol
## It's an array of linked lists:
- ![[Pasted image 20240707122839.png]]

## Implementation C
```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

// Define the structure for the linked list node
typedef struct HashNode {
    char* key;
    char* value;
    struct HashNode* next;
} HashNode;

// Define the structure for the hash table
typedef struct HashTable {
    int size;
    HashNode** table;
} HashTable;

// Create a new hash node
HashNode* createNode(const char* key, const char* value) {
    HashNode* newNode = (HashNode*)malloc(sizeof(HashNode));
    newNode->key = strdup(key);
    newNode->value = strdup(value);
    newNode->next = NULL;
    return newNode;
}

// Create a hash table
HashTable* createHashTable(int size) {
    HashTable* hashTable = (HashTable*)malloc(sizeof(HashTable));
    hashTable->size = size;
    hashTable->table = (HashNode**)malloc(size * sizeof(HashNode*));
    for (int i = 0; i < size; i++) {
        hashTable->table[i] = NULL;
    }
    return hashTable;
}

// Hash function
unsigned int hash(const char* key, int tableSize) {
    unsigned int hashValue = 0;
    for (int i = 0; key[i] != '\0'; i++) {
        hashValue += key[i];
    }
    return hashValue % tableSize;
}

// Insert into hash table
void insert(HashTable* hashTable, const char* key, const char* value) {
    unsigned int hashIndex = hash(key, hashTable->size);
    HashNode* newNode = createNode(key, value);
    newNode->next = hashTable->table[hashIndex];
    hashTable->table[hashIndex] = newNode;
}

// Search in hash table
char* search(HashTable* hashTable, const char* key) {
    unsigned int hashIndex = hash(key, hashTable->size);
    HashNode* node = hashTable->table[hashIndex];
    while (node != NULL) {
        if (strcmp(node->key, key) == 0) {
            return node->value;
        }
        node = node->next;
    }
    return NULL;
}

// Remove from hash table
void delete(HashTable* hashTable, const char* key) {
    unsigned int hashIndex = hash(key, hashTable->size);
    HashNode* node = hashTable->table[hashIndex];
    HashNode* prev = NULL;

    while (node != NULL && strcmp(node->key, key) != 0) {
        prev = node;
        node = node->next;
    }

    if (node == NULL) return; // Key not found

    if (prev == NULL) {
        hashTable->table[hashIndex] = node->next;
    } else {
        prev->next = node->next;
    }

    free(node->key);
    free(node->value);
    free(node);
}

// Print the hash table
void printHashTable(HashTable* hashTable) {
    for (int i = 0; i < hashTable->size; i++) {
        printf("Index %d: ", i);
        HashNode* node = hashTable->table[i];
        while (node != NULL) {
            printf("(%s, %s) -> ", node->key, node->value);
            node = node->next;
        }
        printf("NULL\n");
    }
}

// Main function to demonstrate hash table operations
int main() {
    HashTable* hashTable = createHashTable(10);

    insert(hashTable, "name", "Alice");
    insert(hashTable, "age", "25");
    insert(hashTable, "city", "New York");

    printf("Search for 'name': %s\n", search(hashTable, "name"));
    printf("Search for 'age': %s\n", search(hashTable, "age"));
    printf("Search for 'city': %s\n", search(hashTable, "city"));

    printHashTable(hashTable);

    delete(hashTable, "age");
    printf("After deleting 'age':\n");
    printHashTable(hashTable);

    return 0;
}

```