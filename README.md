This project seeks to compare how well different supervised learning techniques perform in determining whether a given image should be classified as a left turn or a right turn. The images to be used are from the first-person perspective of a vehicle driver. The classification techniques used in this notebook include:

Logistic Regression
kNN (with various k)
Decision Tree (with various max_depth and various max_leaf_nodes)
While more advanced machine learning techniques are used these days for image recognition (such as convolutional neural networks for self-driving car applications in particular), this project serves to assess these more fundamental techniques. They're less complex in nature, require less computing power to train and test, and could prove useful as a pre-processing layer(s) in a larger implementation.

The initial dataset is fairly straightforward, containing 63,825 rows of data (images and corresponding steering angles):

Images ([256 px H x 455 px W x 3 color channels (BGR)], .jpg format, 3.25 GB)
Steering angle ([-388.82, 252.61], .csv format, 1.1 MB)

Positive Steering angle values indicate a clockwise turn (right) while negative values indicate a counterclockwise turn (left). Part of the preprocessing of the Images will be to flatten their 3D structure into a 1D structure, where ultimately each pixel's brightness will correspond to a feature  𝑋𝑖,𝑛. The steering angle will then correspond to the associated steering direction (-1 for left turns, +1 for right turns)  𝑦𝑖.

The data was provided by Sully Chen via his driving-datasets repository on GitHub: https://github.com/SullyChen/driving-datasets. It is offered via the MIT license.
