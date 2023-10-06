# Problem Set One - Data Science Math

# Introduction
This Markdown document outlines a problem set in data science mathematics, including loading the MNIST dataset, visualizing images, and running a random model on MNIST.

## Question One - Load MNIST and Display Montage
To begin, we import necessary packages and define functions for data handling and visualization.

# Importing required packages
import numpy as np <br>
import matplotlib.pyplot as plt  <br>
import torch from torchvision <br>
import datasets from skimage.util <br>
import montage from skimage.io import imread <br>

# Functions for GPU data handling
def GPU(data): <br>
    return torch.tensor(data, requires_grad=True, dtype=torch.float, device=torch.device('cuda'))

def GPU_data(data): <br>
    return torch.tensor(data, requires_grad=False, dtype=torch.float, device=torch.device('cuda'))

# Functions for plotting a montage of images
def plot(x): <br>

# Code for plotting images <br>
    pass

def montage_plot(x):<br>

# Code for creating and displaying montages
    pass

# Downloading and preparing the MNIST dataset
train_set = datasets.MNIST('./data', train=True, download=True)<br>
test_set = datasets.MNIST('./data', train=False, download=True)

# Converting datasets to NumPy arrays and normalizing values
X = train_set.data.numpy()<br>
X_test = test_set.data.numpy()<br>
Y = train_set.targets.numpy()<br>
Y_test = test_set.targets.numpy()<br>
X = X[:, None, :, :] / 255<br>
X_test = X_test[:, None, :, :] / 255<br>

# Display a montage of images
montage_plot(X[125:150, 0, :, :])<br>
Question Two - Running a Random Model (y=mx) on MNIST<br>
In this section, we reshape the data, transfer it to the GPU, and perform operations with random matrices.<br>

# Reshaping data for the 'y=mx' model
X = X.reshape(X.shape[0], 784)<br>
X_test = X_test.reshape(X_test.shape[0], 784)<br>

# Transferring datasets to the GPU
X = GPU_data(X)<br>
Y = GPU_data(Y)<br>
X_test = GPU_data(X_test)<br>
Y_test = GPU_data(Y_test)<br>

# Question Three - Training a Random Walk Model
Here, we transpose the data, create a random matrix, and optimize it to achieve at least 75% accuracy.<br>

# Transposing the data
X = X.T

# Conclusion
This Markdown document outlines the steps and code snippets for solving problem set one in data science mathematics, including loading the MNIST dataset, visualizing images, running a random model, and training a random walk model.


