# Color-Detection-Using-CNN

# Description:
This project aims to detect and classify different colors in images using a Convolutional Neural Network (CNN). The dataset used here is secondary and was obtained from Roboflow which contains 1,248 images grouped into 10 color categories (Black, Blue, Green, Brown, Grey, Orange, Red, Violet, White, and Yellow). The trained model accurately classifies images into their respective color categories.

# Methodology:
## Data Collecton
The image dataset was sourced from Roboflow , which provided the data pre-divided into training, testing, and validation subsets across ten color categories: Black, Blue, Green, Brown, Grey, Orange, Red, Violet, White, and Yellow. For simplified processing, all images from these subsets were consolidated into a single folder.

## Data Splitting
The combined dataset (containing 1,248 images) was divided into training and validation. This resulted in 998 images for training and 250 images for validation.

## Data Augmentation
To enhance generalization and minimize overfitting, data augmentation techniques were applied to the training images.

## Model Architecture
A Convolutional Neural Network (CNN) was built using the Keras library. The network looks at each image and learns to recognize the patterns and features of its color. Because each image only has one color, the model’s main task is to match the image to its color category. Convolutional layers help detect important color features, pooling layers reduce the data size, and dense layers decide the most likely color class. Dropout is used to improve reliability. The final layer chooses one color out of the ten possible options.

## Model Evaluation
The CNN was trained on the augmented training data using the Adam optimizer and categorical cross-entropy loss. Model performance was evaluated on both training and validation sets. 

## Results:
The CNN achieved validation accuracy of 97.6% across all 10 color categories. Testing on a new, unseen image confirmed that the trained CNN could accurately identify the dominant color based solely on pixel information. 
