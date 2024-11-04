# LITA-CLASS-DOCUMENTATION 

Project Overview

The purpose of this project is to clean the dataset to ensure accuracy, consistency and it been usable for various applications and analysis.
Data source
The data was collected from the HR Information desk.
The dataset includes the following data:
-	Text Extraction
•	Code
-	Text Cleaning 1 
•	Names
•	Company 
•	Salary
-	Text Cleaning  2
•	Names
-	Text Cleaning  3
•	First name
•	Surname
•	Text Cleaning  4
•	Email addresses and Names.
Project Objective
The objective of this project is to handle missing information in Text Extraction Data and also to make sure the names of the staffs are written accurately.
Data Tools and Methods Used
Microsoft Excel was used to clean the data using the whole
i.	Exploring the data to understand the structure and what is expected to be in the dataset 
ii.	Identify the issues that need to addressed such as missing data, names and emails.
iii.	Deciding on the strategy to address the missing data.
iv.	Ensuring consistent capitalizing and spacing in the names and emails.

Formulars Used
Text Extraction Data
A description was given in the data on how to extract the Department, Purchase Date and Asset Category Codes from the Codes Column.
The data for the first codes were found using the following formulars and flash fill was used to fill the rest of the cells.

```LEFT(B10,2)``` -  Used to extract the Department codes from the Codes Column 

```MID(B10,3,6)``` -  Used to extract the Purchase Date codes from the Codes Column

```RIGHT(B10,4)``` -  Used to extract the Asset Category Code from the Codes Column


Text Cleaning 1 Data
```TRIM(B6)``` -  Used to eliminate unnecessary spaces from the names 
```UPPER(E6)``` - Used to enter the names in Uppercase
```LOWER(E6)``` - Used to enter the names in lowercase
```PROPER(E6)``` - Used to properly enter the names
```TRIM(PROPER(B6))``` – Used to properly enter the names and eliminate spaces
```PROPER(C6) – To enter the company names properly

Text Cleaning 2 Data
```LEFT(B6,FIND(" ",B6))``` - To extract the first names from the full names.
```RIGHT(B6,LEN(B6)-FIND(" ",B6))``` - To extract the surnames from the full names.
```LOWER(C6&"@lita.org") ```– To enter the first name with an email, forming an email address.

Text Cleaning 3
```B6&" "&C6```- To join the first name and the surname together to form a full name.

Text Cleaning 4
```LEFT(B6,FIND(".",B6)-1)```- Extracting the First name from the email address


