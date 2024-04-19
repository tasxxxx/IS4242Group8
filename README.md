# IS4242Group8

## Introduction to Problem
In Singapore’s recycling plants, such as SembWaste, there is heavy reliance on manual labour for identification and sorting of recyclable materials which present challenges in meeting the increased demand efficiently (Kashyap, 2022). The current system is not only labour
intensive, but also poses numerous health threats to the workers, which makes it tough for companies to find workers to perform the tasks.

## Proposed Solution
The introduction of an image recognition system can allow for the automation of identification of recyclable materials among the piles of trash, and also sorts it based on the different recyclable material on a conveyor belt. As accuracy is essential in this step, it is ideal for the trash to be sorted automatically one by one. This would tackle the bottleneck in the current recycling system by improving the efficiency of sorting the trash into the recyclable ones and reducing manpower.

## Built with
Python <br/>
Jupyter Notebook

## Getting Started
The files labelled_iamges consists of the json file for the raw images, which was labeled on Roboflow and saved collectively in data_preprocessing_image_classification file.

The kaggle_data file consists of the images from kaggle dataset, that was used in comparison against our collected images.

The our_dataset file is the final file that consisted of the train, validation and test split of the data post data preprocessing and augmentation. It is further split into the individual class based on the folder name. 

The different ipynb are labelled according to the model used, as well as the dataset and image variation (coloured or grayscale).

## Libraries Used
json <br/>
shutil <br/>
cv2 <br/>
imgaug <br/>
tensorflow <br/>
Sequential <br/>
keras.layers <br/>
ImageDataGenerator <br/>
sklearn.metrics <br/>
keras <br/>
PIL <br/>
pathlib <br/>
scipy <br/>
os <br/>
numpy <br/>
matplotlib.pyplot <br/>
torchvisio.datasets <br/>
torchvision.transform <br/>
random <br/>
seaborn <br/>
tensorflow.keras.optimizers <br/>
skimage.transform <br/>

## Data Preprocessing
The data preprocessing step includes grayscaling of images to reduce the colour channel to 1, and resizing images to 128 x 128 pixels for consistency.
The data is split into 70:20:10 ratio for train, validation and test set. 
The data augmentation process includes flipping the image horizontally, modifying the brightness, saturation, and contrast to increase the training data size and prevent data leakage.

## Training

## Results
