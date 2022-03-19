# Python_SQL
This notebook uses the MySQL Connector and Python to implement a database on MySQL Server, and to create, read, update and delete data in that database.
## About
The notebook takes the reader step-by-step through all the processes involved with using Python and the MySQL Connector to perform the standard CRUD functions on a database running on MySQL Server.

I implemented the same code to build the below database using data from [this](https://github.com/jessicahoganma/SQL_hospital_Project) previous project, but this time I did it doing it via Python using MySQL Connector.

![Hospital Database ERD](https://user-images.githubusercontent.com/98434176/159106140-f85d0a51-3298-4388-8af9-cb4470ec8503.png)



# Methods Used
Defining functions in Python  
Database Implementation  
Creating, Reading, Updating and Deleting data using SQL and Python  
# Technologies Used
[MySQL Community Server](https://dev.mysql.com/downloads/mysql/)  
[MySQL Python Connector](https://dev.mysql.com/doc/connector-python/en/)  
[PopSQL](https://popsql.com/)  
[Jupyter Notebook](https://jupyter.org/)  
[pandas](https://pandas.pydata.org/)  
# Data Sources
The data used were created by myself for an [earlier](https://github.com/jessicahoganma/SQL_hospital_Project) project. Some participant names were created using [Fake Name Generator](https://www.fakenamegenerator.com/gen-random-us-us.php).

# Table of Contents
1. Library Import  
1.1 Library Import  
2. Connect to Server and Create Database  
2.1 Define Server Connection Function  
2.2 Create a New Database  
2.3 Modify Server Connection Function, Create Database Connection Function  
2.4 Define Query Execution Function  
3. Creating Tables  
3.1 Create Teacher Table  
3.2 Create Remaining Tables  
3.3 Define Foreign Key Relationships  
4. Populating Tables  
4.1 Populate Teacher Table  
4.2 Populate Remaining Tables  
5. Reading Data  
5.1 Define Data Reading Function  
5.2 - Read Data from Database  
5.3 - Formatting Output into a List  
5.4 - Formatting Output into a List of Lists  
5.5 - Formatting Output into a pandas DataFrame  
6. Updating Records  
6.1 Updating Client Address  
7. Deleting Records  
7.1 Deleting a Course  
7.2 Restoring the Course  
8. Creating Records from Lists  
8.1 Create Execute List Query Function  
8.2 Add New Teachers  
9. Conclusion  
9.1 Conclusion  

1. Import Libraries 
2. 1.1 - Import Libraries  
3. Our first stel is to import [MYSQL Connector](https://dev.mysql.com/doc/connector-python/en/) and [pandas](https://pandas.pydata.org/) 
