Emotion Recognition Model with Keras


This repository contains a Convolutional Neural Network (CNN) model implemented using Keras for emotion recognition from grayscale images. The model is designed to classify images into one of seven emotion categories.

Features

Convolutional Layers: Extract spatial features from input images using multiple Conv2D layers.

Batch Normalization: Improve training stability and convergence speed.

Dropout Layers: Prevent overfitting by randomly deactivating neurons during training.

MaxPooling Layers: Downsample feature maps to reduce dimensionality and computation.

Fully Connected Layers: Perform the final classification into one of the seven emotion categories.

Learning Rate Scheduling: Automatically reduce the learning rate if the validation loss plateaus.


Model Architecture

Input Layer: Accepts grayscale images of shape (48, 48, 1).

Convolutional Layers:
Four Conv2D layers with increasing filter sizes (128, 256, 512).
ReLU activation for non-linearity.
Batch Normalization for stability.
Pooling and Dropout:
MaxPooling layers to reduce spatial dimensions.
Dropout layers to mitigate overfitting.
Fully Connected Layers:
Two dense layers with ReLU activation.
Regularization and dropout applied.

Output Layer:
Dense layer with softmax activation for classification into 7 categories.

Training Details-

Loss Function: Categorical Crossentropy.
Optimizer: Adam with an initial learning rate of 0.001.
Evaluation Metric: Accuracy.


Learning Rate Scheduler:
Reduces the learning rate by a factor of 0.5 if the validation loss does not improve for 5 epochs.
Minimum learning rate is set to 1e-6.