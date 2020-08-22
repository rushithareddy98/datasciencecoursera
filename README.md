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
# Tidy data set description
## The variables in the tidy data
Tidy data contains 180 rows and 68 columns. Each row has averaged variables for each subject and each activity.

## Only all the variables estimated from mean and standard deviation in the tidy set were kept.
mean(): Mean value
std(): Standard deviation
##The data were averaged based on subject and activity group.
Subject column is numbered sequentially from 1 to 30. Activity column has 6 types as listed below.

1. WALKING
2. WALKING_UPSTAIRS
3. WALKING_DOWNSTAIRS
4. SITTING
5. STANDING
6. LAYING
## The tidy data contains 6 rows (averaged based on activity) and 68 columns (66 variables and activity labels).
1. "activitylabel"
2. "subject"
3. "tBodyAcc-mean()-X"
4. "tBodyAcc-mean()-Y"
5. "tBodyAcc-mean()-Z"
6. "tBodyAcc-std()-X"
7. "tBodyAcc-std()-Y"
8. "tBodyAcc-std()-Z"
9. "tGravityAcc-mean()-X"
10. "tGravityAcc-mean()-Y"
11. "tGravityAcc-mean()-Z"
12. "tGravityAcc-std()-X"
13. "tGravityAcc-std()-Y"
14. "tGravityAcc-std()-Z"
15. "tBodyAccJerk-mean()-X"
16. "tBodyAccJerk-mean()-Y"
17. "tBodyAccJerk-mean()-Z"
18. "tBodyAccJerk-std()-X"
19. "tBodyAccJerk-std()-Y"
20. "tBodyAccJerk-std()-Z"
21. "tBodyGyro-mean()-X"
22. "tBodyGyro-mean()-Y"
23. "tBodyGyro-mean()-Z"
24. "tBodyGyro-std()-X"
25. "tBodyGyro-std()-Y"
26. "tBodyGyro-std()-Z"
27. "tBodyGyroJerk-mean()-X"
28. "tBodyGyroJerk-mean()-Y"
29. "tBodyGyroJerk-mean()-Z"
30. "tBodyGyroJerk-std()-X"
31. "tBodyGyroJerk-std()-Y"
32. "tBodyGyroJerk-std()-Z"
33. "tBodyAccMag-mean()"
34. "tBodyAccMag-std()"
35. "tGravityAccMag-mean()"
36. "tGravityAccMag-std()"
37. "tBodyAccJerkMag-mean()"
38. "tBodyAccJerkMag-std()"
39. "tBodyGyroMag-mean()"
40. "tBodyGyroMag-std()"
41. "tBodyGyroJerkMag-mean()"
42. "tBodyGyroJerkMag-std()"
43. "fBodyAcc-mean()-X"
44. "fBodyAcc-mean()-Y"
45. "fBodyAcc-mean()-Z"
46. "fBodyAcc-std()-X"
47. "fBodyAcc-std()-Y"
48. "fBodyAcc-std()-Z"
49. "fBodyAccJerk-mean()-X"
50. "fBodyAccJerk-mean()-Y"
51. "fBodyAccJerk-mean()-Z"
52. "fBodyAccJerk-std()-X"
53. "fBodyAccJerk-std()-Y"
54. "fBodyAccJerk-std()-Z"
55. "fBodyGyro-mean()-X"
56. "fBodyGyro-mean()-Y"
57. "fBodyGyro-mean()-Z"
58. "fBodyGyro-std()-X"
59. "fBodyGyro-std()-Y"
60. "fBodyGyro-std()-Z"
61. "fBodyAccMag-mean()"
62. "fBodyAccMag-std()"
63. "fBodyBodyAccJerkMag-mean()"
64. "fBodyBodyAccJerkMag-std()"
65. "fBodyBodyGyroMag-mean()"
66. "fBodyBodyGyroMag-std()"
67. "fBodyBodyGyroJerkMag-mean()"
68. "fBodyBodyGyroJerkMag-std()"
# variable units
Activity variable is factor type. Subject variable is integer type. All the other variables are numeric type.

