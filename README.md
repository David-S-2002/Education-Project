# Using Data to Determine Whether ACT/SAT Scores in the U.S. are Predicted by Socioeconomic Factors

## Description
This project aims to use the data science methodology to answer a question about education inequality in the U.S.. Specifically, we will determine whether there is a relationship between average ACT scores and socioeconomic factors. We will also determine whether there is a relationship between average ACT scores and geographic location. 

I concluded that some socioeconomic factors affect ACT scores but not others. The percentage of students who qualify for free or reduced lunch is the variable that affects ACT scores the most. The percentage of students whose parents have college degrees also influences ACT scores, but not as much. The other socioeconomic variables have no relationship with ACT scores, and geographic location has no relationship with ACT scores.

We are using the EdGap dataset, which contains the average ACT/SAT scores from schools and socioeconomic information about school districts. We are also using a school information dataset from the National Center for Education Statistics. 

## Data
The EdGap data was obtained from [EdGap.org](https://www.edgap.org/#4/37.68/-95.98). The socioeconomic data is from the Census Bureau’s American Community Survey. EdGap.org states that the test score data is from the states' departments of education or another public data release. The EdGap data is in the file EdGap_data.xlsx. 

The school information data was obtained from the [National Center for Education Statistics](https://nces.ed.gov/ccd/pubschuniv.asp). The file name of the school information data is ccd_sch_029_1617_w_1a_11212017.csv. However, the file is too large for GitHub, so it can be accessed [here](https://drive.usercontent.google.com/u/0/uc?id=1HvW2w-o2XZzCm4KTvnb1Bb3BvoAa14BP&export=download).

The state population dataset contains publicly available census data from the [United States Census Bureau](https://www.census.gov/). The state population dataset is in the file state_populations.csv. 

The zip code dataset, obtained from [United States Zip Codes](https://www.unitedstateszipcodes.org/), contains demographic information, such as population, for each U.S. zip code. We will use the personal use version of their dataset. The zip code dataset is in the file zip_code_database.csv.

## Requirements
I used the following software:

- Python 3.10.11
- Google Colab
- Python libraries:
  - Pandas
  - NumPy
  - Matplotlib
  - Seaborn
  - Scikit-Learn

## Data Preparation
I took the following steps to prepare the data:
1. Exploring the contents of the datasets
2. Converting the data types of columns when necessary
3. Selecting only some columns in the school information dataset
4. Renaming the columns to be understandable, concise, and snake case
5. Performing exploratory data analysis to see if the data are suitable for answering the question
6. Joining the EdGap and school information data frames on the ID column
7. Checking for rows with out-of-range values (like negative percentages or negative ACT scores) and dropping those rows
8. Identifying missing values
9. Dropping rows with missing categorical data
10. Using Sci-kit Learn's IterativeImputer to impute the missing numerical data
11. Creating a derived variable for the percentage of people who are employed
12. Converting categorical data to a numerical representation
13. Reformatting the zip code and state population datasets and selecting only the relevant columns
14. Finding the total population in every two-digit prefix of a zip code
15. Joining the zip code dataset and the state population dataset to the clean dataset
16. Splitting the data into training and testing sets, then normalizing that data. Note that there is a training set and a test set for answering the main question, and a different training set and test set for answering the geographic location question.

The file that performs steps 1-11 is David_Stanko_data_preparation_education.ipynb. The file that performs steps 12-16 is David_Stanko_education_analysis_notebook.ipynb. The clean data files are train_data_main.csv, test_data_main.csv, train_data_geographic.csv, and test_data_geographic.csv.

## Authors:
David Stanko

## License:
This project is licensed under the MIT license.


