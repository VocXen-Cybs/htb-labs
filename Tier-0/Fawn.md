Starting Point - Tier 0

-Machine Name: Fawn

-Difficulty: Very Easy

-IP address: 10.129.1.14



##      Steps:

- check ftp version

      sudo nmap 10.129.1.14 -sV -p 21 -Pn
- enter root

        sudo su
- login to ftp server

        ftp 10.129.1.14
- when asked for the name put

        anonymous
- for the password, just click enter
- list the files inside the ftp server

        ls
- downlaod the file

      get flag.txt
- back to root, use ctrl + c
- change diractory to Downloads

        cd Downloads
- list the files in the downloads diractory

        ls
- open the file

        cat flag.txt


##      Taks:

Task 1

-What does the 3-letter acronym FTP stand for?

    File Transfer Protocol


Task 2

-Which port does the FTP service listen on usually?

    21


Task 3

-FTP sends data in the clear, without any encryption. What acronym is used for a later protocol designed to provide similar functionality to FTP but securely, as an extension of the SSH protocol?


    SFTP


Task 4

-What is the command we can use to send an ICMP echo request to test our connection to the target?


    ping


Task 5

-From your scans, what version is FTP running on the target?


    vsftpd 3.0.3


Task 6

-From your scans, what OS type is running on the target?


    Unix


Task 7

-What is the command we need to run in order to display the 'ftp' client help menu?


    ftp -?


Task 8

-What is username that is used over FTP when you want to log in without having an account?


    anonymous


Task 9

-What is the response code we get for the FTP message 'Login successful'?


    230


Task 10

-There are a couple of commands we can use to list the files and directories available on the FTP server. One is dir. What is the other that is a common way to list files on a Linux system.


    ls


Task 11

-What is the command used to download the file we found on the FTP server?


    get


Submit Flag

-Submit root flag

    035db21c881520061c53e0536e44f815
