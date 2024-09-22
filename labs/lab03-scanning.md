# Lab: Scanning and Reconnaissance

## Part 1: Usage of Nmap is Required for Questions 1 - 4.  Usage of SHODAN is Not Allowed!

For questions 1 to 6, the target's IP address is [redacted --see Canvas]. You are granted permission to attack this remote system.

1. List the services and corresponding port number(s) that the target is running.

2. Is the target running a web server --YES or NO?  If the target is running web server software, how do you know? What web server software and version number is being used?

3. Is the target running a database server of some kind --YES or NO? If the target is running a database server, how do you know? What database server software and version number is being used?

4. What operating system *and* distribution is the target (most likely) running?

5. There is a peculiar service running on this target.  What port number is this peculiar service?  What gives you the impression that this is a peculiar service?  What does this service do, provide?  NOTES: You must make a network connection to this peculiar service and determine what it does. Just looking up the service associated with the port number is not enough.

6. Gain remote access to the target. To put it more bluntly: break into the server, gain access, have permission to modify the filesystem! You have authorization to do so! Explain how you gained access to the target, and also provide a screenshot.

## Part 2: Usage of Nmap Not Allowed!

7. Here is a new target IP address: [redacted --see Canvas]. *_Without using Nmap or directly accessing the target via IP address_*, determine the open ports of this target and what this target is. Examples of UNACCEPTABLE ways (directly accessing target) include: going to `http://[redacted]/`, `https://[redacted]/`, `ssh [redacted]`.

8. NETGEAR R8000, R7000, and R6400 routers have known vulnerabilities. Using SHODAN, determine how many of them are (still) exposed on the Internet. An article from December 2016: https://arstechnica.com/security/2016/12/unpatched-bug-allows-hackers-to-seize-control-of-netgear-routers/

## Submitting This Lab

For students officially enrolled in the course, submit lab on Canvas.
