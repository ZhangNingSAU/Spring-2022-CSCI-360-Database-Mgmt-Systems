# CSCI360 Spring 2022
# Homework 3 for Chapter 5 Part I
# due: 11:59pm 02/22/2022

# Database: this homework is based on the MUSIC database in the textbook.
+ Note: Make sure that you reload the music database(the batch mode command) once before executing the following sql statements.
# Queries
1. Print the column information in table **played**.<br>
2. Print the artist names. <br>
3. Print the id and name for each album. <br>
4. Print the album id, track id, and the played date and time for the tracks that were played before August 15, 2006. <br>
5. Print the name and time for the 5th track in the album with id=5.<br>
6. Print the information for tracks that start with 'L' and end with 't'. <br>
7. Print the information for albums that have letter 't' as the third character.<br>
8. Print the track information of artist with id = 1, order the result by album in acsending and time in descending.<br>
9. Print the information for the first 3 artists.<br>
10. Print the information for the 5 tracks that were played recently.<br>


+ Note: You can use the ER models to help you understand the structure of the database.
+ Note: No JOIN operation is needed.

![](/Resources/4-musicer.png)

![](/Resources/5-musicer2.png)

# Step 1: Complete Q1-Q10, and save your queries and results in two separate files.
1. Queries.sql, which contains all the sql statements. Please specify the numbers of questions, here is one sample file(double minus is used for comments).
~~~~
-- Q1. Print the column information in table Played
SELECT 
-- Q2. 
~~~~
2. Results.txt, which contains the results for the statements. Here is one sample file.
~~~~
-- Q1. Print the column information in table Played
+-----------+---------------------------+
| artist_id | artist_name               |
+-----------+---------------------------+
|         1 | New Order                 |
|         2 | Nick Cave & The Bad Seeds |
|         3 | Miles Davis               |
|         4 | The Rolling Stones        |
|         5 | The Stone Roses           |
|         6 | Kylie Minogue             |
+-----------+---------------------------+
-- Q2.
~~~~
# Step 2: Zip the two files, name the archive according to the requirement in the syllabus.
+ For example, you can name it as CSCI360_Homework3_JohnDoe(0123456).zip(Your file may have a different suffix based on the zip software you use), where 0123456 is your BeeCard number.
# Step 3: Submit the zipped file on [Blackboard](https://blackboard.sau.edu/)
