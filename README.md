Getting-and-Cleaning-Data-Course-Project
========================================

The following files are part of this project:
- 1.  README.md (this file)
- 2.  Codebook.md (Description of the data set)
- 3.  run_analysis.R (creates the tidy data set)
- 4.  tidydata.txt (the output of the script, stored on Coursera)


The run_analysis.R script assumes it is placed as the same level as the "UCI HAR Dataset" directory.  As you will see in the script, the first line of code takes you into this directory.
```{r}
setwd("UCI HAR Dataset") 
```
The script read in the features.txt file in order to understand the values that the columns of the features dataset contains
```{r}
features <- read.table("features.txt")
```

In order to just use those columns that contain mean() or std() the script uses grep as follows:
```{r}
meanstd <- grep("*-mean\\(|-std*", features[,2])
```
According to this post (https://class.coursera.org/getdata-005/forum/thread?thread_id=23) by TA David Hood states "There are no specific marking critieria on the number of columns.", so including other columns that may contain the word mean is not necessary.

After moving int the test diretory the script reads in the features dataset from the X_test.txt file, the activity data (values 1-6 representing WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING respectively) from the y_test.txt file and the subject data from the subject_test.txt file.
```{r}
testdata <- read.table("X_test.txt")
testactivity <- read.table("y_test.txt")
testsubject <- read.table("subject_test.txt")
```

The activity and subject data is added to the test data using cbind, as each value in these files map to a row in the features X_test.txt file.
```{r}
testdata <- cbind(testdata, testactivity) 
testdata <- cbind(testdata, testsubject)
``` 

After moving over to the train directory the process is repeated to read in and combine the data the same way the test data was handled above, with this similar code.
```{r}
traindata <- read.table("X_train.txt")
trainactivity <- read.table("y_train.txt")
trainsubject <- read.table("subject_train.txt")
traindata <- cbind(traindata, trainactivity)
traindata <- cbind(traindata, trainsubject)
```

Next, merging the test and train data (Per Step 1 of the instructions for  creating run_analysis.R) is performed with:
```{r}
alldata <- rbind(testdata, traindata)
```
Since I added two columns to the data (sactivity and subject), I  makes sure I retain that data when I subset, so I add thoes column numbers to the subsetting vector "meanstd".
```{r}
meanstd <- append(meanstd, c(562,563))
```

Subset the data to just those columns (Per Step 2 of the instructions for creating run_analysis.R)
```{r}
subsetdata <- alldata[,meanstd]
```

Factor the Activity Numbers (1-6) so they are represented by descriptive activity name (Per Step 3 of the instructions for creating run_analysis.R)
which are available in the activity_labels.txt file
```{r}
subsetdata <- cbind(subtestdata, factor(subtestdata[,67],labels = c("WALKING","WALKING_UPSTAIRS","WALKING_DOWNSTAIRS","SITTING","STANDING","LAYING"))) 
```
The script then adds descriptive variable names (Per 4 One of the instructions for this creating run_analysis.R)
The code below is truncated since it contains 69 column names.  Please see the code book for more information.
```{r}
colnames(subtestdata) <- c("TimeBodyAcceleratorMeanX","TimeBodyAcceleratorMeanY",...
```

The second, independent tidy data set is created with the average of each variable for each activity and each subject
(Per Step 5 of the instructions for this creating run_analysis.R)
This data adheres to the definition tidy data for this course per Week 1 "The Components of Tidy Data"
- 1. Each variable measured is in one column  
- 2. Each different observation of that variable should be a different row  
- 3. A row of variable names at the top is available from the write.table   performed below
- 4. The variable names are human readable  
Also meeting the requirements of tidy data per this discussion, 
https://class.coursera.org/getdata-005/forum/thread?thread_id=199
```{r}
tidydata <- aggregate(subtestdata[,1:66], list( Activity = subtestdata$Activity, Subject = subtestdata$Subject), mean, simplify = TRUE)
```

The data is Written out to file for submission using write.table, and can be read back into R using read.table("tidydata.txt")
```{r}
write.table(tidydata, file = "tidydata.txt", row.names = FALSE)
```