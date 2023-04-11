# Crowdfunding-ETL

## Overview
Working with Britta we extracted CSV files, transformed the data so we can easily upload to PostGres database and loaded the data into a unique database.  

## Process
#### Extract
First we Extracted the [Backer Info](https://github.com/whartzler/Crowdfunding-ETL/blob/main/Resources/backer_info.csv) dataset and did some minor transformation to get the data to be in a more structured format.  The data within the CSV was all included in one column.  

![image](https://user-images.githubusercontent.com/109490755/231193143-e8d540d4-2e0b-456e-a0fa-b72bc05086d2.png)

We converted each row into a dictionary, converted into useable dataframe then exported the dataframe file to a CSV.  
![image](https://user-images.githubusercontent.com/109490755/229884663-6ed4c2fc-0120-4074-9c45-33d747e47ade.png)

#### Transform
Once all the data extracted into a usebale database we transfored the Data.  We split out the name columns into first and last name then dropped the name column and exported the updated dataframe into a CSV.
![image](https://user-images.githubusercontent.com/109490755/229894373-60073a18-4fe2-4a04-811a-e52c20034615.png)

#### Load
To load the data we used an ERD to create various tables within [quick database designs](https://www.quickdatabasediagrams.com/) and exported the [Schema](https://github.com/whartzler/Crowdfunding-ETL/blob/main/crowdfunding_db_schema.sql) in PostGresSQL for analysis. 
![image](https://user-images.githubusercontent.com/109490755/229894884-5cc0e421-69e2-4057-8573-ef211d1f843b.png)


#### Analysis   
Finally we analyzed the tables and created queries to analyze the data.  
1. First we created a table that joined the campaign and contacts tables on ID and included with all the distinct first names, last names, email address and amount left to reach the goal for all Live projects of each contact. 
2. The Second table we created inlcuded joining two tables on ID and including the email address, first and last name of each backer, ID, company name description,end date of the campaing and remaining amount of the campaign goal.  
[Queries for SQL Analysis](https://github.com/whartzler/Crowdfunding-ETL/blob/main/crowdfunding_SQL_Analysis.sql) 

## Conclusion
There is a lot to learn in the ETL process.  The main items learned in this section was getting hands on experience of the ETL process and combining different programs together to create completed database.  


#### Files
 - Extract_Transform_final_code - Jupyter Notebook that Extracts and Transforms the backer_info.csv to be input into a SQL Database.
 - Crowdfunding_SQL_Analysis:  SQL workbook that utilized the newly created table to input into our database and queried on the results.
