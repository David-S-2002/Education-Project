# Using Data to Determine Whether ACT/SAT Scores in the U.S. are Predicted by Socioeconomic Factors

## Project Purpose
This project aims to use the data science methodology to answer a question about education inequality in the U.S.. Specifically, we will determine whether there is a relationship between average ACT/SAT scores and socioeconomic factors. We are using the EdGap dataset, which contains the average ACT/SAT scores from schools and socioeconomic information about school districts. We are also using a school information dataset from the National Center for Education Statistics. 

## Data
The EdGap data was obtained from [EdGap.org](https://www.edgap.org/#4/37.68/-95.98). The socioeconomic data is from the Census Bureau’s American Community Survey. EdGap.org states that the test score data is from the states' departments of education or another public data release. The EdGap data is in the EdGap_data.xlsx. 

The school information data was obtained from the [National Center for Education Statistics](https://nces.ed.gov/ccd/pubschuniv.asp). The file name of the school information data is ccd_sch_029_1617_w_1a_11212017.csv. However, the file is too large for GitHub, so it can be accessed [here](https://drive.usercontent.google.com/u/0/uc?id=1HvW2w-o2XZzCm4KTvnb1Bb3BvoAa14BP&export=download).

## Data Preparation
I took the following steps to prepare the data:
- Exploring the contents of the datasets
- Converting the data types of columns when necessary
- Selecting only some columns in the school information dataset
- Renaming the columns to be understandable, concise, and snake case
- Performing exploratory data analysis to see if the data are suitable for answering the question
- Joining the EdGap and school information data frames on the ID column
- Checking for rows with out-of-range values (like negative percentages or negative ACT scores) and dropping those rows
- Identifying missing values
- Dropping rows with missing categorical data
- Using Sci-kit Learn's IterativeImputer to impute the missing numerical data
- Creating a derived variable for the percentage of people who are employed
- Splitting the data into training and testing sets
- Exporting the training and testing sets

The file that performs the data preparation is David_Stanko_data_preparation_education.ipynb. The clean data files are train_data.csv and test_data.csv.
