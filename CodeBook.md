# Code Book for Getting and Cleaning Data Course Project

This code book describes the variables, data, and transformations used in the **Getting and Cleaning Data Course Project**.

## Source Data

The original dataset, the **Human Activity Recognition Using Smartphones** dataset, was collected from the accelerometers of Samsung Galaxy S smartphones. The dataset is available [here](https://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones).

## Variables in the Tidy Dataset

The tidy dataset (`tidy_dataset.txt`) contains the following variables:

1. **subjectId**: An identifier for each subject in the experiment, ranging from 1 to 30.
2. **activityId**: An identifier linking each record to an activity label.
3. **activityLabel**: Descriptive name of the activity performed by the subject. Activities include:
   - WALKING
   - WALKING_UPSTAIRS
   - WALKING_DOWNSTAIRS
   - SITTING
   - STANDING
   - LAYING

### Measurement Variables

The remaining columns are numeric variables representing the average values of each feature for each subject and activity. These include mean and standard deviation measurements for both time-domain and frequency-domain signals. Example variables are as follows:

- **tBodyAcc-mean()-X**: Mean of body acceleration in the X direction (time-domain)
- **tBodyAcc-std()-Y**: Standard deviation of body acceleration in the Y direction (time-domain)
- **fBodyGyro-mean()-Z**: Mean of body gyroscope measurements in the Z direction (frequency-domain)

### Units of Measurement

The units for all accelerometer and gyroscope measurements are:
- **Accelerometer**: Standard gravity units 'g'
- **Gyroscope**: Radians per second

## Transformations and Cleaning Steps

The data transformation process, performed in the `run_analysis.R` script, includes the following steps:

1. **Merging Data**: The training and test datasets were merged to create a single dataset.
2. **Extracting Relevant Measurements**: Only measurements on the mean and standard deviation for each measurement were extracted.
3. **Applying Descriptive Activity Names**: Activity labels were used to replace activity IDs for clarity.
4. **Labeling with Descriptive Variable Names**: Variable names were made descriptive by replacing abbreviations (e.g., "Acc" with "Accelerometer") and clarifying domain origin (e.g., "t" for time-domain and "f" for frequency-domain).
5. **Creating a Tidy Dataset**: From the cleaned data, a second dataset was created with the average of each variable for each activity and each subject.

## Notes

- Missing values: The dataset has no missing values.
- The data has been reshaped into a tidy format, where each row represents a unique combination of a subject and activity, and each column is a different measurement.

This tidy dataset provides a summary of the original data, making it suitable for further analysis.
