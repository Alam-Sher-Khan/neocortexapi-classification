## **Project Description**

## 1. **Objective: Analyse Image Classification of MNIST Dataset**
* Our First Objective is to examine the HTM parameters (lobal/Local Inhibition, Potential Radius, Local Area Density and NumofActiveColumnsPerInArea.) which results in the highest similarity for the image of same label/class and lowest similarity between images of different classes of MNIST (Modified National Institute of Standards and Technology) dataset.

* We also have to provide the prediction code for image classification so that after learning, system can classify any given testing image based on the training dataset.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
### MNIST Dataset
The MNIST database (Modified National Institute of Standards and Technology database) is a large database of handwritten digits that is commonly used for training various image processing systems.The database is also widely used for training and testing in the field of machine learning.The MNIST database contains 60,000 training images and 10,000 testing images.

**MNIST Images can be extracted using extracted using 7zip https://www.7-zip.org/

![image](https://user-images.githubusercontent.com/93146590/159540392-5db930a4-44c1-49ab-8ab9-08518bfc0420.png)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
## 2. **Approach**

The goal of this project is to implement a program that uses the existing solution as a library and find the spatial pooler parameter values which influence the learning of images resulting in the best correlation matrix and can also predict any input image based on the learning in HTM.
When started the application will load images and start the training process. The training process runs in following steps.

**(1) Convert The Images to binary array via binarization**: 
The Binarization Library was developed as an open source project at Daenet.The current implementation uses a color threshold of 200 for every color in a 8bit-RGB scale.It is responsible for encoding the images in binary form after training of the images.(https://github.com/Alam-Sher-Khan/neocortexapi-classification/blob/Alam/ImageClassification/ImageClassification/InputFolder/One/1_a1.txt)

![image](https://user-images.githubusercontent.com/93146590/159535274-cf1ae555-4964-4944-b988-76f8cf24e2db.png)

**(2) Learn spatial patterns stored in images with the Spatial Pooler(SP)**: 
SP first iterates through all images until the stable state is entered. SP iterate through all the images as it learns. The essential function of spatial pooling is to form an SDR of the inputs. The output of the spatial pooler is as a binary vector, which represents the activation of columns in response to the current input.The SP consists of three phases, namely overlap, inhibition, and learning.

**(3) Validation of SP Learning for different set of images**: 
The result of the learning of images will generate a matrix which will show the relation between the micro (correlation in between the images of same label) and macro (correlation in between the images of different label).The last set of Sparse Density Representations (SDRs), the output of Spatial Pooler(SP) for each binarized image were saved for correlation validation.
There are 2 types of correlation which are defined as follow: 

**Micro Correlation**: Maximum/Average/Minimum correlation in similar bit percent of all images' SDRs which respect to each another in the same label.

**Macro Correlation**: Maximum/Average/Minimum correlation in similar bit percent of all images' SDRs with images from 2 different labels.
The results of the two correlation are printed in the command prompt when executing the code
 
**(4) Prediction Valiation**: 
The prediction code added will help to find the precentage of similarity between th input image and the SDR's of the MNIST dataset, and thus predicting the label of the image having the highest similarity.

**Workflow of the learning and prediction of MNIST images**
![image](https://user-images.githubusercontent.com/93146590/159539891-125feb98-f7c4-4bc1-8cff-73acc8f1f05c.png)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
## 3. Steps to setup the Learning and Prediction Code:
### Step1 - (To setup input folder for learning/training of images)
* Images must be copied in the following folder structure along with the application and the config json: (https://github.com/Alam-Sher-Khan/neocortexapi-classification/tree/Alam/ImageClassification/ImageClassification/InputFolder)

![image](https://user-images.githubusercontent.com/93146590/159564273-96030bdc-3bb9-4ad5-b308-ac0274393f41.png)

**The imagesets(MNIST) are stored inside "InputFolder/".**

![image](https://user-images.githubusercontent.com/93146590/159564326-ca4e9307-5181-4467-b678-145fa21c4af5.png)

**Each Imageset is stored inside a folder whose name is the set's label.**

![image](https://user-images.githubusercontent.com/93146590/159564704-a33729dd-5e81-4831-8604-c9e98d766fae.png)

### Step2 - (To setup image for prediction code)
**Select an Image and give the location path of the image in the prediction code** (https://github.com/Alam-Sher-Khan/neocortexapi-classification/blob/Alam/ImageClassification/ImageClassification/Experiment.cs#L95)

Example:
![image](https://user-images.githubusercontent.com/93146590/159565503-f10609a4-bda9-442d-9068-d31493b10556.png)

**HTM setting of the project can be inputted to the program by means of a .json file** (https://github.com/Alam-Sher-Khan/neocortexapi-classification/blob/Alam/ImageClassification/ImageClassification/htmconfig.json) . Various experiments have been conducted with changes of parameters in the json file
After running the code at the best HTM parameters obtained after experimenting in the learning phase, we can get the prediction status of any input image.

## 4. **Experiment**

### 1 - To find the HTM Parameters which gives the best fit that shows image classification
We have changed various parameters Global/Local Inhibition, Potential Radius, Local Area Density between various images of MNIST datasets. After conducting various experiments we have been able to find the parameters at which we get the least overlapping in between micro and macro and thus the best correlation matrix.

### 2 - To provide the prediction code
After we got the parameters which shows the best correlation matrix, we have added the code for predicting the images after learning phase.
1) Case1- We have entered an image which is somewhere similar to the input images(Dataset), and the prediction code will calculate the maximum percentage of similarity between the entered image and the input images of the label(Dataset)
2) Case2- We have entered and image which is completely different from the input images(Dataset), in this case the prediction code will direct a message as "Image is not similar to any of the input images"
3) The prediction code will calculate the Highest similarity in between the input images of the label(Dataset).
4) The prediction code will give the name of the label which is being predicted with the highest similarity.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 5. Goals Achieved
So far several experiments have been done to get the best correlation matrix in the learning phase and prediction code has been generated based on the initial analysis in the learning phase.

## 6. In-Progress
* We are conducting more experiments to further analyse the effects of other HTM Parameters on learning of MNIST images.
* We are working to create graphs from the data obtained from experiments.
* We are working on prediction code to make the setup of input testing image path independent of the local machine.
