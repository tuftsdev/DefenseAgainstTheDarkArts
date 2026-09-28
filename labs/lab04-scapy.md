# Lab: The Incident Alarm

## Objectives
* Practice and use Python.
* Learn how to parse and dissect network packets programmatically (using Python and Scapy).
* Write a tool to analyze a live stream or a set of network packets for incidents.

## Preliminaries: Learning Python
Being proficient in programming is an essential skill to have as a cyber security practitioner.

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">For me, it&#39;s more than invaluable, it&#39;s essential.</p>&mdash; Jeremiah Grossman (@jeremiahg) <a href="https://twitter.com/jeremiahg/status/875111993463644160">June 14, 2017</a></blockquote>

Because Python 2 was deprecated on January 1, 2020, you must use Python 3 for this lab.  Instructions has been modified for Python 3.12.x.

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

### Getting Started Part 1, Alarm Starter Code
Here is a working `alarm.py`: https://gist.github.com/mchow01/f0f498f29d2b3bd095b8c93172c6ecf7

Your job is to modify the `packetcallback` function. What has been written for you: the handling and parsing of command line arguments, reading of PCAP file, and sniffing of network.

### Getting Started Part 2, Installing Latest Python 3 and Scapy

Step 1: install the latest version of Python for your system.  If you are using macOS and Homebrew, you can install the latest version of Python via `brew install python`.  For Windows, download installer at https://www.python.org/downloads/

Step 2: create a folder for the lab.  Example: `mkdir alarm`

Step 3: Inside the `alarm` folder (via `cd alarm`), create a virtual environment via `virtualenv` for Python.  Run `python3 -m venv env`.  `virtualenv` is a tool that allows you to create virtual environments in Python and manage Python packages --so your system default Python packages, libraries, and tools do not break.  To learn more about virtual environments, read https://learnpython.com/blog/how-to-use-virtualenv-python/.

Step 4. Activate the virtual environment via `source env/bin/activate`.  You will notice `(env)` on your command prompt.  This shows that Python virtual environment is active.

Step 5. Install `scapy` via `pip install scapy`

Step 6. Download a copy of the alarm starter code (above, from GitHub) into the `alarm` folder and call it `alarm.py`

Step 7. Download a copy of `set2.pcap` from Lab 2 into the `alarm` folder (e.g., `wget https://www.cs.tufts.edu/comp/116/set2.pcap`)

Step 8. Run `python3 alarm.py -r set2.pcap`.  The alarm will read in `set2.pcap` and you should see a run of `HTTP (web) traffic detected!` alerts.

Step 9. When you want to exit your virtual environment, run `deactivate` before you close terminal.

### IMPORTANT: What You Are NOT Allowed To Do

1. You are not allowed to modify or touch the code below the comment `# DO NOT MODIFY THE CODE BELOW`
2. You are not allowed to use additional _third party_ Python packages aside from Scapy.

### Running and Using the Tool
Run: `python3 alarm.py`. By default with no arguments, the tool shall sniff on network interface `eth0`.  This will result in an error as you need to be superuser / administrator to sniff network traffic.  Also note, this will not work on macOS because macOS uses `en` for network interfaces.  The tool must handle three command line arguments:

`-i INTERFACE: Sniff on a specified network interface`
`-r PCAPFILE: Read in a PCAP file`
`-h: Display message on how to use tool`

Example 1: `python3 alarm.py -h` shall display something of the like:

`usage: alarm.py [-h] [-i INTERFACE] [-r PCAPFILE]

A network sniffer that identifies basic vulnerabilities

optional arguments: -h, --help show this help message and exit -i INTERFACE Network interface to sniff on -r PCAPFILE A PCAP file to read`

NOTE: again, sniffing on network interfaces requires `sudo`.

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
7. vnc.pcap: https://www.cs.tufts.edu/comp/116/vnc.pcap

### References
* Scapy documentation: https://scapy.readthedocs.io/en/latest/
* Scapy Cheat Sheet (SANS Institute): https://www.sans.org/blog/sans-pen-test-cheat-sheet-scapy/

## Using AI Tools Such as ChatGPT, Claude

You are encouraged to use AI tools such as ChatGPT and Claude for assistance.  Learning to use AI is no longer an emerging skill, but a necessary one especially in tech field.  However, beware of the limits of tools such as ChatGPT:

1. If you provide minimum effort prompts, you will get low quality results.  You will need to refine your prompts in order to get good results.  This will take work.

2. Don't trust anything it says.  If it gives you a number or fact, assume it is wrong unless you either know the answer or can check in with another source.  You will be responsible for any errors or omissions provided by the tool.  It works best for topics you understand.

3. AI is a tool, but one that you need to acknowledge using.

4. Be thoughtful about when this tool is useful.  Don't use if it isn't appropriate for the case or circumstance.

The rules on using ChatGPT were taken from https://twitter.com/curtlanglotz/status/1615945561294901250

### The `README.txt` File

The `README.txt` file must be written:
1. In your own words (candor encouraged)
2. Two pages max
3. Must be in text format --not Markdown because Canvas cannot render Markdown.

Look, most if not all of you will use an LLM like ChatGPT or Claude to do the actual coding of this lab, but how did you go about doing this lab from start to finish?  What questions did you ask to clarify certain elements of this lab (e.g., did you ask what a Nikto scan is)?  What model(s) did you use?  What software / editor did you use?  How did you test the generated program from LLM?  What other thoughts do you have about this lab?  _Write in your own words, and candor is strongly encouraged._

If your `README.txt` reads like AI slop, then you will receive a 0 for this lab.

## Submission
Submit two files: the `README.txt`, `alarm.py`

For students officially enrolled in the course, submit lab on Canvas.

## Assessment
This lab is worth 20 points.

* (10 points) `README.txt`
* (BONUS +1) In liew of submitting a `README.txt`, email me a _handwritten_ `README`.  Take pictures of pages, email pictures.
* (10 points)
  - Alarm detects usernames and passwords sent in-the-clear via HTTP Basic Authentication, FTP, and IMAP
  - Alarm detects FIN scan
  - Alarm detects XMAS scan
  - Alarm detects NULL scan
  - Alarm detects Nikto scan
  - Alarm detects someone scanning for Server Message Block (SMB), Remote Desktop Protocol (RDP), Virtual Network Computing (VNC)
* (-10 points) You made modifications below the comment `# DO NOT MODIFY THE CODE BELOW` in `alarm.py`
* (-20 points) You used AI to write `README.txt`
