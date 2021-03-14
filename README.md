# GCRNet
***

GCRNet is a fragments reassmebly framework based on graph generation strategy and deep learning method. This model concentrates more on the prediction of pairwise matches. The following image is the whole process of the algorithim.

![image](https://github.com/wmhwmh521/GCRNet/blob/main/1.png)


## 1.environment
***

Our model is implemented on the Ubuntu16.04 and RTX-2080TI. We use pytorch(CUDA version) to build the module and run the experiments. If you want to run the codes mentioned in this project, these additional packages are needed:
- python3.6
- pytorch'1.6.0'
- opencv'3.4.2'

## 2.datases
***

In our comparative experiment we use the magazine dataset set up by richer, MIT and BGU datasets. You can download these datasets here 
- [MIT](https://drive.google.com/file/d/13bW2Vpt79F8vuhWvu6NxLIf4FNovg5oz/view?usp=sharing)
- [BGU](https://drive.google.com/file/d/1TT2ghgOw_CSQtvwSlw7z5p6YXBSiItRZ/view?usp=sharing)
- [Rither-magazine](https://drive.google.com/file/d/1rjbOK2qTKAnmEaMTQZ1jkEM5kDdVyfg4/view?usp=sharing)

## 3.structure
***

- GCRNet

GCRNet is the proposed model in our paper. Ii is composed of CNN and RNN modules. All the coresponding functions are collected in this file, such as the preprocessd operation，the architecture of each module and the training process.

- Contrast experiment and robust experiment

Contrast experiment and robust experiment are all additional experiments to exam the ability of the model. These files describe the experiments on other datasets and the results of RNN module with classical descriptors.

## 4.Run the codes 
***

If you have downloaded all datasets and ensure that the path in GCRNet or other files are correct, just run the codes. The training process and the testing process are performed iteratively. In each epoch the results wiil be performed on the window. if you want to run your own data, you have to down load the magazine datasets to train the model for a while and run the evaluate function with corresponding parameters. The final result is an adjacency matrix which indicates the relationship of fragments.

- GCRNet

Fragement Graph_RNN.ipynb is the standard model tested on magazine datasets and other public datasets.

- Ablation Experiment

4resnet.ipynb is the Ablation Experiment tested magazine datasets. The container of residual blocks is reduced one by one.

- Robustness Experiment

NEW_compare.ipynb is the comparable experiments on different artifical descriptors and datasets. It concludes the Robustness Experiment of partially missing image and multi-image reconstruction tasks. The largest reconstruction task consists of 128 shredded pieces.

![image](https://github.com/wmhwmh521/GCRNet/blob/main/128.jpg)
