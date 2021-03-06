
# Self-supervised Video Prediction Project

This project architecture model is inspired https://arxiv.org/abs/1612.01756, and http://www.ais.uni-bonn.de/WS2021/LabVision/Project/winner2019.pdf

We use the DSSIM and L2 loss for training. We use three seed frames and predict the next three frames in an autoregressive manner:

<ul>
<li> Input: GT0 Discard output </li> 
<li> Input: GT1 Discard output </li>  
<li> Input: GT2 Output should be Pred0 (calculate the loss between Pred0 and GT3) </li>  
<li> Input: Pred0 Output should be Pred1 (calculate the loss between Pred1 and GT4) </li>  
<li> Input: Pred1 Output should be Pred2 (calculate the loss between Pred2 and GT5) </li> 
</ul>

The results of the model on the Moving MNIST testing dataset (http://www.cs.toronto.edu/~nitish/unsupervised_video/) can be seen below :

![mmistCombined](https://user-images.githubusercontent.com/8552260/116861158-f5e0e200-ac02-11eb-8f67-92f01b8ac1c1.png)


Results on a customized Robot dataset (created from scratch from youtube videos) are visible below:

![robots_combined (1)](https://user-images.githubusercontent.com/8552260/116861856-1e1d1080-ac04-11eb-9eb9-5ef0ae463e13.png)


# Other Deep Learning models 
DL algorithms implemented using Pytorch (on CUDA GPUs):

List of algorithms:
<ul>
<li> Multi Layer Neural Network </li>
<li> Convolution Neural Networks </li>
<li> WandB implementation for Hyperparameter Sweeps </li>
<li> Convolutions on customzied Robot dataset </li>
<li> Variational Convolutional Autoencoders </li>
<li> LSTM and GRU</li>
<li> DCGAN </li>
<li> WGAN </li>
</ul>
