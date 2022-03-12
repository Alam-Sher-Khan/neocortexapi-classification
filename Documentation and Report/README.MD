Group Name: Team Codecube 
Team members: * Alam Sher Khan
              * Aiman Zehra
              * Soundarya Talawai

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------# **Project Description** 

## **Analyse Image Classification**
In the previous work at the university an Image Classification solution has been implemented. Our task is to implement a program that uses the existing solution and start a training of learning images. The image dataset which we have used in this project is MNIST Database images. Our task is to change various learning parameters and to find the best fit that shows image classification. Most important learning parameters are: Global/Local Inhibition, Potential Radius, Local Area Density and NumofActiveColumnsPerInArea.
We have to demonstrate how these parameters influence the learning. Our code must provide the learning code and prediction code. After learning user should use your code and test the quality of learning. For example, the user after learning enter the image “table”. The prediction code provide a set of predicting results like: “Table – 87%, chair 7%, light - 3%”.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## **Our Approach**

## Objective 1 - To find the HTM Parameters which gives the best fit that shows image classification
We have changed various parameters Global/Local Inhibition, Potential Radius, Local Area Density between various images of MNIST datasets. After conducting various experiments we have been able to find the parameters at which we get the least overlapping in between micro and macro and thus the best correlation matrix.

 For example:
![Capture](https://user-images.githubusercontent.com/93146590/157971089-95cce4d0-f8c8-4332-804e-769f84ac9611.JPG)

## Objective 2 - To provide the prediction code
After we got the parameters which shows the best correlation matrix, we have added the code for predicting the images after learning phase.
1) Case1- We have entered an image which is somewhere similar to the input images(Dataset), and the prediction code will calculate the maximum percentage of similarity between the entered image and the input images of the label(Dataset)
2) Case2- We have entered and image which is completely different from the input images(Dataset), in this case the prediction code will direct a message as "Image is not similar to any of the input images"
3) The prediction code will calculate the Highest similarity in between the input images of the label(Dataset).
4) The prediction code will give the name of the label which is being predicted with the highest similarity.

Example
![Capture](https://user-images.githubusercontent.com/93146590/157980009-4d188b7d-0a7c-4971-86bf-248da9960316.JPG)
![Capture](https://user-images.githubusercontent.com/93146590/158025416-cb7330c9-666b-47a2-802d-ef4c5f967e09.JPG)


---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Steps to setup the Learning and Prediction Code:
## Step1 - 
The imagesets(MNIST) are stored inside "InputFolder/".

![Capture](https://user-images.githubusercontent.com/93146590/157983651-dd5b38c8-463a-4310-b118-3b5e2df73f06.JPG)

Each Imageset is stored inside a folder whose name is the set's label.

![Capture](https://user-images.githubusercontent.com/93146590/157983987-0cdfe35a-811e-49f2-b580-ec515889c2a4.JPG)

## Step2 - 
Select an Image and give the location path of the image in the prediction code.

Example:
![Capture](https://user-images.githubusercontent.com/93146590/158025162-08efce1d-ac9d-49f0-b12b-b273312cd706.JPG)

Run the code and the desired output will be displayed

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Goals Achieved/Progress
All the objectives described in the project description has been achieved successfully, test cases are prepared, code is completed and expected output is achieved, Final report documentation of the project is in progress. We are also working on project to provide more improvised solution and conducting experiments to provide more better results and prediction.
