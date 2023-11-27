# Arrays

This folder contains code examples and information related to working with arrays in PHP.

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

## Remove an Element at a Specific Index

You can use the unset() function to remove an element at a specific index:
```php
$indexToRemove = 2;
unset($numbers[$indexToRemove]); // Removes the element at index 2
```
## External Resources

- **sort($array):** Sorts an array in ascending order.
- **rsort($array):** Sorts an array in descending order.
- **asort($array):** Sorts an associative array in ascending order, maintaining key-value associations.
- **ksort($array):** Sorts an associative array by keys.
- **arsort($array):** Sorts an associative array in descending order, maintaining key-value associations.
- **krsort($array):** Sorts an associative array by keys in descending order.

### Filtering Functions

- **array_filter($array, $callback):** Filters elements of an array using a callback function.
- **array_map($callback, $array):** Applies a callback function to each element of an array and returns the modified array.
- **array_reduce($array, $callback, $initial):** Reduces an array to a single value using a callback function.

### Manipulation Functions

- **array_merge($array1, $array2):** Merges two or more arrays.
- **array_slice($array, $offset, $length):** Returns a slice of an array.
- **array_splice($array, $offset, $length, $replacement):** Removes a portion of the array and replaces it with something else.

### Other Useful Functions

- **count($array):** Returns the number of elements in an array.
- **in_array($needle, $haystack):** Checks if a value exists in an array.
- **array_search($needle, $haystack):** Searches an array for a given value and returns the corresponding key if successful.

This is just a glimpse of the many array functions PHP offers. Exploring these functions will greatly enhance your ability to work with arrays effectively.

For further learning and reference, consider exploring the following external resources:

- [GeeksforGeeks](https://www.geeksforgeeks.org/data-structures/arrays/)
- [Wikipedia](https://en.wikipedia.org/wiki/arrays)

Feel free to dive into the code examples and explanations provided in this folder to enhance your understanding of linked lists. You can also contribute to this repository by adding more linked list-related content or improvements.

Happy coding!


