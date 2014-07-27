Getting-and-Cleaning-Data-Course-Project
========================================

The run_analysis.R script assumes it is placed as the same level as the "UCI HAR Dataset" directory.  As you will see in the script, the first line of code takes you into this directory.

```{r}
setwd("UCI HAR Dataset") 
```
The script read in the features.txt file in order to understand the values that the columns of the features dataset contains

features <- read.table("features.txt")

## Find those features(columns in the data) that contain in a mean( or std.  
## This will get only those features that end in mean() or std(), which
## according to this post (https://class.coursera.org/getdata-005/forum/thread?thread_id=23)
## by TA David Hood states "There are no specific marking critieria on the number of columns."
meanstd <- grep("*-mean\\(|-std*", features[,2])

## Change directory into the "test" subject data
setwd("test")

## Read in the features data
testdata <- read.table("X_test.txt")
## Read in the activity data (values 1-6 representing WALKING, WALKING_UPSTAIRS
## WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING respectively)
testactivity <- read.table("y_test.txt")
## Read in the subject data (values 1-30)
testsubject <- read.table("subject_test.txt")
## combine the activity and subject data into the features data
testdata <- cbind(testdata, testactivity)
testdata <- cbind(testdata, testsubject)

## Change directory to the train data
setwd("../train")

## Read in the features data
traindata <- read.table("X_train.txt")
## Read in the activity data (values 1-6 representing WALKING, WALKING_UPSTAIRS
## WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING respectively)
trainactivity <- read.table("y_train.txt")
## Read in the subject data (values 1-30)
trainsubject <- read.table("subject_train.txt")
## combine the activity and subject data into the features data
traindata <- cbind(traindata, trainactivity)
traindata <- cbind(traindata, trainsubject)

## Merge the test and train data (Per Step 1 of the instructions for this creating run_analysis.R)
alldata <- rbind(testdata, traindata)

## Add the last two rows to the list of columns we want to keep in meanstd
meanstd <- append(meanstd, c(562,563))
## Subset the data to just those columns (Per Step 2 of the instructions for this creating run_analysis.R)


## Factor the Activity Numbers (1-6) so they are represented by descriptive activity names
## (Per Step 3 of the instructions for this creating run_analysis.R)
subsetdata <- cbind(subtestdata, factor(subtestdata[,67],labels = c("WALKING","WALKING_UPSTAIRS","WALKING_DOWNSTAIRS","SITTING","STANDING","LAYING")))

## Add descriptive variable names (Per 4 One of the instructions for this creating run_analysis.R)


## Create a second, independent tidy data set with the average of each variable for each activity and each subject
## (Per Step 5 of the instructions for this creating run_analysis.R)
## This data adheres to the definition tidy data for this course per Week 1 "The Components of Tidy Data"
##  1. Each variable measured is in one column
##  2. Each different observation of that variable should be a different row
##  3. A row of variable names at the top is available from the write.table performed below
##  4. The variable names are human readable
## Also meeting the requirements of tidy data per this discussion, 
## https://class.coursera.org/getdata-005/forum/thread?thread_id=199


## Write data to file for submission


## Move back up to the parent directory, so the script will run correctly again if rerun

