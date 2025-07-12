Starting Point - Tier 0

-Machine Name: Meow

-Difficulty: Very Easy

-IP address: 10.129.59.221


##  Steps:
- open terminal, scan for open ports using
  
        sudo nmap 10.129.59.221 -sV
- to automaticallt log in to the root

        telnet -l root 10.129.59.221
- to list the files inside the port 23, we can use the 

        ls
- to open the file and get the flag, we'll use

        cat flag.txt


##    Tasks:

Task 1

What does the acronym VM stand for?

    Virtual Machine

Task 2

What tool do we use to interact with the operating system in order to issue commands via the command line, such as the one to start our VPN connection? It's also known as a console or shell.

    terminal

Task 3

-What service do we use to form our VPN connection into HTB labs?

    openvpn

Task 4

-What tool do we use to test our connection to the target with an ICMP echo request?

    ping

Task 5

-What is the name of the most common tool for finding open ports on a target?

    nmap

Task 6

-What service do we identify on port 23/tcp during our scans?

    telnet

Task 7

-What username is able to log into the target over telnet with a blank password?

    root

Submit Flag

-Submit root flag

    b40abdfe23665f766f9c61ecba8a4c19
