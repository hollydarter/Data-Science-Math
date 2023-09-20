### matplotlib Notes - 9.15
 
 Matplotlib is a popular Python library for creating static, animated, and interactive visualizations in a wide variety of formats. It provides a flexible and powerful way to generate plots, charts, and graphs. Here's a beginner's guide to using Matplotlib:

### Installing Matplotlib:

If you haven't already installed Matplotlib, you can do so using pip:

pip install matplotlib
Importing Matplotlib:

### Import Matplotlib's main module:

import matplotlib.pyplot as plt

The conventional alias for matplotlib.pyplot is plt, which makes the code shorter and easier to read.

### Creating a Simple Plot:

You can create a basic line plot with Matplotlib by providing data to the plot() function:

x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]
plt.plot(x, y)
plt.show()

The plt.show() command is necessary to display the plot.

### Customizing the Plot:

You can customize various aspects of the plot, such as labels, titles, and colors:

plt.plot(x, y, label='Linear Function', color='blue', linestyle='--', marker='o')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.title('Simple Plot Example')
plt.legend()
plt.grid(True)
plt.show()

### Creating Different Types of Plots:

Matplotlib supports various plot types, including scatter plots, bar charts, histograms, and more. Here's an example of a scatter plot:

x = [1, 2, 3, 4, 5]
y = [2, 4, 1, 3, 5]
plt.scatter(x, y, label='Scatter Plot', color='red', marker='o')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.title('Scatter Plot Example')
plt.legend()
plt.grid(True)
plt.show()

### Subplots:

You can create multiple plots within the same figure using subplots:

x = [1, 2, 3, 4, 5]
y1 = [2, 4, 6, 8, 10]
y2 = [1, 4, 9, 16, 25]
plt.figure(figsize=(10, 4))  # Set the figure size
plt.subplot(1, 2, 1)  # Create the first subplot
plt.plot(x, y1, label='Linear Function', color='blue')
plt.title('Subplot 1')
plt.subplot(1, 2, 2)  # Create the second subplot
plt.plot(x, y2, label='Square Function', color='green')
plt.title('Subplot 2')
plt.tight_layout()  # Adjust subplot layout
plt.show()

### Saving Plots:

You can save your plots to various file formats like PNG, PDF, or SVG using savefig():

plt.savefig('my_plot.png')

This saves the current plot to a file named 'my_plot.png' in the current working directory.
