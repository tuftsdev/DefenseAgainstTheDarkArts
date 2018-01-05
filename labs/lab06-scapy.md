# Lab: The Incident Alarm

## Objectives

1. Learn how to parse and dissect network packets programmatically (using Python and scapy).
2. Write a tool to analyze a live stream or a set of network packets for incidents.

## Overview

"Scapy is a Python module created by Philippe Biondi that allows extensive packet manipulation. Scapy allows packet forgery, sniffing, PCAP reading/writing, and real-time interaction with network targets. Scapy can be used interactively from a Python prompt or built into scripts and programs" (from The SANS Institute's Scapy Cheat Sheet).

Scapy and Python 2.7 are installed on Kali Linux.

We have covered a number of network scanning techniques, and you practiced finding sensitive information in PCAP files in the previous lab. This time, you will apply your knowledge to write a tool that provides notification of incidents via a live stream of network packets or via a set of packets in a PCAP file.

## Instructions

Using Python and scapy, write a program named alarm.py that provides user the option to analyze a live stream of network packets or a set of PCAPs for incidents. Your tool shall be able to analyze for the following incidents:

* NULL scan
* FIN scan
* Xmas scan
* Usernames and passwords sent in-the-clear via HTTP Basic Authentication or FTP

If an incident is detected, alert must be displayed in the format:

`ALERT #{incident_number}: #{incident} is detected from #{source IP address} (#{protocol or port number}) (#{payload})!`

Example outputs:
`ALERT #1: Xmas scan is detected from 192.168.1.3 (TCP)!`
`ALERT #2: Usernames and passwords sent in-the-clear (HTTP) (username:batman, password:brucewayne)`

Your program does not need to support saving the stream of packets to a PCAP file or saving a record of detected incidents.

No credit if you program crashes or if exceptions are not handled properly.

## Running and Using the Tool

In Kali Linux and assuming you are root, run: python `alarm.py`. By default with no arguments, the tool shall sniff on network interface `eth0`. The tool must handle three command line arguments:

    `-i INTERFACE: Sniff on a specified network interface`
    `-r PCAPFILE: Read in a PCAP file`
    `-h: Display message on how to use tool`

Example 1: `python alarm.py -h` shall display something of the like:

`usage: alarm.py [-h] [-i INTERFACE] [-r PCAPFILE]`

`A network sniffer that identifies basic vulnerabilities`

`optional arguments:`
  `-h, --help    show this help message and exit`
  `-i INTERFACE  Network interface to sniff on`
  `-r PCAPFILE   A PCAP file to read`

Example 2: `python alarm.py -r set2.pcap` will read the packets from `set2.pcap`

Example 3: `python alarm.py -i en0` will sniff packets on a wireless interface `en0`

When sniffing on a live interface, the tool must keep running. To quit it, press Control-C

## Testing Your Tool

Your tool must be able to detect the usernames and passwords sent in-the-clear in `set2.pcap` and `set3.pcap` from the Packet Sleuth lab.

Additional PCAP sets to test your alarm:

1. http-basic-auth-multiple-failures.pcap: from https://github.com/LiamRandall/BsidesDC-Training/blob/master/http-auth/http-basic-auth-multiple-failures.pcap

## References

* Official Python tutorial (Python 2.7): https://docs.python.org/2.7/tutorial/
* Scapy documentation (secdev.org): http://www.secdev.org/projects/scapy/doc/usage.html
* Scapy documentation (via Read the Docs): http://scapy.readthedocs.io/en/latest/
* Scapy Cheat Sheet (SANS Institute): https://blogs.sans.org/pen-testing/files/2016/04/ScapyCheatSheet_v0.2.pdf
* Black Hat Python: Infinite Possibilities with the Scapy Module (GitHub): https://bt3gl.github.io/black-hat-python-infinite-possibilities-with-the-scapy-module.html

## The `README` File

This `README` file shall describe the work. This description must:

* Briefly explain what this tool is (that is, an overview).
* Briefly explain how the tool works.
* Identify what aspects of the work have been correctly implemented and what have not.
* Identify anyone with whom you have collaborated or discussed the assignment.
* Say approximately how many hours you have spent completing the assignment.
* Be written in either text format (`README.txt`) or in Markdown (`README.md`). No other formats will be accepted.
* For this lab, you must also address the following questions:
  * Are the heuristics used in this assignment to determine incidents "even that good"?
  * If you have spare time in the future, what would you add to the program or do differently with regards to detecting incidents?

## Submission

Submit two files: the `README` (either `README.txt` or `README.md`) and `alarm.py`

## Assessment

This assignment is worth 25 points.

* (3 points) README
* (2 points) Help interface
* (4 points) Tool allows network sniffing --and by default on `eth0`
* (4 points) Tool allows for reading in a PCAP file
* (2 points) Tool displays alert(s)
* (10 points) Detection of cleartext passwords, FIN scan, XMAS scan, NULL scan