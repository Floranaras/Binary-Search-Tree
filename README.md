# Binary Search Tree Implementation

A comprehensive Binary Search Tree (BST) implementation in C with various tree operations and traversal methods.

## Project Structure

```
bst_project/
├── include/
│   ├── app.h
│   ├── BST.h
│   ├── binTree.h
│   ├── delete.h
│   ├── minMax.h
│   ├── neighbor.h
│   ├── search.h
│   └── transversal.h
├── src/
│   ├── app.c
│   ├── binTree.c
│   ├── delete.c
│   ├── main.c
│   ├── minMax.c
│   ├── neighbor.c
│   ├── search.c
│   └── transversal.c
├── obj/
├── Makefile
└── README.md
```

## Features

The BST implementation provides the following operations:

### Core Tree Operations
- **Create**: Initialize an empty tree
- **Insert**: Add new nodes to the tree
- **Search**: Find nodes by key value
- **Delete**: Remove nodes from the tree with proper restructuring

### Tree Traversal
- **Inorder**: Left → Root → Right (sorted order)
- **Preorder**: Root → Left → Right
- **Postorder**: Left → Right → Root

### Utility Functions
- **Min/Max**: Find minimum and maximum values
- **Successor**: Find the next larger value
- **Predecessor**: Find the next smaller value
- **Memory Management**: Proper cleanup with tree deallocation

## Data Structure

The BST uses the following node structure:

```c
typedef struct node {
    int key;
    struct node *pLeft;
    struct node *pRight;
} nodeType;
```

## Building the Project

### Prerequisites
- GCC compiler
- Make utility

### Compilation
```bash
make all
```

### Other Make Targets
```bash
make clean      # Remove build artifacts
make rebuild    # Clean and build
make run        # Build and execute
```

## Usage

The program demonstrates all BST operations with a predefined set of values:

```c
// Sample tree construction
22, 16, 13, 9, 20, 21, 55, 30, 25, 40, 90
```

### Running the Program
```bash
./bst_program
```

### Expected Output
The program will display:
- Tree traversals in all three orders
- Search demonstration
- Min/max value identification
- Successor/predecessor examples
- Node deletion demonstration

## Module Descriptions

### BST.h
Core data structure definitions and standard library includes.

### binTree.c/h
Basic tree operations including node creation, insertion, and memory management.

### search.c/h
Binary search implementation for finding nodes by key value.

### transversal.c/h
Three standard tree traversal algorithms with visit function.

### minMax.c/h
Functions to find minimum and maximum values in the tree.

### neighbor.c/h
Advanced operations for finding predecessor and successor nodes.

### delete.c/h
Complex node deletion handling all three cases (leaf, one child, two children).

### app.c/h
Main application logic and demonstration of all BST operations.

## Algorithm Complexity

| Operation | Average Case | Worst Case |
|-----------|--------------|------------|
| Search    | O(log n)     | O(n)       |
| Insert    | O(log n)     | O(n)       |
| Delete    | O(log n)     | O(n)       |
| Traversal | O(n)         | O(n)       |

## Memory Management

The implementation includes proper memory management:
- Dynamic allocation for each node
- Recursive tree deallocation in `freeTree()`
- Temporary memory cleanup in neighbor operations

## Error Handling

The code includes basic error handling for:
- NULL pointer checks
- Memory allocation failures
- Edge cases in deletion (root node, leaf nodes)

## Compilation Flags

The Makefile uses the following compiler flags:
- `-Wall -Wextra`: Enable comprehensive warnings
- `-std=c99`: Use C99 standard
- `-g`: Include debugging information
- `-Iinclude`: Specify header file directory

## License

This project is provided for educational purposes.
