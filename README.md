# Classifying images of everyday objects using neural networks
In this notebook, everyday objects like vehicles, animals, birds, etc. have been classified by image processing techniques.
An approach to implement ResNet9 and 18 model architectures on the CIFAR-10 Dataset.  
Dataset Link: [Dataset](https://www.cs.toronto.edu/~kriz/cifar.html)  

## About Dataset
CIFAR-10 consists of 60000 '32X32' color images over 10 classes, each representing some common everyday object, with 6000 images per class.  
In the notebook, the dataset is imported using torchvision from PyTorch.

## Python Libraries/Frameworks used
PyTorch  
Numpy
matplotlib
PIL(Python Imaging Library, for working with Images)

## Notes
1. The dataset has 10 classes and all have equal number of training examples(6000 each). So there is no class imbalance.
2. The model architectures have been defined in separate classes, following the idea of Sequential API.

## Training     
GPU is used for training.  

Some methods used to fasten training processes:  
 
   __Learning Rate Scheduling:__ This is to facilitate changing of the learning rate after each batch of training. Here we implement the "One cycle Learning Rate"     policy, which involves increasing the learning rate for about 30% of epochs and then reducing it.
     
   __Weight Decay:__ This involves regularizing the weights, preventing them from becoming too large by adding an additional term to loss function.

   __Gradient Clipping:__ This involves restricting the gradient values to a small range to avoid undesirable changes in parameters.

## Comparisons
<img src = "https://github.com/kamlesh-ops/CIFAR-10_ResNets/assets/101917668/accfd1ae-9e4d-48a6-a472-e00912cef411" width = "500" heigt = "500">  

The slight abruptness in the curve is possibly due to changing/scheduling learning rate.  

## Loss  
Cross-Entropy Loss, which combines the negative log-likelihood(NLL) loss and log_softmax, is common for classification problems, compared to NLL loss. 
Reference: [Cross_Entropy_Loss](https://pytorch.org/docs/stable/generated/torch.nn.CrossEntropyLoss.html#torch.nn.CrossEntropyLoss)  

## Optimizer
Adam - Converges faster than SGD.

## Accuracy
Around 90% validation accuracy, and 89% test accuracy. 





