# Brain MRI Segmentation using U-Net and Attention U-Net Architecture

## Introduction:

The findings of segmenting MRI images using the U-Net and Attention U-Net designs are shown in this report. Accurately segmenting regions of interest from MRI images is the main objective of this work since it is essential for medical diagnosis and therapy planning.

## Dataset:

The dataset consists of MRI images and their respective segmentation masks. A total of 112 patients' data was processed, with each patient having multiple MRI images and corresponding masks.

Dataset Link: https://www.kaggle.com/datasets/mateuszbuda/lgg-mri-segmentation

## Data Preprocessing:

A structured directory was used to extract and load the dataset.  We read, scaled, and normalized the images and their matching masks.  Techniques for data augmentation were used to enhance generalization.  To ensure uniformity, images were converted from BGR to RGB format.  Pixel values were normalized between 0 and 1 to enhance model convergence.  Normalization scales pixel values, facilitating faster and more stable training.  Binary segmentation masks were thresholded to remove noise and ensure clear region separation.

## Model Architecture:

A convolutional neural network (CNN) architecture called U-Net was created specifically for the segmentation of biological images.  It has an encoder-decoder structure, in which the segmented output is reconstructed by the decoder after the encoder has captured spatial features.  By preserving fine-grained details, skip connections increase the accuracy of segmentation.


## Results:

### U-Net Model:

The accuracy curves for training and validation demonstrate a consistent upward trend, convergent toward nearly flawless segmentation outcomes.  In a similar vein, the loss curve shows a sharp drop before leveling out at a very low value, suggesting that segmentation predictions were made with little mistake.

Accuracy: 99.71%
Loss: 0.78%

![image](https://github.com/user-attachments/assets/28051c7c-afd3-4028-9e1d-704c21614fe0)


The below is the output for the U-Net Model.
First is the original image, second is the ground truth mask, and third is the ordinary U-Net model result.

![image](https://github.com/user-attachments/assets/1541ccb7-0024-41d0-8831-77c8f069b464)


### Attention U-Net Model

Accuracy: 99.71%
Loss: 0.76%

![image](https://github.com/user-attachments/assets/e31b6f4f-91a2-400c-b23d-762db49bed50)


The below are the outputs for the Attention U-Net Model:
First is the original image, second is the ground truth mask, third is the ordinary U-Net model result, and fourth is the Attention U-Net model result.

![image](https://github.com/user-attachments/assets/e95adce3-45b6-4859-a877-a79da784569c)


## Inference:

Attention U-Net demonstrated superior performance, likely due to its ability to focus on relevant regions.
There is no much drastic change in both the accuracy and loss values.




