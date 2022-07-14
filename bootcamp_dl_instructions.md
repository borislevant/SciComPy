# Applied-KamaTech Bootcamp
## Data Engineering, Deep-Learning part
## Questions: anna_levant@amat.com, boris_levant@amat.com
## July 14, 2022

During the previous 2 weeks, all the groups created a new data set, extending the CIFAR-10, adding a few new classes into it. Most groups had the data set in the form of the CSV file, while each row represented the filepath to the picture and the labels. We are ready for the next missions

## Load the data into Cloud and open it inside the Google Collab notebook

The goal of this part is to prepare the data for train, load it into the Cloud (to be able to access it from the Google Colabatory) and to train our first Neural Network with GPUs

1. Once you created the Numpy arrays of Train, Validation and Test, save them into the binary file/s using the following command:

```
np.savez('cfar10_modified.npz', train=x_train, ytrain=y_train, val=x_validation, yval=y_validation, test=x_test, ytest=y_test)
```
Upload the new created file into your own Google Drive. You can use the GMail account of the group or your private account

2. Press the lower button in the leftmost menu:

![image](https://user-images.githubusercontent.com/36374917/178933736-eb68b0be-0061-4618-90ec-bcda90da556b.png)

3. In the menu opened, press the Mount Drive button:

![Mount Drive](https://user-images.githubusercontent.com/36374917/178930872-29de6338-8080-4602-ab39-4ce3e217bb88.png)

4. Run the Code cell that were created:

```
from google.colab import drive
drive.mount('/content/drive')
```

5. Load the data using the following lines of code. Note that *loaded_data* is a "dictionary-type" object and you access it's values by names you specified in the *savez* command

```
loaded_data = np.load('/content/drive/MyDrive/cfar10_modified_1000.npz')
loaded_data['train']
```

## Enable the GPU in Google Collab notebook

In order to enable the GPU in your Google Collab notebooks please follow the instructions:

1. In the Notebook menu choose **Runtime-->Choose runtime type** command

2. In the window choose the **Hardware accelerator type** as GPU

![image](https://user-images.githubusercontent.com/36374917/178932894-fe8b688e-2ed0-4905-93e7-38af5c193b9f.png)

## Train the first Neural Network

Inside Google Collab open the notebook *https://github.com/borislevant/SciComPy/blob/master/cifar10-with-cnn-for-beginer.ipynb*

Modify the following parts:

1. Load your own data from the Google Drive

2. Update the number of classes according to your data

3. Add the validations set (the original notebook uses only train/test sets)

Pay attention that if everything works smoothly, it should take ~10 sec per epoch to train your data. However, if you don't use GPU, then the train can take more than 3 min per epoch

# Good luck!

