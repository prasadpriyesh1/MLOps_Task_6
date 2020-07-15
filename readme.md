# MLOps Task 6

In this task I have implemented face detection using mask R-CNN with the help of supervise.ly

# Steps to be followed

Following steps must be done to perform the task.

 1. Download dataset
 2. pre-processs dataset using supervise.ly
 3. train model on supervise.ly

## Download dataset

I have used a small dataset of 25 images to achieve my goal
[Dataset](https://github.com/prasadpriyesh1/MLOps_Task_6/tree/master/faces)
## pre-process data

 1. create supervise.ly account
 2. choose a team and create a new workspace![face detection workspace](https://github.com/prasadpriyesh1/MLOps_Task_6/blob/master/Screenshot%20%2888%29.png)
 3. import your dataset by simply dragging and dropping
 4. click on projects in the left pane and select the imported dataset
 5. now manually highlight the face in each of the images using polygon option![highlighting face](https://github.com/prasadpriyesh1/MLOps_Task_6/blob/master/Screenshot%20%2879%29.png)
 6. go back to projects
 7. click on the 3 dots >> run DTL>>Create Train Set >> Instance Segmentation.
 8. a json file will be visible, now click on start button to start image augmentation![tasks](https://github.com/prasadpriyesh1/MLOps_Task_6/blob/master/Screenshot%20%2880%29.png)
 

> note : I had 25 images which were converted into 550 images. Image augmentation is useful for small datasets

## Train model

 1. click on Neural Networks in the left pane 
 2. click on add
 3. select 'Mask R-CNN (Keras + TF) (COCO)' model![models](https://github.com/prasadpriyesh1/MLOps_Task_6/blob/master/Screenshot%20%2881%29.png)

Here you need to have your own agent to train the model on . I have used AWS ec2 instance for that which can be easily available on the free tier account. ![ami available](https://github.com/prasadpriyesh1/MLOps_Task_6/blob/master/Screenshot%20%2886%29.png)
![select hardware](https://github.com/prasadpriyesh1/MLOps_Task_6/blob/master/Screenshot%20%2885%29.png)
> note : you need to have a ec2 instance with GPU which will cost u a little bit

 1. click on clusters on the left pane.
 2. click on add button.
 3. run the command shown on the screen on your ec2 instance![enter image description here](https://github.com/prasadpriyesh1/MLOps_Task_6/blob/master/Screenshot%20%2884%29.png)
 4. click on neural network and select 'train' and your model will be trained
 


