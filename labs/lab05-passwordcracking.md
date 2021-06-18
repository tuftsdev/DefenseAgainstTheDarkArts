# Lab: The Summer 2021 Password Cracking Contest

## Instructions

Crack as many of the password hashes (below) that you can.

For students in the COMP / CSO 116 Introduction to Security courses at Tufts University, submit your pot of passwords using `username:password` format for each password that you crack on Canvas.  One `username:password` per line.  Be sure to describe your cracking methodology.  You will have unlimited submissions and an entire month to do this lab.  Only inline (cut-and-paste) submissions will be accepted for this lab.

## The Password Hashes

<pre>
belgium:$1$cHcZPALS$R73l40hQ4uULNXaRVuwb9.:1001:1001:,,,:/home/belgium:/bin/bash
russia:$1$07OeT24w$nZC9lhyUvLS5ZSIpSlBdR/:1002:1002:,,,:/home/russia:/bin/bash
italy:$1$KILD50Wu$ZavxnSFW.rJFw2ZqjabQA/:1003:1003:,,,:/home/italy:/bin/bash
wales:$1$76T7YtxD$zveRCuyTFYDcTtdTcgUOt/:1004:1004:,,,:/home/wales:/bin/bash
switzerland:$1$MvA3qNdR$WjqgkWLoZs2hZ1QfERlSJ.:1005:1005:,,,:/home/switzerland:/bin/bash
turkey:$1$Rkofp2AE$sYSQL71wWeJ2ozDlulmJG/:1006:1006:,,,:/home/turkey:/bin/bash
finland:$1$RoNzitJE$4ypcFUfQeuGvWCROQJjM7/:1007:1007:,,,:/home/finland:/bin/bash
denmark:$1$CCxdcrXz$sIpfymDf9wftTZ2YyWyg31:1008:1008:,,,:/home/denmark:/bin/bash
netherlands:$1$hI4mNVPZ$axj5KW3V8pkRE5TChDdEi0:1009:1009:,,,:/home/netherlands:/bin/bash
ukraine:$1$Iw/e.Fu3$v1le47O4m/wf28tj5K0Aj1:1010:1010:,,,:/home/ukraine:/bin/bash
austria:$1$0fyXp9OJ$CyS9ekf2flJMWTi/kUNLU1:1011:1011:,,,:/home/austria:/bin/bash
nmacedonia:$1$QOorRQ7I$N2IDJN9iwGqbiytH2FMMd.:1012:1012:,,,:/home/nmacedonia:/bin/bash
czechrepublic:$6$HRwOf4/FCUYr/zvG$CqNrTfVVjnPp5rExtWfPs2nxL9dYUUVELIastZQ3eMq3F2jcAlEZtFOL9GEHhzZN8r31OSj.F/pPIKlo23Zli0:1001:1002:,,,:/home/czechrepublic:/bin/bash
england:$6$foIJz9z4Us3/DwZ5$3LH4PH3DpgYlCIE6rWqoHUrhN5sXSWeT4WH/LoMWcJeTEo4NIRo47GqjyTyffta/m4v9K495.LKgVAJcjKskM.:1002:1003:,,,:/home/england:/bin/bash
scotland:$6$PvAZLH2mD5NTfGtI$4HYdb2c1/7smTU1OK.Fl5UBJsdwx0S20QAhx6b36jHPxhGQTQE9YEq8qb/1T0x42irdlF7uRIGOgj/5ELuFWv.:1003:1004:,,,:/home/scotland:/bin/bash
croatia:$6$ynLKp4ycKKapo3o1$6gURCexs5cL0uNfqnKQLSAL2JJEHr1MTq16WHHrcWIfL7vYjE86HReaQBZgLL0YvVhxOKGWUzUVTsmsVezwL9/:1004:1005:,,,:/home/croatia:/bin/bash
slovakia:$6$cmbew2k4yfISqGFh$asC/5Cw2v4hs76xih36cy8Y69cssDAHBByEngvpV/t7kC.pIiky0LTI8ICeRe6vPolqwawxV1ZKTgAYhXguWy.:1005:1006:,,,:/home/slovakia:/bin/bash
spain:$6$d4jFwDQcYiEWTpNr$iEfHg62Nao7yI4wDW5FATV2pbbcc0oL/lxtKCLAbdo4JO2/XOWr9RMZuNBDezxOPAHOmh9g//fsfC4f7w/yFl0:1006:1007:,,,:/home/spain:/bin/bash
sweden:$6$TKyej9Zbm.l2Du0n$r7572ERZzDKaZBxStaso5rJJkM435Z416qebPG2vhxQ8Ak4GVfdOcfh2ZGcWgxKPKsezMA6BCwMrNvi2p6d6N/:1007:1008:,,,:/home/sweden:/bin/bash
poland:$6$iIqKKM.2buc740Za$rs/6tgbvrpFYeeUPX0/62UxIBFfBqxVHz5wRR14Kk5gRJkfuB4Gvx44IvW1ogap4GnthSN7RJVKiOseYEZH4j1:1008:1009:,,,:/home/poland:/bin/bash
portugal:$6$nrZn0QN4KgsOfW96$NjpoAk4WOgeqaxaBUuSyzCamne0XSjY.SLLgnYxoQEnlQhr2mKbH0rHOhBTHKIt1NUZGuMpfaFR5oeNzxmd/c0:1009:1010:,,,:/home/portugal:/bin/bash
france:$6$TGByQYcWcFZC9E8e$C7XvNTVYrhyl2D7jpf2t.0h0Tb.qrSLqgikqPpZV0ALeTzabMezdoD5KBKO4MMlAm9woSAv5hfe/f8YoJoifZ1:1010:1011:,,,:/home/france:/bin/bash
germany:$6$J.dsxyFJUq/cIUS2$XvURhmAj6QooNZ7hUd2osNgycDeYnVrOMAUDF8C3FxkpeIAsN0Za0Yv4Hv6ah7sSdWH9Q2bfOGdvhQuSvMjo.0:1011:1012:,,,:/home/germany:/bin/bash
hungary:$6$pk1.ySvrRtpqJSHJ$/BOSLqcSueNIsrhAf/b46gR6qk1V34krQs3vWUag97RmQ0eeI0V2jIKyfUIRO9f3IwIHVLCg5XGU.l4w4cR3S.:1012:1013:,,,:/home/hungary:/bin/bash
</pre>

## Rules

* Absolutely no collaboration of any kind. This is an individual lab.
* Please be sure to keep records of your cracked passwords, including password pot, screenshots, and logs in case you are questioned.
* You are allowed to use as many password crackers and word lists that you want and that you can find.
* You are allowed to use any infrastructure to crack the passwords (e.g., Amazon Web Services, as many graphic cards that you can afford). Please note that you are responsible for all costs.
* While you have unlimited submissions, be sure to also submit previously submitted passwords.
* You are strongly urged to submit early and often. Only last submission will count.
* The number of passwords to crack in order to get full points on this lab won't be announced until the final week of the competition.
* This contest will end on Wednesday, July 28th at 11:59 PM PDT.
* One last thing: if you crack all the password hashes (read: good luck with that), you will receive an automatic "A" in the course.