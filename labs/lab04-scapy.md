# Lab: The Incident Alarm

## Objectives
* Practice and use Python.
* Learn how to parse and dissect network packets programmatically (using Python and Scapy).
* Write a tool to analyze a live stream or a set of network packets for incidents.

## Preliminaries: Learning Python
Being proficient in programming is an essential skill to have as a cyber security practitioner.

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">For me, it&#39;s more than invaluable, it&#39;s essential.</p>&mdash; Jeremiah Grossman (@jeremiahg) <a href="https://twitter.com/jeremiahg/status/875111993463644160">June 14, 2017</a></blockquote>

Because Python 2 was deprecated on January 1, 2020, you must use Python 3 for this lab.

An interactive Python tutorial: https://www.learnpython.org/

## Overview
"Scapy is a Python module created by Philippe Biondi that allows extensive packet manipulation. Scapy allows packet forgery, sniffing, PCAP reading/writing, and real-time interaction with network targets. Scapy can be used interactively from a Python prompt or built into scripts and programs" (from the SANS Institute's Scapy Cheat Sheet https://www.sans.org/blog/sans-pen-test-cheat-sheet-scapy/).

We have covered a number of network scanning techniques, and you practiced finding sensitive information in PCAP files in the previous lab. This time, you will apply your knowledge to write a tool that provides notification of incidents via a live stream of network packets or via a set of packets in a PCAP file.

## Instructions
Using Python and Scapy, write a program named `alarm.py` that provides user the option to analyze a live stream of network packets or a set of PCAPs for incidents. A starter `alarm.py` is provided for you (more below).  Your tool shall be able to analyze for the following incidents:

* NULL scan
* FIN scan
* Xmas scan
* Usernames and passwords sent in-the-clear via HTTP Basic Authentication, FTP, and IMAP
* Nikto scan
* Someone scanning for Server Message Block (SMB) protocol
* Someone scanning for Remote Desktop Protocol (RDP)
* Someone scanning for Virtual Network Computing (VNC) instance(s)

If an incident is detected, alert must be displayed in the format:

`ALERT #{incident_number}: #{incident} is detected from #{source IP address} (#{protocol or port number}) (#{payload})!`

Example outputs: `ALERT #1: Xmas scan is detected from 192.168.1.3 (TCP)! ALERT #2: Usernames and passwords sent in-the-clear (HTTP) (username:batman, password:brucewayne)`

Your program does not need to support saving the stream of packets to a PCAP file or saving a record of detected incidents.

No credit if you program crashes or if exceptions are not handled properly.

### Getting Started
Here is a working `alarm.py`: https://gist.github.com/mchow01/f0f498f29d2b3bd095b8c93172c6ecf7

Your job is to modify the `packetcallback` function. What has been written for you: the handling and parsing of command line arguments, reading of PCAP file, and sniffing of network.

If you go web browsing in the virtual machine with the alarm running, you will notice the alarm will go off...

### IMPORTANT: What You Are NOT Allowed To Do

1. You are not allowed to modify or touch the code below the comment `# DO NOT MODIFY THE CODE BELOW`
2. You are not allowed to use additional _third party_ Python packages aside from Scapy.

### Running and Using the Tool
Run: `sudo python3 alarm.py`. By default with no arguments, the tool shall sniff on network interface `eth0`.  NOTE: this will not work on macOS because macOS uses `en` for network interfaces.  The tool must handle three command line arguments:

`-i INTERFACE: Sniff on a specified network interface`
`-r PCAPFILE: Read in a PCAP file`
`-h: Display message on how to use tool`

Example 1: `sudo python3 alarm.py -h` shall display something of the like:

`usage: alarm.py [-h] [-i INTERFACE] [-r PCAPFILE]

A network sniffer that identifies basic vulnerabilities

optional arguments: -h, --help show this help message and exit -i INTERFACE Network interface to sniff on -r PCAPFILE A PCAP file to read`

NOTE: sniffing on network interfaces requires `sudo`.

Example 2: `python3 alarm.py -r set2.pcap` will read the packets from `set2.pcap`.  NOTE: reading PCAP files via Scapy or a Python program does not require `sudo`.

Example 3: `sudo python3 alarm.py -i en0` will sniff packets on a wireless interface `en0`

When sniffing on a live interface, the tool must keep running. To quit it, press Control-C

### Testing Your Tool
Your tool must be able to detect the usernames and passwords sent in-the-clear in `set1.pcap`, `set2.pcap`, and `set3.pcap` from the Packet Sleuth lab (Lab 2).

Here are PCAPs you can also use to test your alarm:

1. fin.pcap: https://www.cs.tufts.edu/comp/116/fin.pcap
2. xmas.pcap: https://www.cs.tufts.edu/comp/116/xmas.pcap
3. null.pcap: https://www.cs.tufts.edu/comp/116/null.pcap
4. nikto.pcap: https://www.cs.tufts.edu/comp/116/nikto.pcap
5. rdp.pcap: https://www.cs.tufts.edu/comp/116/rdp.pcap
6. smb.pcap: https://www.cs.tufts.edu/comp/116/smb.pcap

### References
* Scapy documentation: https://scapy.readthedocs.io/en/latest/
* Scapy Cheat Sheet (SANS Institute): https://www.sans.org/blog/sans-pen-test-cheat-sheet-scapy/

### The `README` File
This `README` file shall describe the work. This description must:

* Identify what aspects of the work have been correctly implemented and what have not.
* Identify anyone with whom you have collaborated or discussed the assignment.
* Say approximately how many hours you have spent completing the assignment.
* Be written in either text format. No other formats will be accepted.
* List any additional dependencies used.
* For this lab, you must also address the following questions:
  - Are the heuristics used in this assignment to determine incidents "even that good"?
  - If you have spare time in the future, what would you add to the program or do differently with regards to detecting incidents?

## NEW Starting Spring 2023: Using AI Tools Such as ChatGPT

You are allowed to use AI tools such as ChatGPT for assistance.  Learning to use AI is an emerging skill.  However, beware of the limits of tools such as ChatGPT:

1. If you provide minimum effort prompts, you will get low quality results.  You will need to refine your prompts in order to get good results.  This will take work.

2. Don't trust anything it says.  If it gives you a number or fact, assume it is wrong unless you either know the answer or can check in with another source.  You will be resposible for any errors or omissions provided by the tool.  It works best for topics you understand.

3. AI is a tool, but one that you need to acknowledge using.  Please include a paragraph in your `README` file explaining what you used the AI for and what prompts you used to get the results.  Failure to do so is in violation of academic honesty policies.

4. Be thoughtful about when this tool is useful.  Don't use if it isn't appropriate for the case or circumstance.

The rules on using ChatGPT were taken from https://twitter.com/curtlanglotz/status/1615945561294901250

## Submission
Submit two files: the `README.txt`, `alarm.py`

For students officially enrolled in the course, submit lab on Canvas.

## Assessment
This lab is worth 20 points.

* (2 points) `README.txt`
* (18 points)
  - Alarm detects usernames and passwords sent in-the-clear via HTTP Basic Authentication, FTP, and IMAP (4 points)
  - Alarm detects FIN scan (2 points)
  - Alarm detects XMAS scan (2 points)
  - Alarm detects NULL scan (2 points)
  - Alarm detects Nikto scan (2 points)
  - Alarm detects someone scanning for Server Message Block (SMB), Remote Desktop Protocol (RDP), Virtual Network Computing (VNC) (6 points)
* (-5 points) You made modifications below the comment `# DO NOT MODIFY THE CODE BELOW` in `alarm.py`