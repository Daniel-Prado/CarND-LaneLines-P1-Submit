#**Finding Lane Lines on the Road** 
## by Daniel Prado-Rodriguez,  February Cohort, 2/22/2017

---

**Finding Lane Lines on the Road - Introduction**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road from input images or video sequences.
* Describe and reflect on your work in this written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### My Finding Lanes pipeline description

My pipeline consists of the following steps:

1. Convert the input image to grayscale using the provided helper function that performs a `COLOR_RGB2GRAY` conversion.
I have also experimented with the Intensity component of the HSI colorspace, which is referred to be more optimal in computer vision but I really haven't observed a difference.

2. Apply a Gaussian filter to soften the image and avoid noise. I have used a kernel size of 3 that seems enough for the purpose.
3. Then, using the provided function based on the Canny Edges algorithm, we detect the edges of the shapes contained in the image, including (but not only) the road lines. The parameters used have been a (low, high) threshold of values (50,150), that seems to provide enough level of detail and not too much clutter.
Here is a sample resulting image:
  IMAGE_REF
4. Next, we apply a mask to the edges image to focus only on the area where the lane lines can be present, and setting the rest to black. The are chosen is a trapezoid polygon, with bottom vertices in the corners of the image and top vertices aproximately in the horizon of the road, 10% of the image width.
5. Next, we apply the Hough Transform to detect the lines in the edges image, using the provided helper function `hough_lines`. This function performs two steps:
- Apply the transform
- Draw the lines in top of the image, in red color.

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I .... 

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


###2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


###3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...

