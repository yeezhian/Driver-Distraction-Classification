# Driver-Distraction-Classification
Driver Distraction Classification using CNN, Vanilla Model and VGG Pretrained model 


Driver Distraction Monitoring This notebook is for the classification of driver behavior. We will do image pre-processing and use Deep learning CNN for identifying the behavior of the driver. Which is necessary for handling the unexpected road accident.

Nowadays vehicles are increasing exponentially. We need to be extra careful about the road incident. As there are a couple of things around you, which can distract the driving. We can use this model and implement a smart system, which will monitor driver activities at the time of driving and can alert him about the activities. It will reduce the number of roads accidents and will increase road safety.

State Farm Distracted Driver Detection has divided driving behavior into 10 classes. CLASS Description

C0 Safe Driving

C1 Texting - Right

C2 Talking On The Phone - Right

C3 Texting- left

C4 Talking on the Phone- left

C5 Operating The Radio

C6 Drinking

C7 Reaching Behind

C8 Hair And Makeup

C9 Talking To Passenger

We will implement a deep learning model, which will predict the driver activities at the time of driving.

In DL-CNN-Vanilla-VGGnet.ipynb: 
1. Got image from Kaggle competition.
2. Plot Pie and Bar Chart.
3. Preprocessing image for 10 classes.
4. We utilized Data Augmentation method:Data Augmentation is the technique to generate new sample from the existing sample. So, you can reduce generalization error. It will genrerate natrual sample. There are number of features, which can help you in data agumentation.
#rotation_range : is a value in degrees (0-180), a range within which to randomly rotate pictures.
#height_shift_range : Constructor control the amount of horizontal and vertical shift respectively.
#width_shift_range : Constructor control the amount of horizontal and vertical shift respectively.
#shear_range : Shear Intensity (Shear angle in counter-clockwise direction in degrees)
#zoom_range : Range for random zoom
#horizontal_flip : Randomly filp of input image in horizontally. But we can't use in our case. It can chane the class of images.
#fill_mode : Points outside the boundaries of the input image are filled according to the given mode. (default Nearest)
5. #Create a CNN model with 20 epochs. 
6. Evaluate Accuracy. 
7. Set up hyperparameter and variable.
8. Import the given csv dataset.
9. Split the train the test data.
10. Data visualization and overview.
11. #Building Vanila Model with 4 Convolutional layer:Building the model
we'll develop the model with a total of 4 Convolutional layers, then a Flatten layer and then 2 Dense layers. we'll use the optimizer as rmsprop, and loss as categorical_crossentropy.
12. Evaluate the Accuracy.
13. #Improve the model with Data Augmentation:Here we have augmenting the previous model classifier, we have used the data on which I want to train the model. The folder train includes the images I need. I'll generate more images using ImageDataGenerator and split the training data into 80% train and 20% validation split. 
14. #Improve the model by VGG net transfer learning. 

#Screenshots for Loss Vs Accuracy

![Accuracy1](https://user-images.githubusercontent.com/22896571/70399560-f4919280-19d9-11ea-90ce-a6ff3504cc33.png)
![Accuracy3](https://user-images.githubusercontent.com/22896571/70399565-fb200a00-19d9-11ea-8bde-2f6cea94bd15.png)
![Accuracy2](https://user-images.githubusercontent.com/22896571/70399566-fc513700-19d9-11ea-97cb-dd4c0389ecd8.png)
