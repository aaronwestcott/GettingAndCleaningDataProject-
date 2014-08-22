GettingAndCleaningDataProject-
==============================

The analysis steps performed are as follows (The numbers match the code):
1. All files are read into R.
  X_train.txt
  X_test.txt
  features.txt
  activity_labels.txt
  subject_test.txt
  y_test.txt
  y_train.txt
  subject_test.txt
  subject_train.txt
  activity_labels.txt

2. Using rbind, concatonate the the X_train to X_Test, Y_Train to Y_TEst and subject_train to subject_test data together one set on top of the other.
3. MErge the activity labels o the the Y data and simply grab the full text names of the activities
4. Column bind the subjects to the activities
5. Extracted all teh feature names from the full features set into a logical list  with true for any column name that had mean in it into a list
6. Extracted all teh feature names from the full features set into a logical list with true for any column name that had std in it into a list
7. subsetted the full the X data into 2 data sets.  One containing only columns with mean and the other with std.  
8. Grabbed the full featuer names for both mean and std
9. Cleaned up the names of the features to be more readable
10. renamed the columns of the std and mean data sets
11. bound the mean and std data sets together leaving only 81 features out of the full feature set.
12. bound the subject and activites to the data set of mean and std features
13. rename the subject and activity columns
14. ensure that all columns are numeric
15. calculate the means for all the columns by combinations of subject and activity
16. remove any superfluous columns created by the aggregation (honestly have no idea why it did this)
17. Sortht he data by subject and activity for readibility
18. 18 Write the file out
