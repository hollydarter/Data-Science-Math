### Numpy Notes - 9.15

NumPy is a powerful Python library for numerical and scientific computing. It provides support for arrays and matrices, along with a wide range of mathematical functions to operate on these arrays. Here, I'll give you a beginner's guide to using NumPy:

### Installing NumPy:
If you haven't already installed NumPy, you can do so using pip:

pip install numpy
Importing NumPy:
Start by importing NumPy in your Python script or Jupyter Notebook:

import numpy as np
This is a common convention where we import NumPy as np to make the code more concise.

### Creating Arrays:
NumPy primarily deals with arrays. You can create arrays in various ways:

### Creating an array from a Python list:

python
Copy code
arr = np.array([1, 2, 3, 4, 5])
Creating a multi-dimensional array:

python
Copy code
matrix = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

### Creating arrays with zeros, ones, or a specific range:

zeros = np.zeros((2, 3))  # Creates a 2x3 array filled with zeros
ones = np.ones((3, 2))    # Creates a 3x2 array filled with ones
rng = np.arange(0, 10, 2) # Creates an array [0, 2, 4, 6, 8]
Array Attributes:
NumPy arrays have useful attributes, such as shape, dtype, and size. For example:

arr = np.array([1, 2, 3, 4, 5])
print(arr.shape)  # Prints (5,) for a 1D array
print(arr.dtype)  # Prints int64 for integer data type
print(arr.size)   # Prints 5 for the number of elements

### Indexing and Slicing:
You can access elements in an array using indexing and slice arrays to get specific portions:

arr = np.array([1, 2, 3, 4, 5])
print(arr[0])     # Access the first element (1)
print(arr[1:4])   # Access elements at index 1, 2, and 3

### Basic Operations:
NumPy allows you to perform operations on arrays element-wise, which is one of its strengths:

a = np.array([1, 2, 3])
b = np.array([4, 5, 6])

addition = a + b        # [5, 7, 9]
subtraction = a - b     # [-3, -3, -3]
multiplication = a * b  # [4, 10, 18]
division = a / b        # [0.25, 0.4, 0.5]

### Mathematical Functions:

NumPy provides a wide range of mathematical functions that can be applied to arrays directly:
arr = np.array([1, 2, 3, 4, 5])
mean = np.mean(arr)   # Calculate the mean (average)
std_dev = np.std(arr) # Calculate the standard deviation
max_val = np.max(arr) # Find the maximum value
min_val = np.min(arr) # Find the minimum value

### Array Manipulation:
You can reshape, concatenate, and transpose arrays:

arr = np.array([[1, 2, 3], [4, 5, 6]])
reshaped = arr.reshape(3, 2)  # Reshape to a 3x2 array
concatenated = np.concatenate((arr, arr), axis=0)  # Concatenate vertically
transposed = arr.T  # Transpose the array
