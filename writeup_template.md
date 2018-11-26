# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I applied Gaussian Blur to the
Image withe different kernel size by brute force and finally I selected 5 as a suitable number.

I applied canny as a third step with low and high threshold as 200 and 300 again based on brute force


In order to draw a single line on the left and right lanes, I have written my own draw line function
which fitted the points using linear regression and slope and then I interpolated those lines.

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


There are few shortcomings in my detection algorithm:
1. A lot of brute force is applied which might not get us best solution.
2. Sometimes both lines cross each other.

### 3. Suggest possible improvements to your pipeline
Few improvements I will be working on is:
1. To get better area detection in the image.
2. Better line drawing algorithm.
