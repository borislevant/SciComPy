# Applied-KamaTech Bootcamp
## Data Engineering, Deep-Learning part
## July 14, 2022

During the previous 2 weeks, all the groups created a new data set, extending the CIFAR-10, adding a few new classes into it. Most groups had the data set in the form of the CSV file, while each row represented the filepath to the picture and the labels. We are ready for the next missions

## Train the first neural network

The goal of this part is to prepare the data for train, load it into the Cloud (to be able to access it from the Google Colabatory) and to train our first Neural Network with GPUs

1. Once you created the Numpy arrays of Train, Validation and Test, save them into the binary file/s using the following command:

```
np.savez('cfar10_modified.npz', train=x_train, ytrain=y_train, val=x_validation, yval=y_validation, test=x_test, ytest=y_test)
```

2. Press the lower button in the leftmost menu:

![Files](https://user-images.githubusercontent.com/36374917/178928953-4370e4e1-8187-4032-886e-10c33c92364e.png)

3. In the menu opened, press the Mount Drive button:

![Mount Drive](https://user-images.githubusercontent.com/36374917/178930872-29de6338-8080-4602-ab39-4ce3e217bb88.png)

4. Run the Code cell that were created:

```
from google.colab import drive
drive.mount('/content/drive')
```




Our next mission is to train the
[![Azure Notebooks](https://notebooks.azure.com/launch.png)](https://notebooks.azure.com/yoavram/libraries/SciComPy) 
[![Official website](https://img.shields.io/badge/Website-SciComPy-orange.svg)](https://scicompy.yoavram.com)

## Syllabus

Python is a leading programming language for scientific research, data science, and machine learning. Thia course will familiarize students with the Python scientific stack and with best practices for scientific computing using methods from dynamical systems, stochastic processes, classical statistics, numerical analysis, Bayesian statistics, and artificial neural networks.

Every class will present a scientific problem, a computational method for tackling it, and a Python implementation of the method. Examples will include performing predicting points in tennis matches and survival on the Titanic, modelling evolutionary dynamics and infectious diseases, finding stationary points for a predator-prey system, inference in animal social networks, and classification of handwritten digits.

## Book
