First, download and unzip the data file into your R working directory.
Second, download the R source code into your R working directory.
Finally, execute R source code to generate tidy data file
## Data description
The variables in the data X are sensor signals measured with waist-mounted smartphone from 30 subjects. The variable in the data Y indicates activity type the subjects performed during recording.

## Code explaination
The code combined training dataset and test dataset, and extracted partial variables to create another dataset with the averages of each variable for each activity.

## New dataset
The new generated dataset contained variables calculated based on the mean and standard deviation. Each row of the dataset is an average of each activity type for all subjects.

## The code was written based on the instruction of this assignment
1. Read training and test dataset into R environment. 
2. Read variable names into R envrionment. 
3. Read subject index into R environment.
4. Merges the training and the test sets to create one data set. Use command rbind to combine training and test set
5. Extracts only the measurements on the mean and standard deviation for each measurement. Use grep command to get column indexes for variable name contains "mean()" or "std()"
6. Uses descriptive activity names to name the activities in the data set Convert activity labels to characters and add a new column as factor
7. Appropriately labels the data set with descriptive variable names. Give the selected descriptive names to variable columns
8. From the data set in step 7, creates a second, independent tidy data set with the average of each variable for each activity and each subject. Use pipeline command to create a new tidy dataset with command group_by and summarize_each in dplyr package

# About this R script
File with R code "run_analysis.R" perform 5 following steps (in accordance assigned task of course work):

1. Merging the training and the test sets to create one data set.
  * 1.1 Reading files
  * 1.1.1 Reading trainings tables
  * 1.1.2 Reading testing tables
  * 1.1.3 Reading feature vector
  * 1.1.4 Reading activity labels
  * 1.2 Assigning column names
  * 1.3 Merging all data in one set
2. Extracting only the measurements on the mean and standard deviation for each measurement
* 2.1 Reading column names
* 2.2 Create vector for defining ID, mean and standard deviation
* 2.3 Making nessesary subset from setAllInOne
3. Using descriptive activity names to name the activities in the data set
4. Appropriately labeling the data set with descriptive variable names
5. Creating a second, independent tidy data set with the average of each variable for each activity and each subject
* 5.1 Making second tidy data set
* 5.2 Writing second tidy data set in txt file
