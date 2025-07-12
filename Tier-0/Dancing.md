Starting Point - Tier 0

-Machine Name: Dancing

-Difficulty: Very Easy

-IP address: 10.129.246.161



##      Steps:

- scan to show the service
    
      sudo nmap 10.129.246.161 -sV -Pn

- enter root

      sudo su
- list shared resources

      smbclient -L 10.129.246.161
- connect to the shared smb folder

        smbclient \\\\\10.129.246.161\\WorkShares

- list the files inside the smb shared folder

      ls
- open each files

      cd Amy.J
      cd Jmaes.P

- download the file

      get flag.txt
- back to root

      ctrl + c
- go to the directory where the file is located

      cd Downloads
- open the file

      cat flag.txt

##   Tasks:

Task 1

-What does the 3-letter acronym SMB stand for?


    Server Message Block


Task 2

-What port does SMB use to operate at?


    445


Task 3

-What is the service name for port 445 that came up in our Nmap scan?


    microsoft-ds


Task 4

-What is the 'flag' or 'switch' that we can use with the smbclient utility to 'list' the available shares on Dancing?


    -L


Task 5

-How many shares are there on Dancing?


    4


Task 6

-What is the name of the share we are able to access in the end with a blank password?


    WorkShares


Task 7

-What is the command we can use within the SMB shell to download the files we find?


    get


Submit Flag

-Submit root flag


    5f61c10dffbc77a704d76016a22f1664
