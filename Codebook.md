Code Book for UCI HAR Dataset
=============================
For the Getting and Cleaning Data Course Project July 27, 2014
--------------------------------------------------------------
Dataset source: Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012

The tidy dataset created goes through the following steps to be created
- Merges the training and the test sets to create one data set.
- Extracts only the measurements on the mean and standard deviation for each measurement. 
- Uses descriptive activity names to name the activities in the data set
- Appropriately labels the data set with descriptive variable names. 
- Creates a second, independent tidy data set with the average (mean) of each variable for each activity and each subject. 

The following are the columns of the tidydata.txt file

For and explanation of the original data set please see http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones


Activity - char
- Factor var. WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING

Subject - integer
- The subject performaning the Activity identified by a number 1-30

TimeBodyAcceleratorMeanX - real
- The mean of the mean of the time domain of the body accelerator in the 
X axis for each activity and each subject

TimeBodyAcceleratorMeanY - real
- The mean of the mean of the time domain of the body accelerator in the Y axis for each activity and each subject

TimeBodyAcceleratorMeanZ - real
- The mean of the mean of the time domain of the body accelerator in the Z axis for each activity and each subject

TimeBodyAcceleratorStandardDeviationX - real
- The mean of the standard deviation of the time domain of the body accelerator in the X axis for each activity and each subject

TimeBodyAcceleratorStandardDeviationY - real
- The mean of the standard deviation of the time domain of the body accelerator in the Y axis for each activity and each subject

TimeBodyAcceleratorStandardDeviationZ - real
- The mean of the standard deviation of the time domain of the body accelerator in the Z axis for each activity and each subject

TimeGravityAcceleratorMeanX - real
- The mean of the mean of the time domain of the gravity accelerator in the X axis for each activity and each subject

TimeGravityAcceleratorMeanY - real
- The mean of the mean of the time domain of the gravity accelerator in the Y axis for each activity and each subject

TimeGravityAcceleratorMeanZ - real
- The mean of the mean of the time domain of the gravity accelerator in the Z axis for each activity and each subject

TimeGravityAcceleratorStandardDeviationX - real
- The mean of the standard deviation of the time domain of the gravity accelerator in the X axis for each activity and each subject

TimeGravityAcceleratorStandardDeviationY - real
- The mean of the standard deviation of the time domain of the gravity accelerator in the Y axis for each activity and each subject

TimeGravityAcceleratorStandardDeviationZ - real
- The mean of the standard deviation of the time domain of the gravity accelerator in the Z axis for each activity and each subject

TimeBodyAcceleratorJerkMeanX - real
- The mean of the mean of the time domain of the body accelerator jerk in the X axis for each activity and each subject

TimeBodyAcceleratorJerkMeanY - real
- The mean of the mean of the time domain of the body accelerator jerk in the Y axis for each activity and each subject

TimeBodyAcceleratorJerkMeanZ - real
- The mean of the mean of the time domain of the body accelerator jerk in the Z axis for each activity and each subject

TimeBodyAcceleratorJerkStandardDeviationX - real
- The mean of the standard deviation of the time domain of the body accelerator jerk in the X axis for each activity and each subject

TimeBodyAcceleratorJerkStandardDeviationY - real
- The mean of the standard deviation of the time domain of the body accelerator jerk in the Y axis for each activity and each subject

TimeBodyAcceleratorJerkStandardDeviationZ - real
- The mean of the standard deviation of the time domain of the body accelerator jerk in the Z axis for each activity and each subject

TimeBodyGyroscopeMeanX - real
- The mean of the mean of the time domain of the body gyroscope in the X axis for each activity and each subject

TimeBodyGyroscopeMeanY - real
- The mean of the mean of the time domain of the body gyroscope in the Y axis for each activity and each subject

TimeBodyGyroscopeMeanZ - real
- The mean of the mean of the time domain of the body gyroscope in the Z axis for each activity and each subject

TimeBodyGyroscopeStandardDeviationX - real
- The mean of the standard deviation of the time domain of the body gyroscope in the X axis for each activity and each subject

TimeBodyGyroscopeStandardDeviationY - real
- The mean of the standard deviation of the time domain of the body gyroscope in the Y axis for each activity and each subject

TimeBodyGyroscopeStandardDeviationZ - real
- The mean of the standard deviation of the time domain of the body gyroscope in the Z axis for each activity and each subject

TimeBodyGyroscopeJerkMeanX - real
- The mean of the mean of the time domain of the body gyroscope jerk in the X axis for each activity and each subject

TimeBodyGyroscopeJerkMeanY - real
- The mean of the mean of the time domain of the body gyroscope jerk in the Y axis for each activity and each subject

TimeBodyGyroscopeJerkMeanZ - real
- The mean of the mean of the time domain of the body gyroscope jerk in the Z axis for each activity and each subject

TimeBodyGyroscopeJerkStandardDeviationX - real
- The mean of the standard deviation of the time domain of the body gyroscope jerk in the X axis for each activity and each subject

TimeBodyGyroscopeJerkStandardDeviationY - real
- The mean of the standard deviation of the time domain of the body gyroscope jerk in the Y axis for each activity and each subject

TimeBodyGyroscopeJerkStandardDeviationZ - real
- The mean of the standard deviation of the time domain of the body gyroscope jerk in the Z axis for each activity and each subject

TimeBodyAcceleratorMagnitudeMean - real
- The mean of the mean of the time domain of the body accelerator magnitude for each activity and each subject

