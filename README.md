
# OSS4900-Capstone
Depth Camera Hand Gesture Recognition

Institution: Carleton University

Course: OSS4900 Capstone 

Term: F22 - W23

Students: Adam Thompson, Philippe Beaulieu

Advisor:  Dr. Marzieh Amini

Description:

Camera hardware needed: Intel D435 Depth Camera
 
These programs will take the stream of both RGB and DEPTH from an Intel D435 Depth camera
and predict a defined hand gesture. All the codes are present to create the images, train
these images with bot Mediapipe Hand for RGB and a CNN model for DEPTH, and then be able
to predict hand gesture with a live feed from the Intel D435 cam,era.
              
 Files (to be executed in order if you don't have the dataset):
 - 0 - Pre0 - Intel_VideoCam - saving images.ipynb, this is to create the images
 - 0 - Pre1 - csv_dataset_creation.ipynb, to create the mediapipe landmark dataset from RGB images
 - 0 - Pre2 - cnn_model_creation.ipynb, to create the CNN trained model from DEPTH images 
 - 1 - MAIN - Intel D435_HG_recognition.ipynb, main program to predict the gesture
 - class_name.json, class name from the categogies
 - dataset3.csv, RGB Mediapipe landmark 
 - model.tflite, DEPTH CNN trained model (not included as file is too large)
 
  The folder hierarchy is important to load the images, it is as follow:

     TRAIN
       -DEPTH
          -folder0
             - image0.jpg
             - image1.jpg
             - image2.jpg
             - ...
          -folder1
             - image0.jpg
             - image1.jpg
             - image2.jpg
             - ...
          -...
       -RGB
          -folder0
             - image0.jpg
             - image1.jpg
             - image2.jpg
             - ...
          -folder1
             - image0.jpg
             - image1.jpg
             - image2.jpg
             - ...
          -...
     TEST -> follow the same structure as train
