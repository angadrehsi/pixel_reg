# Supervised Regression

## Problem Statement
Using Deep Learning techniques, predict the coordinates (x,y) of a pixel which has a value of 255 for 1 pixel in a given 50x50 pixel grayscale image and all other pixels are 0. The pixel with a value of 255 is randomly assigned.

## Dataset Generation
* The arrays are generated using np,zeros and pixels are randomly selected using randint function
* 10000 samples generated for training, for model to generalize the coordinates
* Coordinates are normalized from 0-255 to 0-1 range

## Model Architecture
* Convolutional Neural Network (CNN) with 3*3 kernels used for training. 
* MaxPooling: 2x2 pooling layers are used to reduce spatial dimensions. 
* A Flatten layer followed by a Dense (64) layer to convert spatial features into numerical coordinates.
* Sigmoid Activation: The output layer uses a Sigmoid activation function. 

## 3. Performance & Evaluation
* Loss Function: Mean Squared Error (MSE) used
* Metric: Mean Absolute Error (MAE) is used to track accuracy in normalized units.
* Result: The model achieves sub-pixel accuracy, typically reaching an average error of 0.21 pixels on the test set.

## 4. Installation & Usage

### Prerequisites
* Python 3.8+
* NumPy
* Matplotlib
* TensorFlow 2.x
* Pillow (PIL)

### Installation
pip install -r requirements.txt or run all in notebook to install all dependencies