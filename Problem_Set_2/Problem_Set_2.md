# Problem Set Two - Data Science Math - Holly Darter
This markdown file provides a descriptive overview of the python code for a data science math problem set. The code performs several image processing tasks, and describes each part of the code step by step. 
## Question One - Load an RGB image from a URL
In this section, we start by importing the necessary libraries, including `requests`, `PIL`, `numpy`, `matplotlib`, and `cv2`. We then specify the URL of the image we want to load, use the `requests` library to fetch the image data, and display the image using `matplotlib`.
## Question Two - Resize the image to 224x224 
Here, we resize the loaded image to a 224x224-pixel resolution using the `resize` function from the PIL library and display the resized image.
## Question Three - Show a greyscale copy
In this section, we convert the resized RGB image into grayscale by extracting the first channel (R) and display it using the 'gray' colormap. The axis labels are removed to display a clean grayscale version of the image.
## Question Four - Convolve with 10 random features and show filters and feature maps for each
### Generating 10 random 3x3 filters
First, we generate 10 random 3x3 filters for convolution using numpy's random number generation.
### Applying 3D filters to the color image
We define two functions:
1. `generate_random_3d_filters` - to generate random 3D filters with the specified number of filters, filter size, and depth.
2. `apply_3d_filters` - to apply these 3D filters to the color image and return feature maps.
We then generate 10 random 3D filters and apply them to the resized RGB image. The resulting feature maps are displayed alongside the filters.
### Displaying Filters and Feature Maps
We use matplotlib to create subplots for displaying both the generated filters and the feature maps. For filters, we show each filter individually with its corresponding title, and for feature maps, we display them alongside their titles.<br>
<br>
Overall, this code demonstrates a series of image processing tasks, including loading, resizing, grayscale conversion, and convolution with random filters.
## Extra Credit Question One 
Experiment with at least 4 different ways of turning the image from color to grayscale. Explain the technical and qualitative differences of each approach. Speculate as to why you might prefer some over others for certain tasks. Write and test your own convolution function. Compare it to the prewritten function. Explain the steps.
### Method One - Using The luminosity method computes the grayscale value based on the perceived brightness of each channel (R, G, B) as perceived by the human eye. This method takes into account the differences in how our eyes perceive different colors.
0.21*R + 0.72*G + 0.07*B = The greyscale value <br>
This method would useful if the greyscale image is going to be looked at by a human because it is a closer representation of what the colored image would look like due to how the human eye percieves color. 
### Method Two - The average method takes the average of the red blue and green channels for the greyscale value of each pixel
avg(r,g,b = greyscale value) <br>
This method is useful since it is a simple and straightforward approach. It has the advantage of being able to be completed in a short amount of time, and efficiently. It is best for a quick visual reference. It also gives a uniform greyscale as each color chanel is given equal weight. 
### Method Three - The desaturation method calculates the grayscale value by taking the maximum and minimum of the three colors for each pixel and averaging the max and min.
Greyscale = (max(R,G,B) + min(R,G,B))/2
This method is useful because it preserves color information. Unlike other conversion methods, this method is able to retain some of the original color information. It also in many cases is visually aesthetic, especially when you want to retain a sense of the original image's color. 
### Method Four - Single channel greyscale: only using the values from one of the three channel to create a greyscale image. My code used only the r chanel for the greyscale values. 
greyscale value = r value <br>
The method is also useful when you need faster processing, or if a image is only one color. The other formulas would skew the greyscale image if the color image is only one color because of the 0s in the other chanels. 
