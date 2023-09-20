### How to make a random greyscale image in numpy - 9.15

To create a random grayscale image and display it using Matplotlib, you can follow these steps:

### Import the necessary libraries:

import numpy as np
import matplotlib.pyplot as plt

### Generate random grayscale pixel values. You can use numpy to create a random array of integers within the grayscale range (typically 0 to 255):

# Define the dimensions of your image (e.g., 100x100)

width, height = 100, 100

# Generate random grayscale pixel values

random_grayscale_image = np.random.randint(0, 256, (height, width), dtype=np.uint8)

Here, we use np.random.randint to generate random integers between 0 and 255, and we specify dtype=np.uint8 to ensure the values are within the valid range for grayscale pixel values.

### Display the image using Matplotlib:

# Create a Matplotlib figure and axis

plt.figure(figsize=(6, 6))
plt.axis('off')  # Hide the axis

# Display the random grayscale image using Matplotlib's imshow

plt.imshow(random_grayscale_image, cmap='gray', vmin=0, vmax=255)

# Show the plot

plt.show()

### In the code above:

We create a Matplotlib figure and set the size with plt.figure(figsize=(6, 6)).
We hide the axis with plt.axis('off') for a cleaner image display.
We use plt.imshow to display the random grayscale image. We specify cmap='gray' to ensure it's displayed as grayscale.
We set vmin and vmax to 0 and 255 to ensure the colormap's full range is used for grayscale.
Now, when you run this code, it will generate a random grayscale image and display it using Matplotlib. You can adjust the dimensions (width and height) to change the size of the image, and you can modify other parameters to customize the display further if needed.
