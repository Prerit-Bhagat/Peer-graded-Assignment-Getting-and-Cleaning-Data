# Getting and Cleaning Data Course Project

This repository contains the files required for the **Getting and Cleaning Data Course Project** on Coursera. The purpose of this project is to demonstrate the ability to collect, work with, and clean a data set to prepare tidy data suitable for analysis.

## Project Overview

The dataset used in this project comes from the Human Activity Recognition (HAR) study, in which data was collected from the accelerometers on a Samsung Galaxy S smartphone. The primary objective is to process this raw data into a tidy format that can be used for further analysis, including calculating average values for various measurements.

### Dataset Source
The original dataset can be accessed [here](https://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones).  
Download link for the data: [UCI HAR Dataset](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip).

## Files in the Repository

- **run_analysis.R**: This R script performs the following steps:
  1. Merges the training and test datasets to create one unified data set.
  2. Extracts measurements on the mean and standard deviation for each measurement.
  3. Replaces activity IDs with descriptive activity names.
  4. Labels the data set with descriptive variable names.
  5. Creates a second, independent tidy data set with the average of each variable for each activity and each subject.

- **tidy_dataset.txt**: The final, tidy data set created by `run_analysis.R`. This file contains the average of each measurement variable for each activity and each subject.

- **CodeBook.md**: A code book that describes:
  - All variables and summaries calculated in the tidy dataset.
  - Units of measurement and any transformations or modifications applied during data cleaning.

- **README.md**: This document, which explains the contents of the repository, describes the purpose of the project, and provides instructions on how to run the analysis.

## Project Instructions and Requirements

The requirements for this project included:
1. **Merging** the training and test datasets to create a single dataset.
2. **Extracting** measurements on the mean and standard deviation for each measurement.
3. **Using descriptive activity names** to name the activities in the dataset.
4. **Labeling** the data set with descriptive variable names.
5. **Creating a second tidy dataset** that shows the average of each variable for each activity and each subject.

## How to Run the Analysis

To recreate the analysis and produce the `tidy_dataset.txt`, follow these steps:

1. Download the dataset from the provided link and unzip it in your working directory.
2. Clone this repository or download the `run_analysis.R` script.
3. Run the `run_analysis.R` script in R. This script will load the data, clean it, and create `tidy_dataset.txt` in your working directory.

```R
source("run_analysis.R")
