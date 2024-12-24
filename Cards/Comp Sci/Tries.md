up:: [[Computer Science MOC]]
tags:: #Programming  
# Trie
- A [[Search Trees]] of [[Arrays]]
- O(1) --> [[Program Running Time (Big O)]]
- Takes up a lot of space due to `nullptr` everywhere where the tri isnt used
- **Trie Structure:**
	- Each node represents a single character of the input strings.
	- The root node represents the empty string.
	- Each path down the tree may represent a single word.
## Implementation in C
```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

#define ALPHABET_SIZE 26

// Trie node
struct TrieNode {
    struct TrieNode *children[ALPHABET_SIZE];
    int isEndOfWord;
};

// Function to create a new Trie node
struct TrieNode *createNode(void) {
    struct TrieNode *node = (struct TrieNode *)malloc(sizeof(struct TrieNode));
    node->isEndOfWord = 0;

    for (int i = 0; i < ALPHABET_SIZE; i++) {
        node->children[i] = NULL;
    }

    return node;
}

// Function to insert a word into the Trie
void insert(struct TrieNode *root, const char *word) {
    struct TrieNode *current = root;

    while (*word) {
        int index = *word - 'a';
        if (!current->children[index]) {
            current->children[index] = createNode();
        }
        current = current->children[index];
        word++;
    }

    current->isEndOfWord = 1;
}

// Function to search for a word in the Trie
int search(struct TrieNode *root, const char *word) {
    struct TrieNode *current = root;

    while (*word) {
        int index = *word - 'a';
        if (!current->children[index]) {
            return 0;
        }
        current = current->children[index];
        word++;
    }

    return current != NULL && current->isEndOfWord;
}

// Function to free the Trie
void freeTrie(struct TrieNode *root) {
    for (int i = 0; i < ALPHABET_SIZE; i++) {
        if (root->children[i]) {
            freeTrie(root->children[i]);
        }
    }
    free(root);
}

// Driver code
int main() {
    // Creating the root of the Trie
    struct TrieNode *root = createNode();

    // Inserting words into the Trie
    insert(root, "hello");
    insert(root, "world");

    // Searching for words in the Trie
    printf("Searching for 'hello': %s\n", search(root, "hello") ? "Found" : "Not Found");
    printf("Searching for 'world': %s\n", search(root, "world") ? "Found" : "Not Found");
    printf("Searching for 'helloworld': %s\n", search(root, "helloworld") ? "Found" : "Not Found");

    // Freeing the Trie
    freeTrie(root);

    return 0;
}

```