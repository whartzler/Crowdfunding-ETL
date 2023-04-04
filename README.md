# Crowdfunding-ETL

## Overview
Working with Britta we extracted CSV files, transformed the data so we can easily upload to PostGres database and loaded the data into a unique database.  

## Process
First we Extracted the [Backer Info](https://github.com/whartzler/Crowdfunding-ETL/blob/main/Resources/backer_info.csv) dataset and performed some transformation.  The data within the CSV was all in one column.  We converted each row into a dictionary, converted into useable dataframe then exported the dataframe file to a CSV.  
![image](https://user-images.githubusercontent.com/109490755/229884663-6ed4c2fc-0120-4074-9c45-33d747e47ade.png)

Once all the data extracted into a usebale database we transfored the Data.  We split out the name columns into first and last name then dropped the name column and exported the updated dataframe into a CSV.
![image](https://user-images.githubusercontent.com/109490755/229894373-60073a18-4fe2-4a04-811a-e52c20034615.png)

Using an ERD we created various tables within [quick database designs]9https://www.quickdatabasediagrams.com/) and exported the [Schema](https://github.com/whartzler/Crowdfunding-ETL/blob/main/crowdfunding_db_schema.sql) to be uploaded in PostGresSQL. 
![image](https://user-images.githubusercontent.com/109490755/229894884-5cc0e421-69e2-4057-8573-ef211d1f843b.png)


was reviewed to make sure we didnt miss anything we created and ERD to easily upload the data into PostGres. Once the data was uplaoded into PostGres we validated the data was uploaded correctly.  Finally we created some additional queries to display the email contacts that have live outcomes the remaining goal amount and the backers their reamining goal amount.

## Conclusion
There is a lot to learn in the ETL process.  The main items learned in this section was getting hands on experience of the ETL process and combining different programs together to create completed database.  


#### Files
 - 
 - Extract_Transform_final_code - Jupyter Notebook that Extracts and Transforms the backer_info.csv to be input into a SQL Database.
 - Crowdfunding_SQL_Analysis:  SQL workbook that utilized the newly created table to input into our database and queried on the results.
