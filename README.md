# csci8360-p3-tooYoungTooSimple

#  CIFAR-10 Image Classification with Deep Residual Networks on Torch

This is project 3 in CSCI 8360 course at University of Georgia, Spring 2016. In this project we were challenged to predict the class labels of the test set from CIFAR-10 image dataset with 10 different labeled categories. The dataset consist of 60,000 PNG images with 50,000 in the training set and 10,000 in the test set. We conducted a number of manipulations on the data and applied the Deep Residual Networks with 200 layers by Kaiming He to train the classification model. In the end, the model achieves 92.51% prediction accuracy in the test set.

## Getting Started

Here are the instructions to run the ?lua scripts with torch locally on Mac OS or Linux, if one wants to run this code in Amazon AWS EMR, be sure to change the data path.

### The data
There are in total 10 category labels for each of the images, which are airplane, automobile, bird, cat, deer, dog, frog, horse, ship and truck. Each of the files is a PNG image with 32*32 pixels and three color channels: standard RGB format.
Lists of documents in the train set and test set as well as labels of training documents are provided in the following files:

```
X_small_train.txt, y_small_train.txt
X_small_test.txt, y_small_test.txt
X_train.txt, y_train.txt
X_test.txt
```

### Installing

Install Torch on Ubuntu 14.04 Amazon EC2 GPU Instances with CUDA GPU as below,

```
git clone https://github.com/torch/distro.git ~/torch --recursive
```

Install cuDNN v4 or v5 and the Torch bindings
```
wget "https://developer.nvidia.com/cuda-downloads"
wget https://codeload.github.com/brotchie/torch-ubuntu-gpu-ec2-install/zip/master
sudo dpkg -i cuda-repo-ubuntu1404_7.5-18_amd64.deb

# Run the torche easy one-line install. This will install the cuda accelerated
# tensor and neural net lua packages.
curl -s https://raw.githubusercontent.com/torch/ezinstall/master/install-all | bash
```


## Procedure
There are two parts in this project: data manipulation and model training.  
###Data Manipulation
We consider  the train and test data:

1. ;
2. ;
3. ;
4. 

###Model Training
* .
* We apply  .
* For the idea of Deep Residual Networks, please look at the paper "Identity Mappings in Deep Residual Networks" (http://arxiv.org/abs/1603.05027) for details.

###Prediction

Conducting classification on the test set by the above model, we achieve classification accuracy 92.51%.


## Running
To run the code, be sure change the data path and install all dependent lua modules, and run with  command simply as below,

```
th main.lua -netType residual-nn-pre -depth 1001 -batchSize 64 -nGPU 2 -nThreads 4 -dataset cifar10 -nEpochs 200 -shareGradInput false




```

## Authors

* **[Xiaodong Jiang](https://www.linkedin.com/in/xiaodongjiang)** - Ph.D. Student, *Department of Statistics*
* **[Yang Song](https://www.linkedin.com/in/yang-song-74298a118/en)** - M.S. Student, *Department of Statistics*
* **[Yaotong Cai](https://www.linkedin.com/in/yaotong-colin-cai-410ab026)** - Ph.D. Candidate, *Department of Statistics*

## Acknowledgments

* Thanks all team members for the laborious work and great collaboration.
* Thanks [Dr. Quinn](http://cobweb.cs.uga.edu/~squinn/), .
