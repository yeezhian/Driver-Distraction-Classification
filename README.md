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

![Screen Shot 2019-12-08 at 8 00 33 PM](https://user-images.githubusercontent.com/22896571/70406418-7f33bb00-19f5-11ea-9162-63aa9938b529.png)
![Screen Shot 2019-12-08 at 8 00 42 PM](https://user-images.githubusercontent.com/22896571/70406421-7fcc5180-19f5-11ea-9a45-9ca7dbf9a103.png)





We will implement a deep learning model, which will predict the driver activities at the time of driving.
# Data Augmentation method:
 Data Augmentation is the technique to generate new sample from the existing sample. So, you can reduce generalization error.  It will genrerate natrual sample. There are number of features, which can help you in data agumentation.
 rotation_range : is a value in degrees (0-180), a range within which to randomly rotate pictures.
 height_shift_range : Constructor control the amount of horizontal and vertical shift respectively.
 width_shift_range : Constructor control the amount of horizontal and vertical shift respectively.
 shear_range : Shear Intensity (Shear angle in counter-clockwise direction in degrees)
 zoom_range : Range for random zoom
 horizontal_flip : Randomly filp of input image in horizontally. But we can't use in our case. It can chane the class of images.
 fill_mode : Points outside the boundaries of the input image are filled according to the given mode. (default Nearest)
 ![Data Augmentation 2](https://user-images.githubusercontent.com/22896571/70406074-5101ab80-19f4-11ea-86c8-90b8d51c2aeb.png)
 ![DataAugmentation](https://user-images.githubusercontent.com/22896571/70406060-48a97080-19f4-11ea-9f48-519b85811537.png)

 
 # CNN Model with Data Augmentation Method
 Deep learning CNN models to train and test, each input image will pass it through a series of convolution layers with filters  (Kernals), Pooling, fully connected layers (FC) and apply Softmax function to classify an object with probabilistic values between 0 and 1. The below figure is a complete flow of CNN to process an input image and classifies the objects based on values.
 ![CNN Architecture](https://user-images.githubusercontent.com/22896571/70406073-4f37e800-19f4-11ea-9c07-518257fd5d21.png)
 ![CNN with Augmentation](https://user-images.githubusercontent.com/22896571/70406065-4a733400-19f4-11ea-9866-2a649f1e7862.png)
 


 
# Building Vanila Model with 4 Convolutional layer:Building the model
we'll develop the model with a total of 4 Convolutional layers, then a Flatten layer and then 2 Dense layers. we'll use the optimizer as rmsprop, and loss as categorical_crossentropy.
![Vanilla Model ](https://user-images.githubusercontent.com/22896571/70406062-49420700-19f4-11ea-8307-efbfa9596f18.png)


 # Improve the model with Data Augmentation:
 Here we have augmenting the previous model classifier, we have used the data on which I want to train the model. The folder train includes the images I need. I'll generate more images using ImageDataGenerator and split the training data into 80% train and 20% validation split. 
 ![Screen Shot 2019-12-08 at 7 55 40 PM](https://user-images.githubusercontent.com/22896571/70406221-d9804c00-19f4-11ea-8fe0-e3694cf590d0.png)
# Improve the model by VGG net transfer learning
Transfer Learning  is another interesting paradigm to prevent overfitting. Transfer Learning works by training a network on a big dataset such as ImageNet [12] and then using those weights as the initial weights in a new classification task. Typically, just the weights in convolutional layers are copied, rather than the entire network including fully-connected layers.
![Transfer Learning](https://user-images.githubusercontent.com/22896571/70406067-4d6e2480-19f4-11ea-8fbd-5c68d7d2cab2.png)
# Results
# Screenshots for Loss Vs Accuracy

![Accuracy1](https://user-images.githubusercontent.com/22896571/70399560-f4919280-19d9-11ea-90ce-a6ff3504cc33.png)
![Accuracy3](https://user-images.githubusercontent.com/22896571/70399565-fb200a00-19d9-11ea-8bde-2f6cea94bd15.png)
![Accuracy2](https://user-images.githubusercontent.com/22896571/70399566-fc513700-19d9-11ea-97cb-dd4c0389ecd8.png)
