# CSCI 360 Spring 2022
# Dr. Ning Zhang
# Chapters 1,2,3 MySQL Introduction

# Objectives:
+ Learn the basics of MySQL
+ Learn the installation of MySQL(XAMPP)
+ Learn how to use XAMPP and MySQL monitor

# 1. Basics of MySQL
## What is MySQL
+ pronounced “My Ess Cue Ell”
+ **“the world’s most popular open source database,”** as the developers at the [MySQL AB corporation](http://www.mysql.com) claim
+ modest-sized database
+ MySQL is a relatively recent entrant into the well-established area of **relational database management systems (RDBMs)**
+ Structured Query Language (SQL)
  - insert, retrieve, and manipulate data.
+ We can interact with the database using the PHP and Perl programming languages, and allows interaction with your data over the medium most people prefer these days: the Web.
  
## Why Is MySQL so Popular?
+ The MySQL development process focuses on offering a very efficient implementation of the features most people need. 
  - This means that MySQL still has fewer features than its chief open source competitor, PostgreSQL, or the commercial database engines.
  - The skills you get from this book will serve you well on any platform.
  - MySQL HAS been the choice for so many beginners and small sites, and now for some heavyweight database users in government and industry.
+ Factors
  - Size and speed
  - Ease of installation
  - Attention to standards
  - Responsiveness to community
  - Easy interface to other software


## Elements of MySQL and Its Environment
+ A MySQL installation has two components: 
  - a server that manages the data
  - clients that ask the server to do things with the data
    + MySQL monitor program that allows you to connect to a MySQL server and run SQL queries.
    + mysqladmin program that allows you to perform various server administration tasks.
    + any program that knows how to talk to the MySQL server is a client (a program for a web-based shopping site or an application to generate sales graphs for a marketing team can both be clients).
      - web server vs. database server
        ![web server vs. database server](https://docs.oracle.com/cd/E24150_01/pt851h2/eng/psbooks/tsvt/img/gv_DistinctTiersOfArchitectureStartingWithDatabaseMovingToApplicati_tsvt7fff.png)
  
+ Four aspects of using MySQL
  - MySQL server
  - SQL
    + core of MySQL use
  - Programming languages
    + a general-purpose programming language such as PHP or Perl to automatically create and execute SQL queries on the MySQL server.
  - Web database applications
    + you can use PHP or Perl to create dynamic, database-driven web applications that can publish information from the database to the Web, and capture information provided by users.

## The LAMP Platform
+ Linux operating system
+ Apache web server
+ MySQL database management system
+ Perl or PHP scripting language.

## Structured Query Language
+ language developed by IBM
+ still used today to interact with relational databases


# 2. Installation of MySQL
+ On textbook "Learning MySQL", Chapter 2 introduces the installation of the LAMP platform in details.
+ In our class, we use the XAMPP application.
  - [XAMPP 8 Tutorial ](XAMPP8%20Tutorial.md)

# 3. Using the MySQL Monitor
+  client-server architecture
  - clients connect to the server to perform database operations
  
  ![client-server architecture](https://www.oreilly.com/library/view/access-database-design/1565926269/tagoreillycom20070221oreillyimages86579.png)
  
+ The standard MySQL command-line client or “monitor” program provided by MySQL AB is the client you’ll probably use the most often.
  - The monitor allows you to control almost all aspects of database creation and maintenance using SQL and the custom MySQL extensions to SQL.

## Starting the Monitor
+ The monitor program is called simply mysql and is found in a directory with the other MySQL programs. 
  - The exact location depends on your operating system and how you chose to install MySQL
 
  - Windows(you can locate the program from XAMPP directly)
  
  ![xamppwin](../Resources/xamppwin.png)
  
  - Mac(There is no such a button on Mac version)
  
  ![xamppmac](../Resources/xamppmac2.png)
  
    + You need to start from `Terminal` application(use `Spotlight` to search for `Terminal` or find the application in `Applications` folder) and run the following command
  
    ~~~~
    /Applications/xampp/bin/mysql --user=root
    ~~~~
    
    ![xamppmac3](../Resources/xamppmac3.png)
    + If you want to use command `mysql` directly, you can 
      - 1. use any text editor to open file `~/.bash_profile`
      - 2. add `export PATH="$PATH:/Applications/xampp/bin"` to the end of the file
      - 3. save and quit the file
      - 4. run `source ~/.bash_profile` in terminal or open a new terminal
      - 5. then, you can use command `mysql --user=root` directly
    + Note: I am using MAC, the mysql program may look different on Windows, but most of the commands we use in this class will be the same.
    + Note: The default password is NULL, if you have set up a password, you need to use the following command
    ~~~~
    mysql --user=root --password=the_mysql_root_password
    ~~~~
## Stoping the Monitor

~~~~
exit;
~~~~

or 

~~~~
quit;
~~~~

![](../Resources/1.stopmonitor2.png)

## Commands
+ version of MySQL
~~~~
SELECT VERSION();
~~~~

+ Note: Do NOT miss the ;

![](../Resources/1.selectversion.png)


+ list all the databases 

~~~~
SHOW DATABASES;
~~~~
  
![](../Resources/1.showdatabases.png)

## Style, Case, and Semicolons
+ A command-line command is a combination of 
  - SQL keywords
  - MySQL proprietary commands
  - names of databases and database components
+ A command-line command is Not case-sensitive
  - e.g.: **show databases** is equivalent to **SHOW DATABASE**
+ A command-line command follows conventions for better readibility.
  - SQL keywords and MySQL proprietary commands are **UPPPERCASE**.
  - names of databases and database components are **lowercase**.
+ A command-line command ends with the semicolon character (;).

~~~~
SELECT User, Host
FROM user;
~~~~

## The Monitor HELP 
+ **HELP** lists commands the monitor understands.

![](../Resources/1.help.png)

+ **HELP Contents** gets help on how to interact with the MySQL server. 

![](../Resources/1.helpcontents.png)

+ **HELP Data Manipulation**  gets information on data manipulation

![](../Resources/1.helpdatamanipulation.png)

+ **HELP SHOW DATABASES** gets information on SHOW DATABASES command

![](../Resources/1.helpshowdatabases.png)

## Running the Monitor in Batch Mode
+ run the following commands in interactive mode
~~~~
use mysql;
SELECT COUNT(*) FROM user;
~~~~

![](../Resources/1.batch1.png)

+ run the commands in batch mode
  - save the commands in a file with extension sql, e.g., count_users.sql
  - run the file using the followng command
  ~~~~
  SOURCE count_users.sql
  ~~~~
    + Note: 
      - If you are using XAMPP, you need to specify the full path of the sql file if it is not in the current directory. To get the current directory, you can use command `pwd` in your terminal(MAC) or command `cd` in your shell(windows).
      
      ![windowscd](../Resources/1.windowscd.png)
      
      ![macpwd](../Resources/1.macpwd.png)
      
      - In our class, we use XAMPP, folder `htdocs` is recommended to save all the files.
        + If you are using Mac, the path is `/Applications/xampp/htdocs`
    
    
        + If you are using Windows, the path is `C:\xampp\htdocs` (You can also find the folder by click **Explore**)
    
      ![explore](../Resources/1.explore.png)
    
  - run the file using its full path
    + If you are using Windows, the full path is `C:\xampp\htdocs\count_users.sql`
  
  ![batch2_2](../Resources/1.batch2_2.png)
  
  - change the full path if you put the sql file in a different path
   
  ![batch2_3](../Resources/1.batch2_3.png)
  
## Loading the Sample Databases
  - Download music.sql from http://tahaghoghi.com/LearningMySQL/downloads.php
  - Put the sql file in the correct folder
  - Run the file
    + MacOS(xampp 7.4.28)
    ~~~~
    source /opt/lampp/htdocs/music.sql 
    ~~~~
    + MacOS(xampp 8.1.4): `source full_path_of_music.sql_file`
    ~~~~
    -- suppose the full path is ~/Downloads/music.sql, you can run
    source ~/Downloads/music.sql
    ~~~~
    
    + Windows
    ~~~~
    source C:\xampp\htdocs\music.sql 
    ~~~~
  
## MySQL Monitor Program Options
+ The monitor program can take several parameters
  - host
    + The host the server is running on; you can leave this out if the server is running on the same host as the client (localhost).
  - user
    + The username to use when connecting to the MySQL server
  - password
    + The password of this user
      - no password
      ~~~~
      mysql --user=the_username
      ~~~~
      - prompt you for a password
      ~~~~
      mysql --user=the_username --password
      ~~~~
      - provide password with username
      ~~~~
      mysql --user=the_username --password=correct_password
      ~~~~
  - database
    ~~~~
    mysql --user=root --database=mysql
    ~~~~
    or
    ~~~~
    mysql --user=root mysql
    ~~~~
  - safe-updates
    + the following command will be prevented.
    ~~~~
    DELETE FROM user;
    ~~~~
## Graphical Clients
+ [MySQL Administrator](http://dev.mysql.com/downloads)
+ [MySQL Query Browser](http://dev.mysql.com/downloads)
+ XAMPP(we use XAMPP in our class, see [XAMPP Tutorial](XAMPP%20Tutorial.md) to learn how to open the graphical clients on the web browser.)
