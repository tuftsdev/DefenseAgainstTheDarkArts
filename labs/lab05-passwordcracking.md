# Lab: The Fall 2026 Password Cracking Contest

## Instructions and Rules

Crack as many of the password hashes (below) that you can.

For students in the CS 116 Introduction to Security courses at Tufts University, submit your pot of passwords using `username:password` format for each password that you crack on Canvas.  One `username:password` per line, _text only_.  Be sure to describe your cracking methodology.  You will have unlimited submissions and an entire month to do this lab.  Only inline (cut-and-paste), text only, submissions will be accepted for this lab (e.g., no PDFs, no URLs allowed).

## The Password Hashes

<pre>sisterbear:$1$XRub7jM3$PbPrTbDihmbvW7rPDUZqn/:1001:1001:,,,:/home/sisterbear:/bin/bash
grizzlybear:$1$PvdZwfFc$an2eYa.WX0kZonUuE7gO6.:1002:1002:,,,:/home/grizzlybear:/bin/bash
jackbear:$1$USPPxCIF$ozJIti0iWbmiUOAGxCw3I/:1003:1003:,,,:/home/jackbear:/bin/bash
pandabear:$1$hqlSNWAg$9rHaTHqOIhNQZ3DNBRtfu.:1004:104:,,,:/home/pandabear:/bin/bash
yogibear:$1$hSC0V30g$O.62m.1Dzix3.8PImLmdd1:1005:1005:,,,:/home/yogibear:/bin/bash
mamabear:$1$m8KgJkZH$V7L.swdMXDm6QLgRBx0.Y0:1006:1006:,,,:/home/mamabear:/bin/bash
barneybear:$1$wS8tdtBc$f3TxmTF40KFaqZOinHHeQ0:1007:1007:,,,:/home/barneybear:/bin/bash
papabear:$1$Al9bu5eA$1LbMzSMVlxWgPiXKL4N.V1:1008:1008:,,,:/home/papabear:/bin/bash
bluebear:$6$moqkkF4KgucVEOUu$EQKss2jH0/6AnGS6qdgapKJsWsWg9/J1bToMGdM/IxKWXUbBXo2s28xIhg/cwwXbgGgtDOeG1bXEu3EjO974k.:1009:1009:,,,:/home/bluebear:/bin/bash
cozybear:$6$Z3rxHlRrTxkPaT61$/vo/lw8waWnssQqX5U3xbK9olYmv2nBwIxEsC.DWCBTndGf77WyJ49UM9SYm8wSHKBEQmGN.I5wjEuO.nsA8q1:1010:1010:,,,:/home/cozybear:/bin/bash
polarbear:$6$g6EevLu3ruHfMeZg$NLobiOWRI2/1Cs0XxtK7AKtx/O1jFDPBVwEQWFt5JynU0xhWevT09Bmtev/Xt12/Flk5lkW3xRZZZJGFtdG3d.:1011:1011:,,,:/home/polarbear:/bin/bash
teddybear:$6$ijBCxCGVuNQ.qzP.$Cf1Qm0oHpoVR.uPlHqC9lJlQ/HrrI6XSNjBFBcHTBgTaIO3rVU1uc.dHI8UqcdV8JDECY7jZW3UdOLWHnEZGB/:1012:1012:,,,:/home/teddybear:/bin/bash
carebear:$6$uOJYruhu00W6F53p$IA8hrlbxj1vJb1RVybOLMpSyFtUdTwoFTTe3UMAMf9GNduWF0BBc1vtQ1vFhJDo74USjzazFLoFzvUk6hA6ai0:1013:1013:,,,:/home/carebear:/bin/bash
blackbear:$6$2L8YnH5Z8g7b4V0d$Ratr9orpFyqsLg.xPVMNgsjLh/mif.oqhHTc9u7UuEbDucxPtmqhYwkqs6DFHLQaoG1cVmsHohqhfM6Qrpp9h/:1014:1014:,,,:/home/blackbear:/bin/bash
fancybear:$6$uSg/nkTIaCkf8s5M$FcrrC8oCmKdc4oklHJ6nY2VSEBx.Pf4l1CbeuN2I8IKWDjoFoP0irixk2BCCj3bKDMmY3DFg3yUAUdqIA/3N71:1015:1015:,,,:/home/fancybear:/bin/bash
brotherbear:$6$6u/i0OVIrXcXYalb$GAiUTMfToVuItH8wPRESLR062Zj0fOMHHBBHEmj8N7HAmK9Y.Zb4EzQW3OyX6dNYqsdOXvlu.2ssEsl2FGjqX1:1016:1016:,,,:/home/brotherbear:/bin/bash
</pre>

* Absolutely no collaboration of any kind. This is an individual lab.
* Please be sure to keep records of your cracked passwords, including password pot, screenshots, and logs in case you are questioned.
* When you provide your cracked passwords, provide a very brief explanation on what you did (e.g., password cracker used, wordlist, etc.)
* You are allowed to use as many password crackers and word lists that you want and that you can find.  That is, you are not limited to using John the Ripper; you can use any other password cracker (e.g., Hashcat).
* Do not send the entire `crackme.txt` to a password cracker, it will confuse it because of multiple hash algorithms used.  Separate the list of hashes by hash algorithm; crack each list separately.
* You are allowed to use any infrastructure to crack the passwords (e.g., Amazon Web Services, as many graphic cards that you can afford). Please note that you are responsible for all costs.
* While you have unlimited submissions, be sure to also submit previously submitted passwords.
* You are strongly urged to submit early and often. Only last submission will count.
* The number of passwords to crack in order to get full points on this lab won't be announced until the final week of the competition.
* This contest will end on Friday, October 30th at 11:59 PM PST.
* One last thing: if you crack all the password hashes (read: good luck with that), you will receive an automatic "A" in the course.
