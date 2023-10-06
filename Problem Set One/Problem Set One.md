# Problem Set One - Data Science Math

# Introduction
This Markdown document outlines a problem set in data science mathematics, including loading the MNIST dataset, visualizing images, and running a random model on MNIST.

# Question One - Load MNIST and Display Montage
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

# Code for creating and displaying montages
def plot(x):<br>
    # Plot images<br>
    fig, ax = plt.subplots()<br>
    im = ax.imshow(x, cmap='gray')<br>
    ax.axis('off')<br>
    fig.set_size_inches(7, 7)<br>
    plt.show()<br>

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

# Question Two - Running a Random Model (y=mx) on MNIST<br>
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

#  First, initialize variables for the best matrix 'm_best' and its accuracy 'acc_best'
m_best = 0 <br>
acc_best = 0

# Perform an optimization loop for a set number of iterations (100,000 times)
for i in range(100000):

# Next: 
Set the step size for random updates <br>
    Create a random matrix 'm_random' and move it to the GPU <br>
    Update the matrix 'm' with a small random change, <br>
    Calculate predictions 'y' by multiplying 'm' with the dataset 'X'<br>
    Find the index with the highest value along axis 0 in 'y'<br>
    Calculate accuracy by comparing 'y' with the true labels 'Y'<br>

### Finally, If the new accuracy is better than the previous best, update 'm_best' and 'acc_best'.

# Conclusion
This Markdown document outlines the steps and code snippets for solving problem set one in data science mathematics, including loading the MNIST dataset, visualizing images, running a random model, and training a random walk model.


