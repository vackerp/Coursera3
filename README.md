===========================================

This script should be run from the indicated directory (setwd()). Related data files should be downloaded into the working directors where the script is used and unziped. The URL of the source zip files is indicated.




This file explains how the scripts run_analysis.R of this repo work.

The R script `run_analysis.R` c process the required data. Then, it creates two new tidy data sets:

- `merged_data.txt` : combines training and test data sets (together with subject and activity data).

- `means.txt` : aggregates the aforementioned data by subject and activity (the mean of multiple trials for each feature is taken).


====================
## Source

Information about used data in: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

Used data set: [zip file](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip) 
