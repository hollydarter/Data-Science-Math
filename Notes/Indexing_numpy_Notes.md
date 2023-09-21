### Indexing in numpy - 9.17

Indexing in NumPy works similarly to indexing in Python lists but offers more advanced indexing options for multidimensional arrays. NumPy arrays can be indexed in the following ways:

## 1. Single Element Indexing:

You can access a single element from a NumPy array by specifying the index of that element for each dimension.

import numpy as np

arr = np.array([1, 2, 3, 4, 5])
element = arr[2]  # Access the element at index 2 (3rd element)
print(element)  # Output: 3

## 2. Slicing:

You can extract a portion of an array using slicing. This allows you to create a new array that contains a range of elements.

arr = np.array([1, 2, 3, 4, 5])
subset = arr[1:4]  # Slice from index 1 (inclusive) to index 4 (exclusive)
print(subset)  # Output: [2 3 4]

## 3. Negative Indexing:

Negative indices count from the end of the array. -1 refers to the last element, -2 to the second-to-last, and so on.

arr = np.array([1, 2, 3, 4, 5])
last_element = arr[-1]  # Access the last element
print(last_element)  # Output: 5

## 4. Multidimensional Array Indexing:

For multidimensional arrays, you specify indices for each dimension, separated by commas.

import numpy as np

matrix = np.array([[1, 2, 3],
                   [4, 5, 6],
                   [7, 8, 9]])
element = matrix[1, 2]  # Access the element in row 1, column 2 (6)
print(element)  # Output: 6

## 5. Slicing Multidimensional Arrays:
You can use slicing for multidimensional arrays as well, specifying a range for each dimension.

import numpy as np

matrix = np.array([[1, 2, 3],
                   [4, 5, 6],
                   [7, 8, 9]])
subset = matrix[0:2, 1:3]  # Slice rows 0 and 1, and columns 1 and 2
print(subset)
# Output:
# [[2 3]
#  [5 6]]

## 6. Boolean Indexing:
You can use Boolean arrays to filter elements based on a condition.

import numpy as np

arr = np.array([1, 2, 3, 4, 5])
condition = arr > 3  # Creates a Boolean array with True for elements > 3
result = arr[condition]
print(result)  # Output: [4 5]

These are some of the fundamental ways to index and slice NumPy arrays. NumPy provides powerful capabilities for manipulating and extracting data from arrays, making it a versatile library for numerical computing and data analysis.
