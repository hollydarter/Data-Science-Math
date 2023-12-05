Homework 3 Report
Introduction
This Jupyter notebook presents the solution to Homework 3, which involves fine-tuning the AlexNet model on the Flowers 102 dataset. The main tasks include importing necessary libraries, defining utility functions for plotting tensors and training models, downloading and extracting the dataset, and finally, training the AlexNet model.

Importing Libraries and Modules
The notebook begins by importing the required libraries and modules. This includes popular deep learning libraries such as NumPy, PIL (Python Imaging Library), imageio, scikit-image, Matplotlib, PyTorch, and torchvision. Additionally, utility functions from skimage, scipy, and torchsummary are imported for specific tasks.

Utility Functions
1. plot(x, title=None)
This function is designed to plot a tensor using Matplotlib. It converts the input tensor to a NumPy array, transposes it if necessary, and displays the image using Matplotlib. Grayscale images are handled by squeezing the color channel and clipping values to the valid range [0, 1].

2. plot2(x)
This function displays a tensor or NumPy array as a grayscale image using Matplotlib. If the input is a PyTorch tensor, it is first converted to a NumPy array before displaying.

3. train_model(model, num_epochs=10)
This function trains a PyTorch model using the specified number of epochs. It utilizes the CrossEntropyLoss as the loss function and Stochastic Gradient Descent (SGD) as the optimizer. The training loop includes both training and validation phases, and the learning rate is adjusted using a stepwise decay.

Dataset Download and Preparation
The notebook proceeds with downloading and extracting the Flowers 102 dataset. The dataset is then prepared by defining transformations, such as resizing, cropping, and normalizing images, for both training and validation datasets.

Model Definition
The AlexNet model is chosen for fine-tuning. It is loaded with pre-trained weights and moved to the GPU if available.

Exploratory Data Analysis
Several images from the training dataset are randomly selected and plotted alongside their labels, providing a visual understanding of the dataset.

Model Fine-Tuning
The AlexNet model is fine-tuned on the Flowers 102 dataset for a specified number of epochs (in this case, 10 epochs). The training progress is printed for each epoch, including training and validation accuracy.

Conclusion
This detailed report outlines the steps taken in the Jupyter notebook to fine-tune the AlexNet model on the Flowers 102 dataset. The code is structured and includes comments to explain each section. The notebook provides a comprehensive solution to the specified homework tasks.




