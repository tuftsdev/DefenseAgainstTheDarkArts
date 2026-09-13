# Lab: Packet Sleuth

## Objectives

1. Learn how to read and dissect files and sensitive information (including usernames and passwords) from packet sets using open source tools
2. Work with real network traffic from arguably the world's most dangerous computer network
3. Understand the dangers of sending data over an open network unencrypted, "in-the-clear"

## Note on AI Usage

Do not use any AI tools for this lab (e.g., ChatGPT, Claude, Ollama, local models, etc).  This is a straight-forward lab to do using Wireshark.  You are foolish to do this lab using AI.

## Overview

You are given four sets of packet captures from different networks in PCAP format to analyze.  One is from arguably the world's most hostile network, DEF CON in Las Vegas, NV.

## Instructions

Download the following PCAP files:
* Set 1: https://www.cs.tufts.edu/comp/116/set1.pcap (11.5 MB)
* Set 3: https://www.cs.tufts.edu/comp/116/set3.pcap (101 KB)
* Set 4: https://www.cs.tufts.edu/comp/116/set4.pcap (61 MB. NOTE: I am not responsible for the contents in this PCAP.)

Wait, where is `set2.pcap`?  It is inside `set1.pcap`.

Open and analyze the sets of packets using Wireshark (or `tshark`).  Aside from the command line interface and standard *nix commands, you do not need to use other tools.  Please answer all the questions below:

### set1.pcap

1. What application protocol was used to transfer files from PC to server?

2. Briefly describe why the protocol used to transfer the files is insecure?

3. What is the secure alternative to the protocol used to transfer files?

4. What is the IP address of the server? (be careful)

5. What was the username and password used to access the server?

6. How many files were transferred from PC to server?

7. Extract all the files that were transferred from PC to server.  Each file must have same corresponding file name as they were originally transferred from (e.g., `set2.pcap`). These files must be part of your submission!

8. What is the model and version of the phone used to take the picture found in `set1.pcap`?

### set2.pcap

A Pi-hole is a network-level advertisement and Internet tracker blocking application which acts as a DNS sinkhole and optionally a DHCP server, intended for use on a private network. https://pi-hole.net/

9. How many packets are in `set2.pcap`?

10. What is the protocol of the packets? (also, recall one of your answers in Lab 1)

11. The Pi-hole is trying to find which device has a certain IP address on the network.  What is that IP address?

12. What is, or what kind of device has the IP address in question?  Specify the vendor.

### set3.pcap

13. How many plaintext username-password pairs are there in this packet set?

14. For each of the plaintext username-password pair that you found, provide the username and password, and identify the protocol used.

**IMPORTANT NOTE: PLEASE DO NOT LOG ON TO THE WEBSITE OR SERVICE ASSOCIATED WITH THE USERNAME-PASSWORD THAT YOU FOUND!**

15. Of all the plaintext username-password pairs that you found, how many of them are legitimate?

### set4.pcap

16. How many packets are there in this set?

17. How many plaintext username-password pairs are there in this packet set? Please do not count accounts such as "anonymous" or "cisco".

18. For each of the plaintext username-password pair that you found, provide the username and password, identify the protocol used, server IP, the corresponding domain name if possible (e.g., google.com), and port number.

**IMPORTANT NOTE: PLEASE DO NOT LOG ON TO THE WEBSITE OR SERVICE ASSOCIATED WITH THE USERNAME-PASSWORD THAT YOU FOUND!**

19. Of all the plaintext username-password pairs that you found, how many of them are legitimate? That is, the username-password was valid, access successfully granted? Please do not count any anonymous or generic accounts.

### General Question

20. Based on PCAP sets 1, 3, and 4, what advice would you give to the owners of the username-password pairs that you found so their account information would not be revealed "in-the-clear" in the future?

## Submitting This Lab

For students officially enrolled in the course, submit lab on Canvas.
