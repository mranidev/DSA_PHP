# Linked Lists

Welcome to the "Linked Lists" folder in this repository! This folder contains code examples, explanations, and resources related to linked lists data structures. Whether you're new to linked lists or looking for specific operations and implementations, you'll find useful information here.

## Contents

1. [Introduction to Linked Lists](#introduction-to-linked-lists)
2. [Singly Linked Lists](#singly-linked-lists)
3. [Doubly Linked Lists](#doubly-linked-lists)
4. [Circular Linked Lists](#circular-linked-lists)
5. [Common Operations](#common-operations)
    - [Insertion](#insertion)
    - [Deletion](#deletion)
    - [Traversal](#traversal)
6. [External Resources](#external-resources)

## Introduction to Linked Lists

A linked list is a fundamental data structure consisting of nodes, each containing data and a reference to the next (and possibly previous) node. This folder provides an introduction to various types of linked lists and their usage.

![Linked List](https://simplesnippets.tech/wp-content/uploads/2019/06/linked-list-data-structure-block-diagram1.png)

### Singly Linked Lists:

Singly Linked Lists are a type of linked list where each node points to the next node in the sequence. They consist of nodes, where each node contains a data element and a reference (or pointer) to the next node in the sequence. The last node typically points to `NULL` to indicate the end of the list.

#### Structure:
- Each node contains two components:
  1. Data: The value or payload stored in the node.
  2. Next: A reference (pointer) to the next node in the sequence.

#### Common Operations:
1. **Insertion**: Adding a new node to the list.
2. **Deletion**: Removing a node from the list.
3. **Traversal**: Iterating through the list to access or manipulate nodes.

#### Example PHP Code:

```php
class Node {
    public $data;
    public $next;

    public function __construct($data) {
        $this->data = $data;
        $this->next = null;
    }
}

class SinglyLinkedList {
    public $head;

    public function __construct() {
        $this->head = null;
    }

    // Inserting a new node at the beginning of the list
    public function insertAtBeginning($data) {
        $newNode = new Node($data);
        $newNode->next = $this->head;
        $this->head = $newNode;
    }

    // Inserting a new node at the end of the list
    public function insertAtEnd($data) {
        $newNode = new Node($data);
        if ($this->head === null) {
            $this->head = $newNode;
            return;
        }
        $current = $this->head;
        while ($current->next !== null) {
            $current = $current->next;
        }
        $current->next = $newNode;
    }

    // Traversing the list and printing its elements
    public function display() {
        $current = $this->head;
        while ($current !== null) {
            echo $current->data . " ";
            $current = $current->next;
        }
    }
}

// Example usage:
$linkedList = new SinglyLinkedList();
$linkedList->insertAtBeginning(3);
$linkedList->insertAtBeginning(2);
$linkedList->insertAtBeginning(1);
$linkedList->insertAtEnd(4);
$linkedList->insertAtEnd(5);
$linkedList->display(); // Output: 1 2 3 4 5```

### Doubly Linked Lists:

Doubly Linked Lists are a type of linked list where each node points to both the next and the previous nodes in the sequence. They consist of nodes, where each node contains a data element, a reference (or pointer) to the next node, and a reference (or pointer) to the previous node. This bidirectional linkage allows traversal in both forward and backward directions.

#### Structure:
- Each node contains three components:
  1. Data: The value or payload stored in the node.
  2. Next: A reference (pointer) to the next node in the sequence.
  3. Previous: A reference (pointer) to the previous node in the sequence.

#### Common Operations:
1. **Insertion**: Adding a new node to the list.
2. **Deletion**: Removing a node from the list.
3. **Traversal**: Iterating through the list to access or manipulate nodes.

#### Example PHP Code:

```php
class Node {
    public $data;
    public $next;
    public $prev;

    public function __construct($data) {
        $this->data = $data;
        $this->next = null;
        $this->prev = null;
    }
}

class DoublyLinkedList {
    public $head;
    public $tail;

    public function __construct() {
        $this->head = null;
        $this->tail = null;
    }

    // Inserting a new node at the beginning of the list
    public function insertAtBeginning($data) {
        $newNode = new Node($data);
        if ($this->head === null) {
            $this->head = $newNode;
            $this->tail = $newNode;
        } else {
            $newNode->next = $this->head;
            $this->head->prev = $newNode;
            $this->head = $newNode;
        }
    }

    // Inserting a new node at the end of the list
    public function insertAtEnd($data) {
        $newNode = new Node($data);
        if ($this->tail === null) {
            $this->head = $newNode;
            $this->tail = $newNode;
        } else {
            $newNode->prev = $this->tail;
            $this->tail->next = $newNode;
            $this->tail = $newNode;
        }
    }

    // Traversing the list forward and printing its elements
    public function displayForward() {
        $current = $this->head;
        while ($current !== null) {
            echo $current->data . " ";
            $current = $current->next;
        }
    }

    // Traversing the list backward and printing its elements
    public function displayBackward() {
        $current = $this->tail;
        while ($current !== null) {
            echo $current->data . " ";
            $current = $current->prev;
        }
    }
}

// Example usage:
$doublyLinkedList = new DoublyLinkedList();
$doublyLinkedList->insertAtBeginning(3);
$doublyLinkedList->insertAtBeginning(2);
$doublyLinkedList->insertAtBeginning(1);
$doublyLinkedList->insertAtEnd(4);
$doublyLinkedList->insertAtEnd(5);

echo "Forward traversal: ";
$doublyLinkedList->displayForward(); // Output: 1 2 3 4 5
echo "\n";

echo "Backward traversal: ";
$doublyLinkedList->displayBackward(); // Output: 5 4 3 2 1


