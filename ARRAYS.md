# Arrays

Welcome to the "Arrays" folder in this repository! This folder contains code examples and information related to working with arrays in PHP. Whether you're new to programming or looking for specific array-related operations, you'll find useful resources here.

## Contents

1. [Creating Arrays](#creating-arrays)
2. [Adding Elements](#adding-elements)
    - [Add to End](#add-to-end)
    - [Add to Beginning](#add-to-beginning)
    - [Insert at Specific Index](#insert-at-specific-index)
3. [Removing Elements](#removing-elements)
    - [Remove First](#remove-first)
    - [Remove Last](#remove-last)
    - [Remove at Specific Index](#remove-at-specific-index)

## Creating Arrays

To create an array in PHP, you can use square brackets `[]` or the `array()` constructor. Here's how:

```php
$myArray = []; // Empty array
$numbers = [1, 2, 3, 4, 5]; // Array with values
```

## Adding to End

You can add an element to the end of an array using the [] operator:
```php
$numbers[] = 6; // Adds 6 to the end of the $numbers array
```

## Add to Beginning

Use the array_unshift() function to add an element to the beginning of an array:
```php
array_unshift($numbers, 0); // Adds 0 to the beginning of the $numbers array
```

## Insert at Specific Index

To insert an element at a specific index, you can use the array_splice() function:
```php
$index = 2;
$elementToInsert = 7;
array_splice($numbers, $index, 0, $elementToInsert); // Inserts 7 at index 2
```

## Remove the First Element from an Array

You can use the array_shift() function to remove the first element from an array:
```php
$firstElement = array_shift($numbers); // Removes and returns the first element
```

## Remove the Last Element from an Array

You can use the array_pop() function to remove the last element from an array:
```php
$lastElement = array_pop($numbers); // Removes and returns the last element
```

## Remove an Element at a Specific Index:

You can use the unset() function to remove an element at a specific index:
```php
$indexToRemove = 2;
unset($numbers[$indexToRemove]); // Removes the element at index 2
```

## Adding Elements - Add to End

You can add an element to the end of an array using the [] operator:
```php
$numbers[] = 6; // Adds 6 to the end of the $numbers array
```

