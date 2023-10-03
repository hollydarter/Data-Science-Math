# Import necessary libraries
import tensorflow as tf  # For machine learning tasks
import matplotlib.pyplot as plt  # For data visualization

# Load the MNIST dataset
mnist = tf.keras.datasets.mnist

# Split the dataset into training and testing sets
(x_train, y_train), (x_test, y_test) = mnist.load_data()

# Create a new figure (plot) with a specified size of 10x10 inches
plt.figure(figsize=(10, 10))

# Display a montage of the first 25 images in the training set
for i in range(25):
    # Create a subplot within a 5x5 grid; i + 1 selects the current subplot
    plt.subplot(5, 5, i + 1)

    # Display the current image from the training set using a grayscale colormap
    plt.imshow(x_train[i], cmap='gray')

    # Set the title of the subplot to the corresponding label from the training set
    plt.title(f"Label: {y_train[i]}")

    # Turn off the axis (axis labels and ticks) for cleaner visualization
    plt.axis('off')

# Adjust the layout of subplots for better spacing
plt.tight_layout()

# Display the entire montage of 25 images
plt.show()

# Import the NumPy library for numerical operations
import numpy as np

# Flatten the images: Reshape the training and testing image data from 2D (28x28) to 1D arrays (784 elements each)
x_train_flat = x_train.reshape(-1, 28 * 28)
x_test_flat = x_test.reshape(-1, 28 * 28)

# Define a simple linear model: Create a random weight vector with 784 elements (one for each pixel)
m = np.random.rand(784)

# Make predictions using the linear model: Calculate the dot product of the flattened training data and the random weight vector
y_pred = np.dot(x_train_flat, m)

# Define a random walk model: Randomly assign a label (0-9) as a prediction
def random_walk_predict(data):
    predictions = []
    for i in range(len(data)):
        prediction = random.randint(0, 9)
        predictions.append(prediction)
    return predictions

# Use the random walk model to make predictions
y_pred_random_walk = random_walk_predict(x_test_flat)
