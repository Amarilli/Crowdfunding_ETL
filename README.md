# ETL group project

## Team

- Amarilli Novel

- Avani Patel

## Summary

Our group built an ETL pipeline using Python, Pandas, Python dictionary methods, and regular expressions to extract and transform the data. 

We created [four CSV files](https://github.com/Amarilli/Crowdfunding_ETL/tree/main/Resources) and used them to create an [ERD](https://github.com/Amarilli/Crowdfunding_ETL/blob/main/Images/QuickDBD_diagram_Crowdfunding.png) and a [table schema](https://github.com/Amarilli/Crowdfunding_ETL/blob/main/crowdfunding_db_schema.sql). 

Finally, we uploaded the CSV file data into a Postgres database.

### Part 1: The Category and Subcategory DataFrames

We extracted and transformed the `crowdfunding.xlsx` Excel data to create a [category DataFrame](https://github.com/Amarilli/Crowdfunding_ETL/blob/main/Resources/category.csv) that had a "category_id" column that had entries going sequentially from "cat1" to "catn", where n was the number of unique categories and a "category" column that contains only the category titles.


### Part 2: The Campaign DataFrame

We extracted and transformed the `crowdfunding.xlsx` Excel data to create a campaign DataFrame that has the following columns:

- The "cf_id" column

- The "contact_id" column

- The "company_name" column

- The "blurb" column, renamed to "description"

- The "goal" column, converted to the float data type

- The "pledged" column, converted to the float data type

- The "outcome" column

- The "backers_count" column

- The "country" column

- The "currency" column

- The "launch_date" column converted to the `datetime` format

- The "end_date" column converted to the `datetime` format

- The "category_id" column, with unique identification numbers matching those in the "category_id" column of the category DataFrame

- The "subcategory_id" column, with the unique identification numbers matching those in the "subcategory_id" column of the subcategory DataFrame

We exported the campaign DataFrame as `campaign.csv` and saved it to our GitHub repository.


### Part 3: The Contacts DataFrame

We extracted and transformed the data from the `contacts.xlsx` Excel data, choosing both options: 

- Option 1: Python dictionary methods.

- Option 2: Use regular expressions.

For *Option 1*, we imported the `contacts.xlsx` file into a DataFrame. We iterated through the DataFrame, converting each row to a dictionary.

Then, we iterated through each dictionary, extracting the dictionary values from the keys by using a Python list comprehension and adding the values for each row to a new list.

Then, we created a new DataFrame that contains the extracted data.

Also, we split each "name" column value into a first and last name and placed each in a new column.

Ultimately, we cleaned and exported the DataFrame as `contacts.csv` and saved it to our GitHub repository.

For *Option 2*, we imported the `contacts.xlsx` file into a DataFrame. Then, we extracted the "contact_id," "name," and "email" columns by using regular expressions.

We created a new DataFrame with the extracted data.

Also, we converted the "contact_id" column to the integer type, and we split each "name" column value into a first and a last name and placed each in a new column.

Ultimately, we cleaned and exported the DataFrame as `contacts.csv` and saved it to our GitHub repository.

### Part 4: The Crowdfunding Database

 We inspected the four CSV files and then sketched an ERD of the tables by using QuickDBDLinks to an external site.

 ![Diagram](https://github.com/Amarilli/Crowdfunding_ETL/blob/main/Images/QuickDBD_diagram_Crowdfunding.png)

We used the information from the ERD to create a table schema for each CSV file.

We saved the database schema as a Postgres file named `crowdfunding_db_schema.sql` and saved it to our GitHub repository.

Then, we created a new Postgres database named `crowdfunding_db`.

We created the tables in the correct order to handle the foreign keys and verified the table creation by running a `SELECT` statement for each table.

Finally, we imported each CSV file into its corresponding SQL table.

1. category
   
![category](https://github.com/Amarilli/Crowdfunding_ETL/blob/main/Images/category_sql.png)


2. subcategory

![subcategory](https://github.com/Amarilli/Crowdfunding_ETL/blob/main/Images/subcategory_sql.png)



3. campaign

![campaign](https://github.com/Amarilli/Crowdfunding_ETL/blob/main/Images/campaign_sql.png)


4. contacts

![contacts](https://github.com/Amarilli/Crowdfunding_ETL/blob/main/Images/contacts_sql.png)


