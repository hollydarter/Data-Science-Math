# Wardrobe Wizard Project - MAP 2192 - Holly Darter

## Introduction

This repository contains code for the Wardrobe Wizard Project developed for MAP 2192 by Holly Darter. The project involves tasks related to image processing, deep learning, and experiment tracking.

## Setup

### Libraries and Tools Installation

Make sure to install the necessary libraries and tools before running the code. Use the following commands:

```
%%capture
!pip install wandb
!apt-get install poppler-utils
!pip install pdf2image
!pip install flashtorch

```
## Python Libraries and Tools

- **wandb**: Experiment tracking library.
- **poppler-utils**: Utilities for working with PDF files.
- **pdf2image**: Library for converting PDFs to images.
- **flashtorch**: Tool for visualizing PyTorch models.

## Code Overview

### GPU Setup

- Determine the device (GPU if available, otherwise CPU).
- Define functions for creating GPU tensors with and without gradient tracking.

### Image and PDF Handling

- Download and convert images from a Google Slides presentation URL.
- Load and preprocess images with PyTorch transformations.
- Retrieve labels from a JSON file hosted on Amazon S3.
## Deep Learning Model

- Instantiate an AlexNet model with pre-trained weights.
- Perform a forward pass of images through the model to obtain predictions.
- Extract class indices with the highest predicted probability for each image.

### Data Manipulation

- Generate predictions, extract class indices, and print corresponding labels.
- Create and manipulate NumPy arrays.
- Convert NumPy arrays to GPU tensors.

### Model Training

- Define a softmax function and a cross-entropy loss function.
- Define functions for generating truncated normal random numbers.
- Implement a simple linear model and set up the training loop using the Adam optimizer.
- Log training accuracy and loss using Weights and Biases (WandB).
- 
## Usage

1. Install the required libraries and tools.
2. Run the provided code sections in a Jupyter Notebook or a Python script.
3. Ensure that configuration parameters, such as learning rate, batch size, and epochs, are appropriately set.

## Results

The code outputs training accuracy and loss using Weights and Biases (WandB) experiment tracking.

Feel free to reach out if you have any questions or need further clarification.
