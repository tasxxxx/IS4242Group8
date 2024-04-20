# IS4242 Group 8: Classification on Recyclable Materials

## Introduction to Problem
In Singapore’s recycling plants, such as SembWaste, there is heavy reliance on manual labour for identification and sorting of recyclable materials which present challenges in meeting the increased demand efficiently (Kashyap, 2022). The current system is not only labour intensive, but also poses numerous health threats to the workers, which makes it tough for companies to find workers to perform the tasks.

## Proposed Solution
The introduction of an image recognition system can allow for the automation of identification of recyclable materials among the piles of trash, and also sorts it based on the different recyclable material on a conveyor belt. As accuracy is essential in this step, it is ideal for the trash to be sorted automatically one by one. This would tackle the bottleneck in the current recycling system by improving the efficiency of sorting the trash into the recyclable ones and reducing manpower.

## Built with
Python <br/>
Jupyter Notebook

## Getting Started
The files labelled_images_name consists of the json file for the raw images from each member, which was labeled on Roboflow and saved collectively in data_preprocessing_image_classification file.

The kaggle_data file consists of the images from kaggle dataset, that was used in comparison against our collected images.

The our_dataset file is the final file that consisted of the train, validation and test split of the data post data preprocessing and augmentation. It is further split into the individual class based on the folder name. 

The various .ipynbs are labelled according to the model used, as well as the dataset and image variation (coloured or grayscale).

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

## Installation
1. First, ensure you have Python 3.x installed on your system.  
2. Install the libraries mentioned above using pip3:  
    e.g. pip3 install json  

## Data Preprocessing
The data preprocessing step includes grayscaling of images to reduce the colour channel to 1, and resizing images to 128 x 128 pixels for consistency.
The data is split into 70:20:10 ratio for train, validation and test set. 
The data augmentation process includes flipping the image horizontally, modifying the brightness, saturation, and contrast to increase the training data size and prevent data leakage.

## Training
Since the project focuses on image classification, three key models were employed:  
1. a Convolutional Neural Network (CNN) serving as the baseline model  
2. a pre-trained InceptionV3 model  
3. a pre-trained ResNet-50 model  

## Results

| Dataset            | Image Variation | Models      | Accuracy |
|--------------------|-----------------|-------------|----------|
| Our collected      | Grayscale       | CNN         | 47%      |
|                    |                 | InceptionV3 | 67%      |
|                    |                 | ResNet50    | 68%      |
| Our collected      | Coloured        | CNN         | 41%      |
|                    |                 | InceptionV3 | 67%      |
|                    |                 | ResNet50    | 70%      |
| Kaggle             | Grayscale       | CNN         | 49%      |
| dataset            |                 | InceptionV3 | 75%      |
|                    |                 | ResNet50    | 79%      |
| Kaggle             | Coloured        | CNN         | 66%      |
| dataset            |                 | InceptionV3 | 74%      |
|                    |                 | ResNet50    | 80%      |

InceptionV3 and ResNet-50 consistently outperformed the baseline CNN model in accuracy on both our collected dataset and the Kaggle dataset. 
There are marginal differences in accuracy between grayscale and coloured images overall, which suggest that grayscale images could be preferable for the simpler and quicker learning speed.
In addition, the top-performing configuration, using the Kaggle dataset's coloured variation with the ResNet-50 model, achieved an impressive accuracy rate of 80% while our collected dataset managed to achieve 70% and 68% accuracy for the coloured and grayscale variation respectively with the same model, which is not far off. 
This meant that the quality of our collected dataset was comparable with the public dataset and could be improved by increasing the training size.




