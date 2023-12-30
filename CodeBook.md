# Introduction

The `run_analysis.R` script executes the 5 steps outlined in the course project's definition.

* Initially, the script combines data with similar characteristics using the `rbind()` function. When we say similar, we are referring to files with identical column numbers that pertain to the same entities.
* Subsequently, only those columns containing mean and standard deviation measures are extracted from the entire dataset. After this extraction, the columns are appropriately named based on the information in `features.txt`.
* Since activity data is represented by values 1:6, we extract activity names and IDs from `activity_labels.txt` and substitute them into the dataset.
* Corrections are made to columns with ambiguous names in the overall dataset.
* Lastly, a new dataset is generated, containing average measures for each subject and activity type (180 rows). The resulting file is named `TidyDataF.txt` and is uploaded to this repository.

# Variables

* The datasets `x_train`, `y_train`, `x_test`, `y_test`, `subject_train`, and `subject_test` store data from the downloaded files.
* `x_data`, `y_data`, and `Merged_Data` combine the aforementioned datasets for further analysis.
* The variable `features` holds the correct names for the `x_data` dataset, and these names are applied to the column names stored in `TidyData`, a numeric vector used to extract the desired data.
* A comparable methodology is applied to activity names using the variable `activities`.
* Finally, `FinalData` encompasses the pertinent averages, which will subsequently be stored in a `.txt` file.
