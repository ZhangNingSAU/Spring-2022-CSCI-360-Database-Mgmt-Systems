# CSCI360 Spring 2022
# Homework 7 for Chapter 8
# due: 11:59pm 04/21/2022

# Database Description: This homework is based on the suppliers-and-parts database you created in [HW5](../Homework/HW5.md).
+ Note: Please run CreateDB.sql and LoadDB.sql to create the database and insert rows. Do NOT run AlterDB.sql.




# Step 1: Write MySQL statements for the following questions:
1. Create a table with two columns, and save the Sno and Sname for suppliers who ship red parts.<br>
+ Note: Create a table and insert Data Using Queries or create a table and copy some data<br>
2. Download the [artists_and_albums.csv](https://raw.githubusercontent.com/ZhangNingSAU/Spring-2022-CSCI-360-Database-Mgmt-Systems/main/Resources/artists_and_albums.csv), create a table, then load the data from artists_and_albums.csv into the table.<br>
+ Note: 
  -  If you are using Mac OS, download the csv file in the `htdocs` folder.
  -  If you are using Windows OS, you need to

    + 1. create a database/or use an existing one

    + 2. use that database

    + 3. create a table with two columns, and the data types should be compatible with the content of the csv file

    + 4. put the artists_and_albums.csv file in the folder C:\xampp\mysql\data\my_db (note that my_db is the database I created, you need to replace it with your own database name) 

5. run the LOAD DATA INFILE command, and provide the file name  'artists_and_albums.csv' directly. (no need to provide the full path) 
4. Save the part information for all parts shipped by more than one supplier into a csv file.<br>
+ Note: Better to save the csv file in `htdocs` folder.<br>
5. Find the shipments by Sname `Smith`, and increase the price by 0.001<br>
+ Note: for the `SET` clause, use `SET Price=Price+0.001`<br>
6. Delete the shipments by Sname `Smith`.<br>
7. Replace s5's city with `Rome`<br>
+ note: use `Replace` clause<br>

# Step 2: Save all the statements in a file, name it as CSCI360_Homework7_JohnDoe(0123456).sql
+ Note: 
  - Place comments before each query(use “--” (double minus) to comment one line), e.g.:
  ~~~~
  -- 1. Create a table with two columns, and save the Sno and Sname for suppliers who ship ONLY red parts.
  your statement here
  ~~~~

# Step 3: Submit your work on [Blackboard](https://blackboard.sau.edu/webapps/login/)
