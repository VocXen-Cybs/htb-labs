Starting Point - Tier 1

-Machine Name: Crocodile

-Difficulty: Very Easy

-IP address: 10.129.1.15


##  Steps:
- log in to ftp server

      ftp anonymous@<ip add>
- list all the contents of the server

      ls
- download the files

      get allowed.userlist.passwd
      get alowed.userlist

- use Gobuster to discover hidden directories and PHP files on the target web server by brute-forcing paths

      gobuster dir -u http://<ip address> -w /usr/share/dirb/wordlists/common.txt -x .php

- go to the login page of the target web app

      http://<ip address>/login.php
- log in using:

      username: admin
      password: (open the file allowed.userlist.passwd, to get the admin password)

##    Tasks:

Task 1

-What Nmap scanning switch employs the use of default scripts during a scan?


    -sC


Task 2

-What service version is found to be running on port 21?


    vsftpd 3.0.3


Task 3

-What FTP code is returned to us for the "Anonymous FTP login allowed" message?


    230

Task 4

-After connecting to the FTP server using the ftp client, what username do we provide when prompted to log in anonymously?


    anonymous


Task 5

-After connecting to the FTP server anonymously, what command can we use to download the files we find on the FTP server?


    get


Task 6

-What is one of the higher-privilege sounding usernames in 'allowed.userlist' that we download from the FTP server?


    admin


Task 7

-What version of Apache HTTP Server is running on the target host?


    Apache httpd 2.4.41

Task 8

-What switch can we use with Gobuster to specify we are looking for specific filetypes?


    -x


Task 9

-Which PHP file can we identify with directory brute force that will provide the opportunity to authenticate to the web service?


    login.php


Submit Flag

-Submit root flag


    c7110277ac44d78b6a9fff2232434d16
