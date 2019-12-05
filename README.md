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

In DL-CNN.ipynb: 
1. Got image from Kaggle competition.
2. Plot Pie and Bar Chart.
3. Preprocessing image for 10 classes.
4. We utilized Data Augmentation method.
5. Create a CNN model with 20 epochs. 
6. Evaluate Accuracy. 

In DL-VanillaAndVGG.ipynb
1. Set up hyperparameter and variable.
2. Import the given csv dataset.
3. Split the train the test data.
4. Data visualization and overview.
5. Building Vanila Model with 4 Convolutional layer. 
6. Evaluate the Accuracy.
7. Improve the model with Data Augmentation.  
8. Improve the model by VGG net transfer learning. 


