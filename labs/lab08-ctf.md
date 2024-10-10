# Lab: The Capture The Flag Game 

## Objectives

1. Find vulnerabilities in web application(s) and then take advantage of them.

## Overview

In this traditional game, you will be finding and exploiting vulnerabilities in a series of applications, mainly web, to gain access to information you should not have access to. The goal is to find the "flags" placed on the server or servers. As in the past, I will tell you how many flags I have planted. I will also provide an obscure hint for each of them.

## Instructions

You will have one week to play the game.

The game: http://[redacted]/

The scoreboard: http://[redacted]/scoreboard

## A Flag

In the style of many Security Capture The Flag games, the format of a flag will look like this: `key{flag}`. Examples: `key{somelongstringthatrepresentshteflag}` or `key{334359b051f4dda20937055605b3706dfe91d6c8}")`. Each flag will worth a certain value: 100 points, 200 points, 300, and 400 points. You will be given a unique key to submit flags, to be posted in Canvas under your grading for this lab.

## Scoring

There will be a scoreboard. The scoreboard will display a hint for each flag, and the scores for each player.  This is also where you will submit flags.  The scoreboard is available at [redacted].

## Assessment

There will be two components for grading:

1. Your team's score for the game (15 points)
2. Your team's CTF writeup (15 points)

## Ground Rules

1. Should you tamper with the scoreboard or flag submission system, 100 points will be deducted from your score for each attempt.

## Preparing to Play

* It is important that you tinker with the applications.
* Use your creativity. That is, if you were an attacker, what would do?
* Be sure to view the source of all the web pages and relevant files.
* For some challenges (flags), some programming or scripting may be necessary.
* Resources that would be ideal to have for the game: SQL reference, a proxy (e.g., Burp Suite), Kali Linux. You are encouraged to use tools that are on Kali Linux.

## The CTF Write-Up

You will produce a write-up that submitted electronically in PDF format.

So what constitutes a good CTF write-up? For each flag that you finds, the following information should be provided:

* A screenshot of the flag
* The exact location of the flag (path or file name)
* The exploit or methodology used to find the flag

A good example of a CTF write-up is https://tcode2k16.github.io/blog/posts/picoctf-2018-writeup/web-exploitation/ (Pico CTF 2018 Web Exploitation Writeup). A list of CTF write-ups can be found at https://ctftime.org/writeups and at https://github.com/VulnHub/ctf-writeups.