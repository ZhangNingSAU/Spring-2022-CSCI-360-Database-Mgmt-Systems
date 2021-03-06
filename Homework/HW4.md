# CSCI360 Spring 2021
# Homework 4 for Chapter 5 Part II
# due: 11:59pm 03/08/2021

# Database: this homework is based on the MUSIC database in the textbook.
+ Note: Make sure that you reload the music database once before executing the following sql statements.
# Queries
1. Print the artist names whose songs have been played. (You may have duplicate names, we will learn how to display unique value later.)<br>
2. Print the names of `New Order`'s songs.
3. Find out the total time of the tracks that have been played.
4. Insert two new artists(choose two artists you like).<br>
5. Insert the following instance to table **played**.
~~~~
artist_id = 2, album_id = 1, track_id = 3, no date and time for played.
~~~~
6. Remove the artist with the largets id. <br>
7. Remove the last two artists(the artists who have the largest id and the second largest id). <br>
8. Update the album names to lowercase letters(Have a guess for the lowercase function or google it).<br>
9. Update the track names whose time lenght is less than 4.00 minutes to uppercase letters. <br>

+ Note: You can use the ER models to help you understand the structure of the database.

![](/Resources/4-musicer.png)

![](/Resources/5-musicer2.png)

# Step 1: Complete Q1-Q9, and save your queries and results in two separate files.
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
+ For example, you can name it as CSCI360_Homework4_JohnDoe(0123456).zip(Your file may have a different suffix based on the zip software you use), where 0123456 is your BeeCard number.
# Step 3: Submit the zipped file on [Blackboard](https://blackboard.sau.edu/)
