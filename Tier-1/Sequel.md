Starting Point - Tier 1

-Machine Name: Sequel

-Difficulty: Very Easy

-IP address: 10.129.95.232


##  Steps:

- connect to a remote MySQL/MariaDB server

      mysql -u root -h <ip add>

- lists all databases that exist on the server

      show databases;
- Switch to the database named htb

      use htb;

- lists all the tables inside the currently selected database (htb)

      show tables;

- list all the content on the table

      SELECT * from users;
      SELECT * from config;
  

##    Tasks:

Task 1

-During our scan, which port do we find serving MySQL?

    3306


Task 2

-What community-developed MySQL version is the target running?


    MariaDB


Task 3

-When using the MySQL command line client, what switch do we need to use in order to specify a login username?


    -u


Task 4

-Which username allows us to log into this MariaDB instance without providing a password?


    root


Task 5

-In SQL, what symbol can we use to specify within the query that we want to display everything inside a table?

    *


Task 6

-In SQL, what symbol do we need to end each query with?


    ;


Task 7

-There are three databases in this MySQL instance that are common across all MySQL instances. What is the name of the fourth that's unique to this host?


    htb


Submit Flag

-Submit root flag

    7b4bec00d1a39e3dd4e021ec3d915da8
