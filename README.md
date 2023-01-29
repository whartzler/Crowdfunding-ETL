# Crowdfunding-ETL

## Overview
Working with Britta we extracted CSV files, transformed the data so we can easily upload to PostGres database and loaded the data into a unique database.  

## Process
Transforming the crowdfunding excel spreadsheet we split out the information into 5 seperate CSV files.  In the Contact info tab in the original crowdfunding CSV the data was all included in one line we had to write code to extract the data and transform it into a useable CSV.  Once all the data was reviewed to make sure we didnt miss anything we created and ERD to easily upload the data into PostGres. Once the data was uplaoded into PostGres we validated the data was uploaded correctly.  Finally we created some additional queries to display the email contacts that have live outcomes the remaining goal amount and the backers their reamining goal amount.

## Conclusion
There is a lot to learn in the ETL process.  The main items learned in this section was getting hands on experience of the ETL process and combining different programs together to create completed database.  


#### Files
 - Extract_Transform_final_code - Jupyter Notebook that Extracts and Transforms the backer_info.csv to be input into a SQL Database.
 - Crowdfunding_SQL_Analysis:  SQL workbook that utilized the newly created table to input into our database and queried on the results.
