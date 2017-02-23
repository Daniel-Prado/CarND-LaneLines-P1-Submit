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

1. Convert the input image to grayscale using the provided helper function that performs a `COLOR_RGB2GRAY` conversion. I have also experimented with the Intensity component of the HSI colorspace, which is referred to be more optimal in computer vision but I really haven't observed a difference.

2. second step

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

