##Source

Source of the original data: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip  

The attached R script (run_analysis.R) performs the following 

##A.Import of files and merge

1. Merges the training and test sets to create one data set, namely

X_test and X_train merged into X_data
Y_test and Y_Train merged into Y_data
subject_Test and subject_Train into Sub_Data


##B.Transformations

Appends the label to each of the file and then merge X_data_m_s, Y_data and Sub_Data to make it as single tidy data set.

Following steps follwed:

1.Reads file features.txt and extracts only the measurements on the mean and standard deviation for each measurement.
The result is stored in X_data_m_s a 10299 x 66 data frame. All measurements appear to be floating point numbers in the range (-1, 1).

2.Reads activity_labels.txt and applies descriptive activity names to name the activities in the data set. All names() are converted into lowercase
 

3.Then it merges the 10299x66 data frame containing features with 10299x1 data frames containing activity labels and subject IDs.The result is saved as merged_tidy_data.txt, a 10299x68 data frame.


##C.Final Computation

Finally, the script creates a 2nd, independent tidy data set with the average of each measurement for each activity and each subject.

This uses melt function for transposing the data. Then uses dcast function to calcuate averages grouped on the basis of activity and subject.

The result is saved as dataset_with_averages.txt, a 180x68 data frame. There are 30 subjects and 6 activities, thus 180 rows in this dataset.
