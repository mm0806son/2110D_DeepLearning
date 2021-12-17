# 2110D_DeepLearning

Course UE D-Deep Learning at IMT Atlantique

Made by:

- David HURTADO @[dr-hurtado](https://github.com/dr-hurtado)
- Zijie NING @[mm0806son](https://github.com/mm0806son)

<img src="https://raw.githubusercontent.com/mm0806son/2110D_DeepLearning/main/Projet/RT-multiperson-pose-pytorch/readme/Authors_skeleton.png?token=ART4NBIMLPOXDNFSVXSWW43BWXDSU" style="zoom:50%;" />

## Project

Thesis Reproduction and application: [Realtime Multi-Person 2D Pose Estimation using Part Affinity Fields](https://arxiv.org/abs/1611.08050)

**Main Activities:**

- Read the paper to understand the mathematical principles and network structure.
- Read the code and understand the main functions.
- Development of new applications based on experimental conditions.

**Our own applications:**

- Processing of single images

  - Body joint confidence map

  <img src="https://raw.githubusercontent.com/mm0806son/2110D_DeepLearning/main/Projet/RT-multiperson-pose-pytorch/readme/Authors_heatmap.png?token=ART4NBOQM2BIUI5AGD5AIDTBWXEHY" alt="Heatmap" style="zoom: 50%;" />

  - Part Affinity Fields (PAFs)

    <img src="https://raw.githubusercontent.com/mm0806son/2110D_DeepLearning/main/Projet/RT-multiperson-pose-pytorch/readme/Authors_Paf.png?token=ART4NBKHYRX2MYWGGX43M3DBWXEN6" style="zoom: 50%;" />

  - Generated body skeleton

    <img src="https://raw.githubusercontent.com/mm0806son/2110D_DeepLearning/main/Projet/RT-multiperson-pose-pytorch/readme/Authors_skeleton_nobg.png?token=ART4NBMIHFUDVHEAJZRQLUTBWXEVU" style="zoom:50%;" />

- Processing [video](https://github.com/mm0806son/2110D_DeepLearning/raw/main/Projet/RT-multiperson-pose-pytorch/readme/Authors_v2_result.mp4)

- Use Google Colab to call a local webcam and process the images

- Layer visualization to see what happened in the network

  - For example, after the preprocessing network (here model0, first 10 layers of vgg19)

    ![](https://raw.githubusercontent.com/mm0806son/2110D_DeepLearning/main/Projet/layer_visualization/model0.jpeg?token=ART4NBM45FIXXLDFYWPTDDDBWXFAY)

  - 3rd stage of PAFs branch (model3_2, first 20 output)

    ![](https://raw.githubusercontent.com/mm0806son/2110D_DeepLearning/main/Projet/layer_visualization/model3_1.png?token=ART4NBLGF65LH5MM5NHWR3LBWXFMO)

  - 3rd stage of confidence map branch (model3_2)

    ![](https://raw.githubusercontent.com/mm0806son/2110D_DeepLearning/main/Projet/layer_visualization/model3_2.png?token=ART4NBITFT3ITJKO3HLIXCDBWXFPW)

- Use Google Colab to call a local webcam and process the video (TODO)

- Control of a robot simulator using `pybullet ` (TODO)

## TP1-2

2021/10/01 & 08

Introduction to PyTorch

- Linear regression
- Logistique regression

## TP3

2021/10/15

Multi-Layer Perception with MNIST dataset

- Build a 2-layer Neuro network
- Evolution of the loss function for both **training** and **validation sets**

<img src="https://raw.githubusercontent.com/mm0806son/Images/main/202110221431226.png" style="zoom:50%;" />

## TP4

2021/10/15

Convolutional Neural Networks (CNN) on MNIST

- Create data loaders
- Build and train a CNN network

## TP5

2021/10/29 Graded session

Fashion-MNIST dataset

- Data loader

- MLP

- CNN

- Transfer learning with vgg-16

  **Accuracy: 93.71%**  (1st in the class :v:)

  Pretrained VGG16 with lr = 0.01, epoch = 7, 
  Normalize((0.485, 0.456, 0.406), (0.229, 0.224, 0.225))

## TP6

2021/11/12 Graded session

Recurrent Neural Networks (RNN) on the the **Lorenz-63 system** (chaos system)
