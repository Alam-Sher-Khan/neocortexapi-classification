## **Project Description**

## 1. **Objective: Analyse Image Classification of MNIST Dataset**
* Our First Objective is to examine the HTM parameters (lobal/Local Inhibition, Potential Radius, Local Area Density and NumofActiveColumnsPerInArea.) which results in the highest similarity for the image classification of MNIST (Modified National Institute of Standards and Technology) dataset.
* We also have to provide the prediction code for image classification so that after learning, system can classify the image based on learning.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
## 2. **Approach**

### MNIST Dataset
The MNIST database (Modified National Institute of Standards and Technology database) is a large database of handwritten digits that is commonly used for training various image processing systems.The database is also widely used for training and testing in the field of machine learning.The MNIST database contains 60,000 training images and 10,000 testing images.

**MNIST Images can be extracted using extracted using 7zip https://www.7-zip.org/

![MNIST-0000000001-2e09631a_09liOmx](https://user-images.githubusercontent.com/93146590/159464591-f38d0df9-eeb0-4b53-b6ae-7e564015a3a5.jpg) 

The goal of this project is to implement a program that uses the existing solution as a library and find the spatial pooler parameter values which influence the learning of images resulting in the best correlation matrix and can also predict any input image based on the learning in HTM.


![image](https://user-images.githubusercontent.com/93146590/159476992-ceecfa2c-d0db-4158-a70b-3671b286137f.png)
  ![image](https://user-images.githubusercontent.com/93146590/159476931-d066b88b-1ded-4243-9e58-1ecd6e3ddaf4.png)  ![image](https://user-images.githubusercontent.com/93146590/159477331-8178b739-c6d9-407a-bf4f-d3931bc536fd.png)  ![image](https://user-images.githubusercontent.com/93146590/159477405-6b03f0ad-8911-41c1-b08d-a2aaf20685f7.png) ![image](https://user-images.githubusercontent.com/93146590/159478497-af3b67c8-22f9-4650-af17-f2ea57e71e30.png)
  ![image](https://user-images.githubusercontent.com/93146590/159478366-66c57685-9255-48c3-a27f-4c8745cb9a3f.png) 
  
  ![image](https://user-images.githubusercontent.com/93146590/159479899-39eccced-86f3-4395-a8e8-19b5b79772d7.png) ![image](https://user-images.githubusercontent.com/93146590/159480218-81369a61-2a2b-490e-a657-fb7ddf970880.png) ![image](https://user-images.githubusercontent.com/93146590/159480428-18ceb06d-c58b-4a85-8d83-dc9072988089.png) ![image](https://user-images.githubusercontent.com/93146590/159480681-3ccaf624-066b-4d51-a43c-6f930dd642a7.png) ![image](https://user-images.githubusercontent.com/93146590/159480865-41d2ea90-6c1e-4b63-857c-d00bcc578341.png) ![image](https://user-images.githubusercontent.com/93146590/159481213-355c99f6-398c-4130-af54-2669404ad30a.png)
  
  ![image](https://user-images.githubusercontent.com/93146590/159482675-6903ea10-15ac-4168-b772-a31c2b41be77.png) ![image](https://user-images.githubusercontent.com/93146590/159483536-f1baa93b-4ce6-461c-8b5c-c1264a1e607b.png) ![image](https://user-images.githubusercontent.com/93146590/159484243-a54df1f7-37dd-4bf1-a9b7-8ca00c0e0984.png) ![image](https://user-images.githubusercontent.com/93146590/159484423-b07bc98a-21e0-4a1d-aa26-ed262e3aae28.png)
![image](https://user-images.githubusercontent.com/93146590/159484590-71c62cd3-a76c-4e85-a990-dbb76639b358.png) ![image](https://user-images.githubusercontent.com/93146590/159484821-f32aa6fe-da97-4cf0-95a2-6b0677fbe6ec.png)

![image](https://user-images.githubusercontent.com/93146590/159485005-5aa702e2-a31c-4535-9b7e-5295318f927a.png) ![image](https://user-images.githubusercontent.com/93146590/159485294-f0489df7-a20f-4bf7-a3ea-cf8b482cb82a.png)



![Capture](https://user-images.githubusercontent.com/93146590/159493693-188786ef-9da3-4496-95d5-271fc9e42b9e.JPG)




## 2. **Our Experiment**

### 1 - To find the HTM Parameters which gives the best fit that shows image classification
We have changed various parameters Global/Local Inhibition, Potential Radius, Local Area Density between various images of MNIST datasets. After conducting various experiments we have been able to find the parameters at which we get the least overlapping in between micro and macro and thus the best correlation matrix.

 For example:
![Capture](https://user-images.githubusercontent.com/93146590/157971089-95cce4d0-f8c8-4332-804e-769f84ac9611.JPG)

### 2 - To provide the prediction code
After we got the parameters which shows the best correlation matrix, we have added the code for predicting the images after learning phase.
1) Case1- We have entered an image which is somewhere similar to the input images(Dataset), and the prediction code will calculate the maximum percentage of similarity between the entered image and the input images of the label(Dataset)
2) Case2- We have entered and image which is completely different from the input images(Dataset), in this case the prediction code will direct a message as "Image is not similar to any of the input images"
3) The prediction code will calculate the Highest similarity in between the input images of the label(Dataset).
4) The prediction code will give the name of the label which is being predicted with the highest similarity.

### Example

### **Case1** - When testing image is similar to the learning dataset

**Testing Image**

![9_pic2](https://user-images.githubusercontent.com/93146590/158055870-5eefaedf-63bb-48e3-9f5c-f9f71b5f050b.png)

**Learning Dataset**

![Capture](https://user-images.githubusercontent.com/93146590/158055986-143d49d7-793a-4b1f-9cb0-907fea8865a5.JPG)

**Output Result in Case 1**

![Capture](https://user-images.githubusercontent.com/93146590/158058910-52c1de99-bc2e-45ee-8b6d-5f54a9ee2cd0.JPG)

### **Case2** - When testing image is completely different from the learning dataset

**Testing Image**

![eight](https://user-images.githubusercontent.com/93139817/159286046-f7a9bcb3-d08c-4afc-bb42-2f53683ca2e9.png)


**Learning Dataset**

![Capture](https://user-images.githubusercontent.com/93146590/158055986-143d49d7-793a-4b1f-9cb0-907fea8865a5.JPG)

**Output Result in Case 2**
![Formatting the display of results](https://user-images.githubusercontent.com/93139817/159286315-22e0ac4e-8d5c-46f1-a682-19c1a44e904c.PNG)


---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## 3. Steps to setup the Learning and Prediction Code:
### Step1 - (To setup input folder for learning/training of images)
* Images must be copied in the following folder structure along with the application and the config json: (https://github.com/Alam-Sher-Khan/neocortexapi-classification/tree/Alam/ImageClassification/ImageClassification/InputFolder)

![Capture](https://user-images.githubusercontent.com/93146590/158056620-58a8ea39-6be9-473e-b7e5-ad398e2504e5.JPG)

* The imagesets(MNIST) are stored inside "InputFolder/".

![Capture](https://user-images.githubusercontent.com/93146590/157983651-dd5b38c8-463a-4310-b118-3b5e2df73f06.JPG)

* Each Imageset is stored inside a folder whose name is the set's label.

![Capture](https://user-images.githubusercontent.com/93146590/157983987-0cdfe35a-811e-49f2-b580-ec515889c2a4.JPG)

### Step2 - (To setup image for prediction code)
* Select an Image and give the location path of the image in the prediction code (https://github.com/Alam-Sher-Khan/neocortexapi-classification/blob/Alam/ImageClassification/ImageClassification/Experiment.cs#L95)

Example:
![Capture](https://user-images.githubusercontent.com/93146590/158025162-08efce1d-ac9d-49f0-b12b-b273312cd706.JPG)

* HTM setting of the project can be inputted to the program by means of a .json file (https://github.com/Alam-Sher-Khan/neocortexapi-classification/blob/Alam/ImageClassification/ImageClassification/htmconfig.json) . Various experiments have been conducted with changes of parameters in the json file
After running the code at the best HTM parameters obtained after experimenting in the learning phase, we can get the prediction status of any input image.

## 4. Working Process
Following steps are included in the processing of the training of images:

1) Binarization/Encoder:It is responsible for encoding the images in binary form after training of the images.(https://github.com/Alam-Sher-Khan/neocortexapi-classification/blob/Alam/ImageClassification/ImageClassification/InputFolder/One/1_a1.txt)

2) Spatial Pooling: The essential function of spatial pooling is to form an SDR of the inputs. The output of the spatial pooler is as a binary vector, which represents the activation of columns in response to the current input.The SP consists of three phases, namely overlap, inhibition, and learning.

3) Learning Validation: The result of the learning of images will generate a matrix which will show the relation between the micro (correlation in between the images of same label) and macro (correlation in between the images of different label)

Example:
![Capture](https://user-images.githubusercontent.com/93146590/158057244-268ce79a-2859-4d44-b534-49d13fe5c935.JPG)

4) Prediction Valiation: The prediction code added will help to find the precentage of similarity between th input image and the SDR's of the MNIST dataset, and thus predicting the label of the image having the highest similarity.


## 5. Goals Achieved
So far several experiments have been done to get the best correlation matrix in the learning phase and prediction code has been generated based on the initial analysis in the learning phase.

## 6. In-Progress
* We are conducting more experiments to further analyse the effects of other HTM Parameters on learning of MNIST images.
* We are working to create graphs from the data obtained from experiments.
* We are working on prediction code to make the setup of input testing image path independent of the local machine.
