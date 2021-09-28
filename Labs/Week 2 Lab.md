# Week 2 Lab

# Contents
* Data collection protocol
* Viewing collected data
* Cleaning and trimming your data
* Uploading your data to a shared repository
* Introduction to Human Activity Recognition using sensor data
* Further readings and tutorials

# Introduction

This week your main task will be to:
* Complete Coursework 1:
    * Collect real time data using the Respeck and the Thingy
    * View your collected data, clean and trim your recordings
    * Upload your complete recordings to a shared repository
* Learn common approaches to data analysis for HAR
* Capture the requirements and use cases for your target application

# Coursework 1

You should have set up your developing environment in [Week 1 Lab](./Week%201%20Lab.md). If you have not yet
completed your setup please go back to the first Lab. 

You should have also started to collect some test data. This week we will be focusing on collecting 
real data which will be used by everyone in the class in training their models. 

## 1. List of activities
Each student in the class will need to collect data for the following activities:
* Sitting (straight, bent forward, bent backward)
* Standing
* Lying down (left, right, on the back, on the front)
* Walking
* Running / Jogging
* Ascending and descending stairs 
* Desk work
* General movement (sudden turns, bending down, getting up from chairs, anything else that doesn't qualify as an activity)
* Falling (on the knees, on the back, on the sides)

You will be using two types of sensors to collect data for these activities:
* The **Respeck** sensor - worn on the lower left ribcage, attached with MeFix tape, sampling accelerometer and gyroscope data at 25Hz
* The **Nordic Cube (Thingy)** - worn in the front right trouser pocket, sampling accelerometer, gyroscope and magnetometer data at 25Hz

If you cannot collect parts of the data (e.g. collecting falling data if you have an injury), please let us know and we will
find other ways to augment the data.

## 2. Sensor placement

### Respeck

Everyone will need to wear the sensors in the same places to ensure consistency across the data.

The **Respeck** sensor should be placed on the **left lower ribcage**, with the blue half against the skin. 
Make sure that the Respeck is first put into the small plastic bag provided. 
You should be able to read the Respeck label when placing it on your chest – this ensures 
the sensor is held the right way up, as shown in the figure below. 

Secure the sensor to the chest using the MeFix tape provided. 
If you run out of tape you should let us know and we will provide you with more. 


<img src="../Images/respeck_placement.png" width="630" alt="respeck placement" />

### Thingy

The Thingy sensor should be placed in the front right pocket of your trousers, with the circle placed in the upper right 
corner and the USB port facing downwards.

<img src="../Images/thingy_placement.png" width="300" alt="thingy placement" />

## 3. Connection to sensors

Open the PDIoT app on your phone and navigate to the *Record Data* activity. Make sure both sensors are connected to the app
by verifying that the live data at the bottom of the screen is changing. 

If you have any issues connecting the phone to your sensors, please ensure you have followed all the steps
in [Week 1 Lab](./Week%201%20Lab.md).

## 4. Recording activities

**Please record each activity for 30 seconds!**

You are required to ensure the recording only contains one activity. 
For example, if you start recording data for walking and you only start moving after the 
first 3 seconds, you should trim the first 3 seconds of this recording, as they are not 
representative of the walking activity. 
The total length of your recordings AFTER TRIMMING should be 30 seconds. 

If you accidentally collect less data for one activity please redo the recording.

Each student should take part in the data collection for both sensors. The only exception should be students who are 
distance learners for PDIoT and are not physically present at the university at the time 
of data collection, as we will not be providing them with hardware. 

If you have any conditions that would prevent you from collecting any of the activities above (for example falling, 
if you have any injuries) please let us know in advance.

## 5. Activity descriptions

Please follow these activity descriptions as closely as possible to ensure consistency across all collected data. 
The Lab Demonstrator will also make sure that you are performing the activities correctly.

1.	**Sitting straight**

Sit down on a chair with your back straight. Breathe normally for 30 seconds. Try to not move, talk, cough or laugh during this recording.

2.	**Sitting bent forward**

Sit down on a chair and lean forward. Breathe normally for 30 seconds. Try to not move, talk, cough or laugh during this recording.

3.	**Sitting bent backward**

Sit down on a chair and lean backward in a relaxed position. Breathe normally for 30 seconds. Try to not move, talk, cough or laugh during this recording.

4.	**Standing**

Stand up with your back straight. Breathe normally for 30 seconds. Try to not move, talk, cough or laugh during this recording.

5.	**Lying down on the left side**

Lie down on an even surface such as a bed or a sofa. Make sure your torso is completely horizontal. Turn onto your left side. Breathe normally for 30 seconds. Try to not move, talk, cough or laugh during this recording.

6.	**Lying down on the right side**

Lie down on an even surface such as a bed or a sofa. Make sure your torso is completely horizontal. Turn onto your right side. Breathe normally for 30 seconds. Try to not move, talk, cough or laugh during this recording.

7.	**Lying down on the front**

Lie down on an even surface such as a bed or a sofa. Make sure your torso is completely horizontal. Turn onto your belly. Breathe normally for 30 seconds. Try to not move, talk, cough or laugh during this recording.

8.	**Lying down on the back**

Lie down on an even surface such as a bed or a sofa. Make sure your torso is completely horizontal. Turn onto your back. Breathe normally for 30 seconds. Try to not move, talk, cough or laugh during this recording.

9.	**Walking**

Find a space where you can walk in a straight line for 30 seconds or take as few sudden turns as possible. Walk at a normal pace and try to not stop during the recording.

10.	**Running or Jogging**

Find a space where you can run or jog in a straight line for 30 seconds or take as few sudden turns as possible. Try to not stop during the recording.

11.	**Ascending stairs**

Find a space where you can continuously climb a flight of stairs for 30 seconds, for example Appleton Tower. Walk up the stairs at a normal pace and do not stop for the 30 seconds of the recording.

12.	**Descending stairs**

Find a space where you can continuously descend a flight of stairs for 30 seconds, for example Appleton Tower. Walk down the stairs at a normal pace and do not stop for the 30 seconds of the recording.

13.	**Desk work**

Sit down on a desk chair in a relaxed position and type something on your computer, move the mouse around or write something on a piece of paper for 30 seconds. Try to not talk, cough or laugh during this recording or make any sudden movements.

14.	**General movement**

Make dynamic movements for 30 seconds. This includes sitting down on a chair, getting up from a chair, bending down, suddenly turning around etc. The most important point is to continue moving for the full 30 seconds.

15.	**Falling on the knees**

From a straight standing position, fall on your knees and stop on your hands. Do this for as many times as it takes to gather 30 seconds of falling data. You can use a pile of pillows to soften your fall.

16.	**Falling on the back**

From a straight standing position, fall on your back on a soft surface, preferably a bed or a mattress. Do this for as many times as it takes to gather 30 seconds of falling data.

17.	**Falling on the left**

From a straight standing position, fall on your left side on a soft surface, preferably a bed or a mattress. Do this for as many times as it takes to gather 30 seconds of falling data.

18.	**Falling on the right**

From a straight standing position, fall on your right side on a soft surface, preferably a bed or a mattress. Do this for as many times as it takes to gather 30 seconds of falling data.

## 6. Obtaining the recorded files

Please check [Week 1 Lab](./Week%201%20Lab.md) for instructions on how to obtain your recording files. 
Make sure there are no test recordings in your file collection - you can check this by the timestamp
appended to each file. 

Copy the files on your computer and store them in a folder for easy access.

## 7. Viewing and cleaning the data

We will now run a Jupyter Notebook to inspect the collected data. 

First, make sure you have activated your conda enviroment for PDIoT. Here, we assume you 
have named your environment `pdiot`.

```angular2html
conda activate pdiot
```

Navigate to the pdiot-practical folder, then start Jupyter Notebook:
```angular2html
jupyter notebook
```

This will open a new tab in your browser. Open the [Week 2 Notebook](./Week%202%20-%20PDIoT%20data%20analysis.ipynb). 
Replace the test filepath with the path of one of your recordings. Then run all the cells of the Notebook.

There are additional comments and explanations in the Notebook about how to load files, plot them and 
what to watch out when cleaning the data. 

Please do not modify the structure of the data in other ways than the stated ones. The goal is to have a 
cohesive dataset with which everyone can work.

## 8. Uploading your data to the shared repository

Gather all your **clean** files and organise them into folders by subject ID. Each subject ID should represent
your and your team mate's student ID. For example, if your team is made out of students *s1234567* and *s7654321*, then your
upload folder structure should look like this:

```
.
+-- 2021
|   +-- s1234567
|   |   +-- Respeck_s1234567_Sitting_{timestamp}.csv
|   |   +-- Respeck_s1234567_Standing_{timestamp}.csv
|   |   +-- ...
|   |   +-- Thingy_s1234567_Standing_{timestamp}.csv
|   |   +-- Thingy_s1234567_Standing_{timestamp}.csv
|   |   +-- ...
|   +-- s7654321
|   |   +-- Respeck_s7654321_Sitting_{timestamp}.csv
|   |   +-- Respeck_s7654321_Standing_{timestamp}.csv
|   |   +-- ...
|   |   +-- Thingy_s7654321_Standing_{timestamp}.csv
|   |   +-- Thingy_s7654321_Standing_{timestamp}.csv
|   |   +-- ...
```

Upload your data to the [shared repository](https://github.com/specknet/pdiot-data/tree/master/2021). Careful to upload it to the 2021 folder. 

### <span style="color: red">Read carefully ! </span>

Due to new GitHub organization rules you will have to fork the repo and create a pull request for your upload. The pull request will be approved by one of the PDIoT moderators by the end of each day. 

You can follow the full instructions here: https://github.com/firstcontributions/first-contributions

Summary:

1. Fork the pdiot-data repo

2. On your forked repo, create a new branch (e.g. group-A-upload) and add your files to that branch

3. Commit and push changes to your forked repo

4. From your forked repo, create a pull request to pdiot-data/master in order to integrate your changes

You can follow all of these steps from the command line, as well as just the web interface. 

Be very careful with the upload. You will be graded automatically based on the files which you have uploaded.

Do not delete or overwrite other people's data.

# Introduction to Human Activity Recognition

We have prepared a [sample Jupyter Notebook](./Week%202%20-%20Introduction%20to%20Human%20Activity%20Recognition.ipynb) to show you how to preprocess some of the data.

Some recommended readings for Human Activity Recognition papers are:
* [A Study on Human Activity Recognition Using Accelerometer Data from Smartphones](https://www.sciencedirect.com/science/article/pii/S1877050914008643)
* [Deep Learning for Sensor-based Human Activity Recognition: Overview, Challenges and Opportunities](https://arxiv.org/pdf/2001.07416.pdf)
* [Human Activity Recognition with Convolutional Neural Networks](https://arxiv.org/pdf/1906.01935.pdf)

You should start developing your Human Activity Recognition model using a deep learning library. We highly recommend using [Tensorflow](https://www.tensorflow.org/install) for its portability to Android devices.

For good tutorials on how to get started with Tensorflow we recommend:
* the official [documentation](https://www.tensorflow.org/learn)
* online tutorials for HAR, for example [this one](https://towardsdatascience.com/time-series-classification-for-human-activity-recognition-with-lstms-using-tensorflow-2-and-keras-b816431afdff). This doesn't mean that you need to implement the same machine learning methods, but it does provide insight into how an end-to-end HAR system would work.

Things to remember:
* HAR models need to be tested on completely unseen subjects due to intra-subject variability
* Careful how you split your recordings 
* Consider carefully how you want to develop your Machine Learning model - remember it needs to run on an Android Phone or
directly on the sensor Firmware.
  
# Capturing the requirements of your application
Start thinking about how your users might want to interact with your application. 

Questions to consider:
* How will you show your users the current activity?
* Do you want all your processing to happen on the phone or do you want to include a backend component?
* How much input will users have to give you?
* What will the purpose of your app be? Simple activity tracking? Remote patient monitoring? 
