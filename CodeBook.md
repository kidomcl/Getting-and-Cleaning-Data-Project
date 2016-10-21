##Process for Successful Execution of Code

You have to download sourse data from link below and unzip it to working directory of R Studio.
You have to perform R script.
About source data

As sourse data for work was used Human Activity Recognition Using Smartphones Data Set. A full description is available at the site where the data was obtained: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones Here are the data for the project: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

##About R script

File with R code "run_analysis.R" perform 5 following steps (in accordance assigned task of course work):<br />
1. Merging the training and the test sets to create one data set.<br />
1.1 Reading files<br />
1.1.1 Reading trainings tables<br />
1.1.2 Reading testing tables<br />
1.1.3 Reading feature vector<br />
1.1.4 Reading activity labels<br />
1.2 Assigning column names<br />
1.3 Merging all data in one set<br />
2. Extracting only the measurements on the mean and standard deviation for each measurement<br />
2.1 Reading column names<br />
2.2 Create vector for defining ID, mean and standard deviation<br />
2.3 Making nessesary subset from setAllInOne<br />
3. Using descriptive activity names to name the activities in the data set<br />
4. Appropriately labeling the data set with descriptive variable names<br />
5. Creating a second, independent tidy data set with the average of each variable for each activity and each subject<br />
5.1 Making second tidy data set<br />
5.2 Writing second tidy data set in txt file<br />

NOTE : The code takes for granted all the data is present in the same folder, un-compressed and without names altered.

##About variables:<br />

x_train, y_train, x_test, y_test, subject_train and subject_test contain the data from the downloaded files.<br />
x_data, y_data and subject_data merge the previous datasets to further analysis.<br />
features contains the correct names for the x_data dataset, which are applied to the column names stored<br />
activity_labels contains the data downloaded from the file<br />
merge_train contains the merged training data<br />
merge_test contains the merged test data<br />
SetAllInOne contains the merge_train  and merge_test data <br />
ColNames stores the SetAllInOne data into new table<br />
mean_and_std contains the following vectors(activityId, SubjectId, mean..,std..) from ColNames<br />
setForMeanAndStd contains the sorted data as per mean_and Std<br />
setWithActivityNames contains the merge data of setForMeanAndStd and activity_list<br />
secTidySet contains the aggregated data as per activityId and subjectId and then it is ordered in ascending order as per subjectID<br />
