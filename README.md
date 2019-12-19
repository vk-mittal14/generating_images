# Image Generation
This repository contains different methods for generating new images.

### Image Generation Using Multivariate Gaussian Distribution 
We can make our model to generate new images by learning a multivariate gaussian distribution, the parameters for the model that are mean and covariance will be same as the mean of the data for that class and covariance of the data. <br>
I trained my model on MNIST digit data. The code can be found in [bayes.py](https://github.com/i-m-vivek/generating_images/blob/master/bayes.py).


![Bayes Generated Images](https://github.com/i-m-vivek/generating_images/blob/master/images/Bayes_Gen/generated_image-40000.png)
First Row is the mean of the images over the dataset & the second row represents the image created by multivariat gaussian distribution.<br>

### Image Generation Using Gaussian Mixture 
Code for Gaussian Mixture can be found in [bayes_classifier_gmm-mnist.py](https://github.com/i-m-vivek/generating_images/blob/master/bayes_classifier_gmm-mnist.py).
![Gaussian Mixture Generated Images](https://github.com/i-m-vivek/generating_images/blob/master/images/gmm_images/generated_image.png)

### Image Generation Using Autoencoder with the use of Guassian Mixture 
Follow this [link](https://colab.research.google.com/drive/1-51-quUrtDcXyVrNRkEg7imb0NrLdo9r) to play with the code.


![Gaussian Mixture With AE](https://github.com/i-m-vivek/generating_images/blob/master/images/gmm-bayes/decoded-9.png)
The first row presents the image generated by my gaussian mixture & the second row represents the image created by decoder by passing the generated images in it.<br>

__How it Works?__ <br> 
* Firstly, I made a model that is same as the Gaussian Mixture used in the section 2 then I trained a Autoencoder to map MNIST images to MNIST images. 
* I fed the image that I got from the Gaussian Mixture in the decoder of the model after that I got a decoded image that is the final output.
