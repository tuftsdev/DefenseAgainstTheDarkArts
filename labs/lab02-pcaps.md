# Lab: Packet Sleuth

## Objectives

1. Learn how to read and dissect files and sensitive information (including usernames and passwords) from packet sets using open source tools
2. Work with real network traffic from arguably the world's most dangerous computer network
3. Understand the dangers of sending data over an open network unencrypted, "in-the-clear"

## Overview

You are given three sets of packet captures from three different networks in PCAP format to analyze: one from a network where file transfers occurred, one from a university network, and one from arguably the world's most hostile network, DEF CON in Las Vegas, NV.

## Instructions

Download the following PCAP files:

* Set 0: https://www.cs.tufts.edu/comp/116/set0.pcap (4 KB)
* Set 1: https://www.cs.tufts.edu/comp/116/set1.pcap (6.4 MB)
* Set 2: https://www.cs.tufts.edu/comp/116/set2.pcap (20 KB)
* Set 3: https://www.cs.tufts.edu/comp/116/set3.pcap (61 MB. NOTE: I am not responsible for the contents in this PCAP.)

Open and analyze the sets of data, one at a time, using Wireshark. It is encouraged that you also use additional open source tools (e.g., Ettercap, dsniff) for your analysis. Please answer all the questions below:

### set0.pcap

1. What is the MAC address and the vendor (i.e., company name) of the device with the IP address 192.168.1.217?

### set1.pcap

2. What application protocol was used to transfer files from PC to server?

3. Briefly describe why the protocol used to transfer the files is insecure?

4. What is the secure alternative to the protocol used to transfer files?

5. What is the IP address of the server? (be careful)

6. What was the username and password used to access the server?

7. How many files were transferred from PC to server?

8. Extract all the files that were transferred from PC to server. VERY IMPORTANT: each file MUST have proper file extension. These files must be part of your submission!

### set2.pcap

9. How many plaintext username-password pairs are there in this packet set?

10. For each of the plaintext username-password pair that you found, provide the username and password, and identify the protocol used.

**IMPORTANT NOTE: PLEASE DO NOT LOG ON TO THE WEBSITE OR SERVICE ASSOCIATED WITH THE USERNAME-PASSWORD THAT YOU FOUND!**

11. Of all the plaintext username-password pairs that you found, how many of them are legitimate?

### set3.pcap

12. How many packets are there in this set?

13. How many plaintext username-password pairs are there in this packet set? Please do not count accounts such as "anonymous" or "cisco".

14. For each of the plaintext username-password pair that you found, provide the username and password, identify the protocol used, server IP, the corresponding domain name if possible (e.g., google.com), and port number.

**IMPORTANT NOTE: PLEASE DO NOT LOG ON TO THE WEBSITE OR SERVICE ASSOCIATED WITH THE USERNAME-PASSWORD THAT YOU FOUND!**

15. Of all the plaintext username-password pairs that you found, how many of them are legitimate? That is, the username-password was valid, access successfully granted? Please do not count any anonymous or generic accounts.

16. Provide a listing of all IP addresses with corresponding hosts (hostname + domain name) that are in this PCAP set.

### General Question

17. Based on PCAP sets 1 - 3, what advice would you give to the owners of the username-password pairs that you found so their account information would not be revealed "in-the-clear" in the future?

## Submitting This Lab

For students officially enrolled in the course, submit lab on Canvas.