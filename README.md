# GCRNet
***

GCRNet is a fragments reassmebly framework based on graph generation strategy and deep learning method. This model concentrates more on the prediction of pairwise matches. The following image is the whole process of the algorithim.

![image](https://github.com/wmhwmh521/GCRNet/blob/main/1.png)

## 1.environment
***

Our model is implemented on the Ubuntu16.04 and RTX-2080TI. We use pytorch(CUDA version) to build the module and run the experiments. If you want to run the codes mentioned in this project, these additional packages are needed:
- python3.6
- pytorch
- opencv
- py

## 2.datases
***

In our comparative experiment we use the magazine dataset set up by richer, MIT and BGU datasets. You can download these data here.

## 3.structure
***

- GCRNet

GCRNet is the proposed model in our paper. Ii is composed of CNN and RNN modules. All the coresponding functions are collected in this file, such as the preprocessd operation，the architecture of each module and the training process.

- Contrast experiment and robust experiment

Contrast experiment and robust experiment are all additional experiments to exam the ability of the model. These files describe the experiments on other datasets and the results of RNN module with classical descriptors.

## 4.Run the codes 
***

If you have downloaded all datasets and ensure that the path in GCRNet or other files are correct, just run the codes. The training process and the testing process are performed iteratively. In each epoch the results wiil be performed on the window. if you want to run your own data, you have to down load the magazine datasets to train the model for a while and run the evaluate function with corresponding parameters. The final result is an adjacency matrix which indicates the relationship of fragments.
