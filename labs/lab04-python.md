# Lab: Python

## Objectives

1. Practice and use Python
2. Delve into the cyber attribution problem.

## Overview

Being proficient in programming is an essential skill to have as a cyber security practitioner.

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">For me, it&#39;s more than invaluable, it&#39;s essential.</p>&mdash; Jeremiah Grossman (@jeremiahg) <a href="https://twitter.com/jeremiahg/status/875111993463644160">June 14, 2017</a></blockquote>

On October 7, 2016, the Department Of Homeland Security (DHS) and the Office of the Director of National Intelligence (DNI) issued a joint statement on election security compromises (https://www.dhs.gov/news/2016/10/07/joint-statement-department-homeland-security-and-office-director-national). DHS has released a Joint Analysis Report (JAR) attributing those compromises to Russian malicious cyber activity, designated as GRIZZLY STEPPE.

## Instructions

Download the GRIZZLY STEPPE Indicators Comma-Separated Values (CSV) file at https://www.us-cert.gov/security-publications/GRIZZLY-STEPPE-Russian-Malicious-Cyber-Activity.  Write a Python program that opens up the CSV file, parses (extracts) all the IPv4 addresses, replaces all the "[.]" with ".", and finally outputs all IP addresses on the terminal.  This is the requirement to complete this lab.

## Advanced

Extend your Python program to analyze all the IP addresses.  Loosely speaking, you can do whatever you want.  The big question to answer: based on the IP addresses and from your analysis, are you really confident that Russians were behind the election security compromises?

Side note: for your interest, my Python program is ~25 lines of code.

## Learning Python

For this class, we will be using Python 2.7.x. Official tutorial: https://docs.python.org/2.7/tutorial/

An interactive Python tutorial: https://www.learnpython.org/

## Submission

You must submit two files:

1. Your Python program that ends in the extension `.py`

2. A `README` about your program.  Identify what aspects of the work have been correctly implemented and what have not. Identify anyone with whom you have collaborated or discussed the assignment. Say approximately how many hours you have spent completing the lab.