TimeBodyAcceleratorMagnitudeStandardDeviation - real
- The mean of the standard deviation of the time domain of the body accelerator magnitude for each activity and each subject

TimeGravityAcceleratorMagnitudeMean - real
- The mean of the mean of the time domain of the gravity accelerator magnitude for each activity and each subject

TimeGravityAcceleratorMagnitudeStandardDeviation - real
- The mean of the standard deviation of the time domain of the gravity accelerator magnitude for each activity and each subject

TimeBodyAcceleratorJerkMagnitudeMean - real
- The mean of the mean of the time domain of the body accelerator jerk magnitude for each activity and each subject

TimeBodyAcceleratorJerkMagnitudeStandardDeviation - real
- The mean of the standard deviation of the time domain of the body accelerator jerk magnitude for each activity and each subject

TimeBodyGyroscopeMagnitudeMean - real
- The mean of the mean of the time domain of the body gyroscope magnitude for each activity and each subject

TimeBodyGyroscopeMagnitudeStandardDeviation - real
- The mean of the standard deviation of the time domain of the body gyroscope magnitude for each activity and each subject

TimeBodyGyroscopeJerkMagnitudeMean - real
- The mean of the mean of the time domain of the body gyroscope jerk magnitude for each activity and each subject

TimeBodyGyroscopeJerkMagnitudeStandardDeviation - real
- The mean of the standard deviation of the time domain of the body gyroscope jerk magnitude for each activity and each subject

FreqBodyAcceleratorMeanX - real
- The mean of the mean of the frequency domain of the body accelerator in the X axis for each activity and each subject

FreqBodyAcceleratorMeanY - real
- The mean of the mean of the frequency domain of the body accelerator in the Y axis for each activity and each subject

FreqBodyAcceleratorMeanZ - real
- The mean of the mean of the frequency domain of the body accelerator in the Z axis for each activity and each subject

FreqBodyAcceleratorStandardDeviationX - real
T- he mean of the standard deviation of the frequency domain of the body accelerator in the X axis for each activity and each subject

TFreqBodyAcceleratorStandardDeviationY - real
T- he mean of the standard deviation of the frequency domain of the body accelerator in the Y axis for each activity and each subject

FreqBodyAcceleratorStandardDeviationZ - real
T- he mean of the standard deviation of the frequency domain of the body accelerator in the Z axis for each activity and each subject

FreqBodyAcceleratorJerkMeanX - real
- The mean of the mean of the frequency domain of the body accelerator jerk in the X axis for each activity and each subject

FreqBodyAcceleratorJerkMeanY - real
- The mean of the mean of the frequency domain of the body accelerator jerk in the Y axis for each activity and each subject

FreqBodyAcceleratorJerkMeanZ - real
- The mean of the mean of the frequency domain of the body accelerator jerk in the Z axis for each activity and each subject

FreqBodyAcceleratorJerkStandardDeviationX - real
- The mean of the standard deviation of the frequency domain of the body accelerator jerk in the X axis for each activity and each subject

FreqBodyAcceleratorJerkStandardDeviationY - real
- The mean of the standard deviation of the frequency domain of the body accelerator jerk in the Y axis for each activity and each subject

FreqBodyAcceleratorJerkStandardDeviationZ - real
- The mean of the standard deviation of the frequency domain of the body accelerator jerk in the Z axis for each activity and each subject

FreqBodyGyroscopeMeanX - real
- The mean of the mean of the frequency domain of the body gyroscope in the X axis for each activity and each subject

FreqBodyGyroscopeMeanY - real
- The mean of the mean of the frequency domain of the body gyroscope in the Y axis for each activity and each subject

FreqBodyGyroscopeMeanZ - real
- The mean of the mean of the frequency domain of the body gyroscope in the Z axis for each activity and each subject

FreqBodyGyroscopeStandardDeviationX - real
- The mean of the standard deviation of the frequency domain of the body gyroscope in the X axis for each activity and each subject

FreqBodyGyroscopeStandardDeviationY - real
- The mean of the standard deviation of the frequency domain of the body gyroscope in the Y axis for each activity and each subject

FreqBodyGyroscopeStandardDeviationZ - real
- The mean of the standard deviation of the frequency domain of the body gyroscope in the Z axis for each activity and each subject

FreqBodyAcceleratorMagnitudeMean - real
- The mean of the mean of the frequency domain of the body accelerator magnitude for each activity and each subject

FreqBodyAcceleratorMagnitudeStandardDeviation - real
- The mean of the standard deviation of the frequency domain of the body accelerator magnitude for each activity and each subject

FreqBodyAcceleratorJerkMagnitudeMean - real
- The mean of the mean of the frequency domain of the body accelerator jerk magnitude for each activity and each subject

FreqBodyAcceleratorJerkMagnitudeStandardDeviation - real
- The mean of the standard deviation of the frequency domain of the body accelerator jerk magnitude for each activity and each subject

FreqBodyGyroscopeMagnitudeMean - real
- The mean of the mean of the frequency domain of the body gyroscope magnitude for each activity and each subject

FreqBodyGyroscopeMagnitudeStandardDeviation - real
- The mean of the standard deviation of the frequency domain of the body gyroscope magnitude for each activity and each subject

FreqBodyGyroscopeJerkMagnitudeMean - real
- The mean of the mean of the frequency domain of the body gyroscope jerk magnitude for each activity and each subject

FreqBodyGyroscopeJerkMagnitudeStandardDeviation - real
- The mean of the standard deviation of the frequency domain of the body gyroscope jerk magnitude for each activity and each subject
 