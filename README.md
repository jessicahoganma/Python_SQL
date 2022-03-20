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
The final step of this stage is to create a function which will allows you to execute queries written in SQL.  
![Screen Shot 2022-03-18 at 9 59 44 PM](https://user-images.githubusercontent.com/98434176/159107587-c9bd3be9-ef99-45e1-ad56-b37b98dddafb.png)

### 3.Creating Tables  
3.1 Creating Tables  
![Screen Shot 2022-03-19 at 9 02 29 PM](https://user-images.githubusercontent.com/98434176/159147572-d971cb97-f131-4be1-b334-f46d32b543f4.png)

3.2 Define Foreign Key Relationships  
![Screen Shot 2022-03-19 at 9 05 11 PM](https://user-images.githubusercontent.com/98434176/159147620-46071a46-bd22-4263-86b3-36bb57de367a.png)

 
### 4. Populating Tables  
4.1 Populate Tables  
![Screen Shot 2022-03-19 at 9 03 21 PM](https://user-images.githubusercontent.com/98434176/159147589-8accc010-23cb-461d-956e-202855ac0e1d.png)
![Screen Shot 2022-03-19 at 8 42 08 PM](https://user-images.githubusercontent.com/98434176/159147108-82fb168e-7694-4a29-86db-85d78ee50a6f.png)
![Screen Shot 2022-03-19 at 8 42 22 PM](https://user-images.githubusercontent.com/98434176/159147110-584305c7-dd8f-4bb9-bc1d-8bc5c8ea20a6.png)
![Screen Shot 2022-03-19 at 9 03 52 PM](https://user-images.githubusercontent.com/98434176/159147597-06d768b4-f73e-4511-8e24-227a82410aa2.png)


### 5. Reading Data   
5.1 In order to create read queries, a new function will be needed   
![Screen Shot 2022-03-18 at 11 15 50 PM](https://user-images.githubusercontent.com/98434176/159109791-519331a7-e4ef-43df-89f8-b1565d22c4c7.png)

5.2 Read Data from Database   
![Screen Shot 2022-03-18 at 11 19 16 PM](https://user-images.githubusercontent.com/98434176/159109951-6c57f94e-5012-4f1b-943a-927c94f23227.png)   
![Screen Shot 2022-03-19 at 10 14 31 PM](https://user-images.githubusercontent.com/98434176/159149228-d4c0c328-0530-4317-a100-6901713f560c.png)
![Screen Shot 2022-03-19 at 10 48 17 PM](https://user-images.githubusercontent.com/98434176/159149984-f13d777d-0718-47c9-a5de-ac4b214af4de.png)

5.3 - Formatting Output into a List  
Now results can be added to a list of tuples
![Screen Shot 2022-03-19 at 10 55 55 PM](https://user-images.githubusercontent.com/98434176/159150167-327b5d07-211c-4b43-a4da-ecbfe2709497.png)
![Screen Shot 2022-03-19 at 10 58 37 PM](https://user-images.githubusercontent.com/98434176/159150250-044f67ad-7b8f-4e3c-944a-a7f9faf91392.png)

5.4 - Formatting Output into a List of Lists
Returning a list of lists 
![Screen Shot 2022-03-19 at 11 00 15 PM](https://user-images.githubusercontent.com/98434176/159150293-cdcfdb66-9050-45db-97bb-60de57b36946.png)

5.5 - Formatting Output into a pandas DataFrame  
Creating a pandas DataFrame  
![Screen Shot 2022-03-19 at 11 15 08 PM](https://user-images.githubusercontent.com/98434176/159150617-07be990d-508b-4c09-ac3e-ac0915bc7aea.png)

6. Updating Records  
6.1 - Updating Patient Address  
A hospital has moved locations, and now located at 23 Fingiertweg, 14534 Berlin. We can change that in our database like so:  
![Screen Shot 2022-03-19 at 11 16 11 PM](https://user-images.githubusercontent.com/98434176/159150646-eaac5f8e-a7a8-4e60-bd84-641786c81892.png)

7. Deleting Records  
7.1 - Deleting a Course  
We can also use our execute_query function to delete records, by using DELETE FROM.  

Let's try this with our course table. First let's remind ourselves of the courses contained in the table.


