The purpose of this project is to demonstrate your ability to collect, work with, and clean a data set. The goal is to prepare tidy data that can be used for later analysis. You will be graded by your peers on a series of yes/no questions related to the project. You will be required to submit: 1) a tidy data set as described below, 2) a link to a Github repository with your script for performing the analysis, and 3) a code book that describes the variables, the data, and any transformations or work that you performed to clean up the data called CodeBook.md. You should also include a README.md in the repo with your scripts. This repo explains how all of the scripts work and how they are connected. 

One of the most exciting areas in all of data science right now is wearable computing - see for example this article . Companies like Fitbit, Nike, and Jawbone Up are racing to develop the most advanced algorithms to attract new users. The data linked to from the course website represent data collected from the accelerometers from the Samsung Galaxy S smartphone. A full description is available at the site where the data was obtained:

http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

Here are the data for the project:

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

 You should create one R script called run_analysis.R that does the following. 

    Merges the training and the test sets to create one data set.
    Extracts only the measurements on the mean and standard deviation for each measurement. 
    Uses descriptive activity names to name the activities in the data set
    Appropriately labels the data set with descriptive variable names. 

    From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.


----------------------------------------


This analysis is need the "reshape2" package. 


This file uses the UCI HAR dataset available from http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones (University of California Irvine Human Activity Recognition) which are tracking accelerometer data collected from smartphones while test subjects performed various activities.

The data is provided in separate files and in two folders. There is both a 'test' and 'train' folder with data used to train an algorithm and one to test the predictions made. This analysis will combine the two sets as we are not performing any computer-directed learning on them.

In the data set, there is a file activity_labels.txt which translates the numeric activity designations into the 6 activities performed. The numeric activities are stored in the y_*.txt files and range from integers 1 to 6, inclusive.

The subject_*.txt files in the test and train directories associate the number of the subject being recorded, so there are multiple data readings for combinations of subject and activity.

The X_*.txt files contain the actual sensor readings and are described by the features_info.txt in the main directory of the data set.

The analysis combined these files and, per the directions, selected out only the mean and standard deviation for each measurement.



NOTE: Since the data has been processed already to calculate the various absolute displacements, it was determined that since the processed measurements were included, the individual X, Y, Z acelerometer were excluded.