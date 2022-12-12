# Attack is the best defense

## Tools

* wireshark
* telnet
* tcpdump
* docker
* hydra

## 0-0-sniffing

### what is this

Security is a vast topic, and network security is an important part of it. A lot of very sensitive information goes over networks that are used by many people, and some people might have bad intentions. Traffic going through a network can be intercepted by a malicious machine pretending to be another network device. Once the traffic is redirected to the malicious machine, the hacker can keep a copy of it and analyze it for potential interesting information. It is important to note that the traffic must then be forwarded to the actual device it was supposed to go (so that users and the system keep going as if nothing happened).

Any information that is not encrypted and sniffed by an attacker can be seen by the attacker - that could be your email password or credit card information. While today’s network security is much stronger than it used to be, there are still some legacy systems that are using unencrypted communication means. A popular one is telnet.

In this project, we will not go over ARP spoofing, but we’ll start by sniffing unencrypted traffic and getting information out of it.

Sendgrid offers is an emailing service that provides state of the art secure system to send emails, but also supports a legacy unsecured way: telnet. You can create an account for free, which is what I did, and send an email using telnet

I wrote the script user_authenticating_into_server that performs the authentication steps that I just showed above. Your mission is to execute user_authenticating_into_server locally on your machine and, using tcpdump, sniff the network to find my password. Once you find it, paste the password in your answer file. This script will not work on a Docker container or Mac OS, use your Ubuntu vagrant machine or any other Linux machine.

You can download the script user_authenticating_into_server [here](https://s3.amazonaws.com/intranet-projects-files/holbertonschool-sysadmin_devops/264/user_authenticating_into_server)

### solution

* The code in ASCII = bXlwYXNzd29yZDk4OTgh7

* user name : mylogin

### Packet

```packet
  0000   d8 b6 b7 a1 1f 63 cc b0 da 2a bf b6 08 00 45 10   .....c...*....E.
0010   00 4a 40 f2 40 00 40 06 62 67 c0 a8 01 07 12 c5   .J@.@.@.bg......
0020   c2 d0 b5 12 02 4b 67 8b 60 d1 67 35 59 20 80 18   .....Kg.`.g5Y ..
0030   01 f5 a3 88 00 00 01 01 08 0a 21 35 2c 39 b2 84   ..........!5,9..
0040   5c 4c 62 58 6c 77 59 58 4e 7a 64 32 39 79 5a 44   \LbXlwYXNzd29yZD
0050   6b 34 4f 54 67 68 0d 0a                           k4OTgh..
```

## 1-dictionary_attack

Password-based authentication systems can be easily broken by using a dictionary attack (you’ll have to find your own password dictionary). Let’s try it on an SSH account.

* Install Docker on your machine Ubuntu Vagrant machine
* Pull and run the Docker image sylvainkalache/264-1 with the command docker run -p 2222:22 -d -ti sylvainkalache/264-1
* Find a password dictionary (you might need multiple of them)
* Install and use hydra to try to brute force the account sylvain via SSH on the Docker container
* Because the Docker container is running locally, hydra should access the SSH account via IP 127.0.0.1 and port 2222
* Hint: the password is 11 characters long
