# ETL group project

## Team

- Amarilli Novel

- Avani Patel

## Summary

Our group built an ETL pipeline using Python, Pandas, Python dictionary methods, and regular expressions to extract and transform the data. 

We created [four CSV files](https://github.com/Amarilli/Crowdfunding_ETL/tree/main/Resources) and used them to create an [ERD](https://github.com/Amarilli/Crowdfunding_ETL/blob/main/Images/QuickDBD_diagram_Crowdfunding.png) and a [table schema](https://github.com/Amarilli/Crowdfunding_ETL/blob/main/crowdfunding_db_schema.sql). 

Finally, we uploaded the CSV file data into a Postgres database.

### Part 1

We extracted and transformed the `crowdfunding.xlsx` Excel data to create a [category DataFrame](https://github.com/Amarilli/Crowdfunding_ETL/blob/main/Resources/category.csv) that has a "category_id" column that has entries going sequentially from "cat1" to "catn", where n is the number of unique categories, and a "category" column that contains only the category titles.


### Part 2

### Part 3

Diagram

[DBD Diagram](https://github.com/Amarilli/Crowdfunding_ETL/blob/main/Images/QuickDBD_diagram_Crowdfunding.png)


![Diagram](https://github.com/Amarilli/Crowdfunding_ETL/blob/main/Images/QuickDBD_diagram_Crowdfunding.png)

### Part 4

Queries

1. category
   
![category](https://github.com/Amarilli/Crowdfunding_ETL/blob/main/Images/category_sql.png)


2. subcategory

![subcategory](https://github.com/Amarilli/Crowdfunding_ETL/blob/main/Images/subcategory_sql.png)



3. campaign

![campaign](https://github.com/Amarilli/Crowdfunding_ETL/blob/main/Images/campaign_sql.png)


4. contacts

![contacts](https://github.com/Amarilli/Crowdfunding_ETL/blob/main/Images/contacts_sql.png)

Link [title](https://www.example.com)

Image ![alt text](image.jpg)
