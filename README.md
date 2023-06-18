# CIFAR-10 implementation using ResNets

An approach to implement ResNet9 and 18 model architectures on the CIFAR-10 Dataset.  

## About Dataset
CIFAR-10 consists of 60000 32X32 colour images in 10 classes, with 6000 images per class.  
In the notebook, the dataset is imported using torchvision from pyTorch.

## Training     
GPU is used for training.  
Some methods used to fasten training processes:  
 
   __Learning Rate Scheduling:__ This is to facilitate changing of the learning rate after each batch of training. Here we implement the "One cycle Learning Rate"     policy, which involves increasing the learning rate for about 30% of epochs and then reducing it.
     
   __Weight Decay:__ This involves regularizing the weights, preventing them from becoming too large by adding an additional term to loss function.

   __Gradient Clipping:__ This involves restricting the gradient values to a small range to avoid undesirable changes in parameters.




