# A DCGAN in Keras

A keras implementation of a custom Deep Convolutional Generative Adversarial Networks (DCGAN) on MNIST dataset. The code is mainly based on the Francois Chollet's [Deep Learning with Python](https://www.manning.com/books/deep-learning-with-python), page 308.
  
  

## Implementation
#### What worked:
+ Using dropout in the discriminator
+ Adding noise to the labels
+ Using strided convolutions
+ Normalizing the data to [-1, 1]

#### Failures and mistakes:
+ Using high learning rates (>1e-3)
+ I initially normalized the data between 0 and 1, but since I was using "tanh" as the last layer of the generator's output, it made the convergence a lot harder
+ Constructing different mini-batches for real and fake images
+ Training the discriminator more than the generator
+ Using SGD optimizer


  
## Results
Training history (First 5000 iterations):  
  
<img src="visualization/viz1.gif" width="270" />
