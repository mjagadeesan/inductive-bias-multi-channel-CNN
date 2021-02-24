# Overview
This is the code repository for the following manuscript: "Inductive Bias of Multi-Channel Linear Convolutional Networks with Bounded Weight Norm" (Meena Jagadeesan, Ilya Razenshteyn, Suriya Gunasekar). 

# Paper Abstract
We study the function space characterization of the inductive bias resulting from controlling the  $\ell_2$ norm of the weights in linear convolutional networks. We view this in terms of an induced regularizer in the function space given by the minimum norm of weights required to realize a  linear function. For two layer linear convolutional networks with $C$ output channels and kernel size $K$, we show the following: (a) If the inputs to the network have a single channel, the induced regularizer for any $K$ is a norm given by a semidefinite program (SDP) that is independent of the number of output channels $C$. We further validate these results through a binary classification task on MNIST. (b) In contrast, for networks with multi-channel inputs, multiple output channels can be necessary to merely realize all matrix-valued linear functions and thus the inductive bias does depend on $C$.  Further, for sufficiently large $C$, the induced regularizer for  $K=1$ and $K=D$ are the nuclear norm and the $\ell_{2,1}$ group-sparse norm, respectively, of the Fourier coefficients---both of which promote sparse structures.

# Experiments
The python notebook (code.ipynb) contains experiments to analyze the implicit bias of gradient descent on two-layer linear convolutional neural networks with a single input channel on the MNIST dataset. These experiments mainly serve to validate the theoretical findings in our paper. 

We empirically observe the following two properties: 
1. For larger kernel sizes, the learned predictor would tend to be sparse in Fourier domain, and  
2. The induced regularizer and the learned predictor are fairly invariant to number of output channels. 
3. When there is a ReLU non-linearity, the induced regularizer continues to be fairly invariant to the number of output channels. 
