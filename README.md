# AN INTRODUCTION TO CONVOLUTIONAL NEURAL NETWORKS USING KERAS FOR IMAGE CLASSIFICATION PROBLEMS

Convolutional networks are Deep Learning algorithms that try to solve some of the problems that exist in traditional neural networks. 

![alt text](https://github.com/qgvidal/cnnImageClassification/blob/main/images/cnn1.jpg)

They are generally used for image classification. The problem with traditional neural networks is that when passing an image to be recognized, it is not the same, for example, a face that appears in a position that is slightly rotated or that is brighter than other, when in reality it is the same face (have the same information). Convolutional networks solve this problem. With this type of network, it does not matter if an image is slightly rotated, has more brightness or less, they will learn to recognize it. The objective is that they learn to extract information that can be valuable and that is relevant. In other words, the goal is to extract the characteristics of an image that allow us to classify them correctly.

This type of neural network is being used a lot today. For example, in medicine for the recognition of diseases or in autonomous driving. Self-driving cars recognize the images around them and are able to classify them.

### WHAT IS A CONVOLUTION? WHAT IS IT USED FOR?

In order to be able to extract relevant information in images where the same face is slightly rotated or appears displaced or with a little brightness or any other characteristic that affects the image, convolutional networks incorporate the process of convolution.

Convolution can mathematically be understood as a function that transforms an input signal, an image for example, into a new transformed output signal. What this process does is filter the image and extract descriptive characteristics from the image itself. Each filter is capable of extracting a characteristic from the image, which can be edges, corners, contours, removing noise from the image, etc.

These filters are neither more nor less than matrix that will pass through the different areas of the image, extracting useful characteristics.

![alt text](https://github.com/qgvidal/cnnImageClassification/blob/main/images/cnn2.jpg)

As you can see in the image, the filter goes through all the positions of the pixel matrix making a convolution.

That is, everything is summarized in a product between matrices: the image, which can be translated into a matrix of pixels where each color has a value, and the convolutional filter.

Now, when applying the filter, we see that there is a problem in the corners. There are no edges to be able to do this matrix multiplication, so if we try to make this product, it will give an error. What is done to solve this type of problem is to add the so-called zero-padding, which is nothing more than adding zero around the image matrix that allows us to make the product of matrices.

![alt text](https://github.com/qgvidal/cnnImageClassification/blob/main/images/cnn3.jpg)

As we are extracting information applying successive filters, the result that we are extracting is information with more important characteristics.


### WHAT IS MAX-POOLING?

Another process that is applied in the different layers of the networks is called max-pooling. What max-pooling does is extract, for each of the sub-arrays that we generate from an image, the maximum value of them. For example:
  
![alt text]( https://github.com/qgvidal/cnnImageClassification/blob/main/images/cnn4.jpg)

As you can see in this case, we have managed to reduce a 4x4 image to a 2x2 image. This process allows all of our operations within the network to be much more robust to changes or movements in the image.
