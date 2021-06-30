# Overview
This is the code repository for the following manuscript: ["Inductive Bias of Multi-Channel Linear Convolutional Networks with Bounded Weight Norm"](https://arxiv.org/abs/2102.12238) (Meena Jagadeesan, Ilya Razenshteyn, Suriya Gunasekar). 

# Paper Abstract
We study the function space characterization of the inductive bias resulting from controlling the $\ell_2$ norm of the weights in linear convolutional networks. We view this in terms of an induced regularizer in the function space given by the minimum norm of weights required to realize a linear function. For two layer linear convolutional networks with C output channels and kernel size K, we show the following: (a) If the inputs to the network have a single channel, the induced regularizer for any K is a norm given by a semidefinite program (SDP) that is independent of the number of output channels C. (b) In contrast, for networks with multi-channel inputs, multiple output channels can be necessary to merely realize all matrix-valued linear functions and thus the inductive bias does depend on C. Further, for sufficiently large C, the induced regularizer for K=1 and K=D are the nuclear norm and the $\ell_{2,1}$ group-sparse norm, respectively, of the Fourier coefficients. (c) Complementing our theoretical results, we show through experiments on MNIST and CIFAR-10 that our key findings extend to implicit biases from gradient descent in overparameterized networks.

# Experiments
The experiments on the MNIST dataset for (linear) convolutional neural networks with a single channel inputs can be found in `single-input-channel/`. 
The experiments on the CIFAR-10 dataset for (linear) convolutional neural networks with a 3-channel inputs can be found in `multi-input-channel/`. 
## Experiments on MNIST
- `single-input-channel/generate_data.ipynb`: code to generate sample of MNIST dataset for binary classification task for linear convolutional neural network experiments
- `single-input-channel/generate_data_nonlinear.ipynb`: code to generate sample of MNIST dataset for binary classification task for nonlinear convolutional neural network experiments
- `single-input-channel/training-test-data/': folder that contains generated samples of MNIST dataset
- `single-input-channel/train-network.ipynb`: code to train the linear convolutional neural network using gradient descent
- `single-input-channel/train-network-nonlinear-bias.ipynb`: code to train a simple nonlinear convolutional neural network with bias parameters using gradient descent
- `single-input-channel/train-network-nonlinear-no-bias.ipynb`: code to train a simple nonlinear convolutional neural network with no bias parameters using gradient descent
- `single-input-channel/train-network-augmented.ipynb`: code to train the linear convolutional neural network using gradient descent for augmented 112x112 images
- `single-input-channel/cvxpy.ipyb`: code to explicitly compute induced regularizer in special cases using CVXPY
- `single-input-channel/plotting.ipynb`: plotting code

## Experiments on CIFAR-10
- `multi-input-channel/generate_training_data.ipynb`: code to generate sample of CIFAR-10 dataset for binary classification task for linear convolutional neural network experiments
- `multi-input-channel/training-test-data/`: folder that contains generated samples of MNIST dataset
- `multi-input-channel/train-network-cifar.ipynb`: code to train the linear convolutional neural network using gradient descent
- `multi-input-channel/cvxpy.ipyb`: code to explicitly compute induced regularizer in special cases using CVXPY
- `multi-input-channel/plotting_cifar.ipynb`: plotting code

