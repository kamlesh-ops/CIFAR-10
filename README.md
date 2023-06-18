# Classifying images of everyday objects using neural networks
In this notebook, everyday objects like vehicles, animals, birds, etc. have been classified by image processing techniques.
An approach to implement ResNet9 and 18 model architectures on the CIFAR-10 Dataset.   

## About Dataset
CIFAR-10 consists of 60000 '32X32' color images over 10 classes, each representing some common everyday object, with 6000 images per class.  
In the notebook, the dataset is imported using torchvision from PyTorch.

## Python Libraries/Frameworks used
PyTorch  
Numpy
matplotlib
PIL(Python Imaging Library, for working with Images)

## Notes
1. The dataset has 10 classes and all have equal number of training examples(6000 each). So there is no 

## Training     
GPU is used for training.  

Some methods used to fasten training processes:  
 
   __Learning Rate Scheduling:__ This is to facilitate changing of the learning rate after each batch of training. Here we implement the "One cycle Learning Rate"     policy, which involves increasing the learning rate for about 30% of epochs and then reducing it.
     
   __Weight Decay:__ This involves regularizing the weights, preventing them from becoming too large by adding an additional term to loss function.

   __Gradient Clipping:__ This involves restricting the gradient values to a small range to avoid undesirable changes in parameters.





