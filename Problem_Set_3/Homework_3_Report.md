# Homework 3 Report

## Introduction

This Jupyter notebook presents the solution to Homework 3, which involves fine-tuning the AlexNet model on the Flowers 102 dataset. The main tasks include importing necessary libraries, defining utility functions for plotting tensors and training models, downloading and extracting the dataset, and finally, training the AlexNet model.

## Importing Libraries and Modules

The notebook begins by importing the required libraries and modules. This includes popular deep learning libraries such as NumPy, PIL (Python Imaging Library), imageio, scikit-image, Matplotlib, PyTorch, and torchvision. Additionally, utility functions from skimage, scipy, and torchsummary are imported for specific tasks.

## Utility Functions

### 1. `plot(x, title=None)`

This function is designed to plot a tensor using Matplotlib. It converts the input tensor to a NumPy array, transposes it if necessary, and displays the image using Matplotlib. Grayscale images are handled by squeezing the color channel and clipping values to the valid range [0, 1].

### 2. `plot2(x)`

This function displays a tensor or NumPy array as a grayscale image using Matplotlib. If the input is a PyTorch tensor, it is first converted to a NumPy array before displaying.

### 3. `train_model(model, num_epochs=10)`

This function trains a PyTorch model using the specified number of epochs. It utilizes the CrossEntropyLoss as the loss function and Stochastic Gradient Descent (SGD) as the optimizer. The training loop includes both training and validation phases, and the learning rate is adjusted using a stepwise decay.

## Dataset Download and Preparation

The notebook proceeds with downloading and extracting the Flowers 102 dataset. The dataset is then prepared by defining transformations, such as resizing, cropping, and normalizing images, for both training and validation datasets.

## Model Definition

The AlexNet model is chosen for fine-tuning. It is loaded with pre-trained weights and moved to the GPU if available.

## Exploratory Data Analysis

Several images from the training dataset are randomly selected and plotted alongside their labels, providing a visual understanding of the dataset.

## Model Fine-Tuning

The AlexNet model is fine-tuned on the Flowers 102 dataset for a specified number of epochs (in this case, 10 epochs). The training progress is printed for each epoch, including training and validation accuracy.

### Training Results

| Epoch | Train Accuracy | Valid Accuracy |
|-------|----------------|----------------|
| 1     | 0.12           | 0.26           |
| 2     | 0.31           | 0.50           |
| 3     | 0.45           | 0.59           |
| 4     | 0.53           | 0.70           |
| 5     | 0.58           | 0.70           |
| 6     | 0.60           | 0.73           |
| 7     | 0.64           | 0.75           |
| 8     | 0.77           | 0.87           |
| 9     | 0.81           | 0.88           |
| 10    | 0.82           | 0.89           |

## Conclusion

This detailed report outlines the steps taken in the Jupyter notebook to fine-tune the AlexNet model on the Flowers 102 dataset. The code is structured and includes comments to explain each section. The notebook provides a comprehensive solution to the specified homework tasks.

[Link to Colab Notebook](https://colab.research.google.com/drive/17AVcW3HjujBEp0VhElI3qhc5jTprf3pO#scrollTo=CnwbXfcisVyA)
