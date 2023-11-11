# Writing-Functions-for-Product-Analysis

Task 1: Instructions
Write a function that takes an NPS CSV file and the source type to create a DataFrame with a column specifying the source type. A docstring describing the arguments and output of the function has been added.

Import pandas with the alias pd.
Complete convert_csv_to_df() so that it functions as the docstring describes.

Task 2: Instructions
Write a function to check if a CSV file has these three columns: response_date, user_id, and nps_rating.

Define a function check_csv() that takes one argument: the csv_name.
Open csv_name as f using with open() .
Return True if the CSV has the three specified columns, otherwise return False.
Test check_cvs() on datasets/corrupted.csv to see if it returns False.


Task 3: Instructions
Write a function that uses check_csv() and convert_csv_to_df() to convert valid files into DataFrames and combines the resulting DataFrames into one DataFrame.

Define a function combine_nps_csvs that takes a dictionary argument, csvs_dict, and iterate over csvs_dict to get the name and source type of each CSV in csvs_dict.
Use check_csv() to see if a CSV is valid.
If it is valid, use convert_csv_to_df() to convert the CSV into a DataFrame called temp and concatenate temp with combined.
If the CSV is not valid, print a message with the CSV's name.

Task 4: Instructions
Write a function categorize_nps that classifies a rating, x, into one of four categories: detractor, passives, promoters, and invalid.

Add conditional cases to check the argument x for each possible category.
Return the category of the rating as a string.

Task 5: Instructions
Write a new line of code to convert_csv_to_df() so that there is a column for each rating's NPS category.

Add a new column, nps_group which holds the result of applying categorize_nps() to the nps_rating column.
