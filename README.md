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
The data used were created by myself for an [earlier](https://github.com/jessicahoganma/SQL_hospital_Project) project. All of the participant names were created using [Fake Name Generator](https://www.fakenamegenerator.com/gen-random-us-us.php).

# Table of Contents
1. Library Import  
1.1 Library Import  
2. Connect to Server and Create Database  
2.1 Define Server Connection Function  
2.2 Create a New Database  
2.3 Modify Server Connection Function, Create Database Connection Function  
2.4 Define Query Execution Function  
3. Creating Tables  
3.1 Create Tables  
3.2 Define Foreign Key Relationships  
4. Populating Tables  
4.1 Populate Tables  
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

### 1. Import Libraries  
1.1 - Import Libraries  
The first step is to import [MYSQL Connector](https://dev.mysql.com/doc/connector-python/en/) and [pandas](https://pandas.pydata.org/)  
![Screen Shot 2022-03-18 at 9 29 19 PM](https://user-images.githubusercontent.com/98434176/159106756-e43317c6-8d5e-4488-a85c-4625abb74dec.png)

### 2. Connect to Server and Create Database  
2.1 - Define Server Connection Function  
Next I defined a function in python which connects to our MySQL Server  
![Screen Shot 2022-03-18 at 9 33 03 PM](https://user-images.githubusercontent.com/98434176/159106869-efcf1f73-1772-409a-8345-69cae0277b51.png)  
![Screen Shot 2022-03-18 at 9 33 57 PM](https://user-images.githubusercontent.com/98434176/159106899-1cb1dd60-f154-42a6-beb9-cb2a84f40f52.png)  
![Screen Shot 2022-03-18 at 9 34 22 PM](https://user-images.githubusercontent.com/98434176/159106912-7d8370cf-898a-4da4-ac53-806578cc8ece.png)  

2.2 - Create a New Database
Then I defined a function to create a new database on the server. Here I used cursor.execute() to execute a CREATE DATABASE SQL command.  
![Screen Shot 2022-03-18 at 9 37 06 PM](https://user-images.githubusercontent.com/98434176/159107034-d28ee345-040c-4688-898d-d49bb48756e5.png)  
![Screen Shot 2022-03-18 at 9 38 53 PM](https://user-images.githubusercontent.com/98434176/159107055-65e67e41-06aa-47e4-84cb-ca8d181f816a.png)  
2.3 - Modify Server Connection Function, Create Database Connection Function  
Now that the database has been created, I modified the create_server_connection function to create a new function for connecting directly to that database  
![Screen Shot 2022-03-18 at 9 42 01 PM](https://user-images.githubusercontent.com/98434176/159107160-c4722526-9d97-4a43-ac9e-bc4addbe134c.png)  

2.4 - Define Query Execution Function
The final step of this stage is to create a function which will allow us to execute queries written in SQL.  
![Screen Shot 2022-03-18 at 9 59 44 PM](https://user-images.githubusercontent.com/98434176/159107587-c9bd3be9-ef99-45e1-ad56-b37b98dddafb.png)

### 3.Creating Tables  
3.1 Creating Tables  
![Screen Shot 2022-03-18 at 10 16 54 PM](https://user-images.githubusercontent.com/98434176/159108014-726ec890-dcfd-427d-b8b0-b2ac90c806ce.png)  
3.2 Define Foreign Key Relationships  
![Screen Shot 2022-03-18 at 10 20 18 PM](https://user-images.githubusercontent.com/98434176/159108124-111b24ef-3d90-4065-8c36-8aad9a9e18da.png)
 
### 4. Populating Tables  
4.1 Populate Tables  
