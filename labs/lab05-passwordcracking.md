# Lab: The Spring 2024 Password Cracking Contest

## Instructions and Rules

Crack as many of the password hashes (below) that you can.

For students in the CS 116 Introduction to Security courses at Tufts University, submit your pot of passwords using `username:password` format for each password that you crack on Canvas.  One `username:password` per line, _text only_.  Be sure to describe your cracking methodology.  You will have unlimited submissions and an entire month to do this lab.  Only inline (cut-and-paste), text only, submissions will be accepted for this lab (e.g., no PDFs, no URLs allowed).

## The Password Hashes

<pre>
jackbear:$1$BGVAnquQ$CB3xkCCex9KYoBLpIzfKO.:1001:1001:,,,:/home/jackbear:/bin/bash
barneybear:$1$OoI8Gjdp$HVZ30fBr92pUZlmJ24XJU0:1002:1002:,,,:/home/barneybear:/bin/bash
teddybear:$1$aT6RQywT$AAbeQ/FvaaLIV.kENTQcA.:1003:1003:,,,:/home/teddybear:/bin/bash
yogibear:$1$1j/LPdi9$it6s0c5XwILlgyg76FFPi/:1004:1004:,,,:/home/yogibear:/bin/bash
sisterbear:$1$.hnet9VI$gpizSxPrpDhWwCJCKggXF0:1005:1005:,,,:/home/sisterbear:/bin/bash
cozybear:$1$/aZIbtfM$7KJvymmIMjzCvtTSGvNrA1:1006:1006:,,,:/home/cozybear:/bin/bash
brotherbear:$1$TAQgSLW0$3YhU40/nln.VqwvdBUMd81:1007:1007:,,,:/home/brotherbear:/bin/bash
carebear:$1$l61DSWE0$yOKLn/jZn7UWlvdMvQgXR0:1008:1008:,,,:/home/carebear:/bin/bash

bluebear:$6$XcMHMb9zwWQ5AQuE$i1E3VYIf8KuRLUxQA1eWGPmgWOTlsReLZtwHbmpz/Hbp3zIxyR8nARhZXwfkXHhEnrrmKoaJA4kmACk0RNrRI/:1009:1009:,,,:/home/bluebear:/bin/bash
papabear:$6$HJRtNnBl1iucewsi$.yxuW2al1ijw15C92CxEIhBKL55yyw.TH3i/zWCFXbIqWlSXdjWe7MjMUAEcUwoLEidmCGhiet.cGyK/KOdst0:1010:1010:,,,:/home/papabear:/bin/bash
blackbear:$6$ObRBq.7idqguqcq8$kVHv6VTxsIH/FHlCLemyyr/YDpYPg262x9p.xgKEdZXDehxzmZv3DnYKdlFnFg2T66YflMLasmhXmxkaZpXBz.:1011:1011:,,,:/home/blackbear:/bin/bash
grizzlybear:$6$p3gbSlLd7JjIoAja$8RsK2eKmnKpE1CuUr1M1fSVo31EsG6ea9I3pjMehsqZp4kk9XwUrshYIh5SE8rOfE3uzqZasxWg4z3.QcJ7rQ/:1012:1012:,,,:/home/grizzlybear:/bin/bash
mamabear:$6$KQZ/ZVnM3FeyfIui$d09eSBXBTA1Who8H6W9WYHF1sh6Y6xjiILQOMwwGt5FssmJQ8v31j2PgXGhG50mmgOXV9L2OfiXaccJnhUUyz0:1013:1013:,,,:/home/mamabear:/bin/bash
pandabear:$6$jgC0GUdU1ZdhLG7D$fzQYiBeZK3xapOF/PXqks62Op3Q2.fEbxQSfIerx6a3sPcj4TW5OQ2VdRa.83ilfELMqhXaghjMf23d/UYh9Q.:1014:1014:,,,:/home/pandabear:/bin/bash
polarbear:$6$FHFLEVv/g0Cf13HB$guZIX/WJSozPB84FNaMo33OPb8KYjxwSriPOkl.62p7wtjPzH8Bd1zB2r0Q6iEyJssIqUb4rHbmFBRT3w/cOL.:1015:1015:,,,:/home/polarbear:/bin/bash
fancybear:$6$MMDvT/foLBfYO.6v$KcIpHBbg9DTS4X9wCllY.UoF23Mysxq.kEy2vYaYMvW8Dyjq3uK91.bNAZo7KGVi16aQ/lL38N0fIgHCr5DwU/:1016:1016:,,,:/home/fancybear:/bin/bash
</pre>

* Absolutely no collaboration of any kind. This is an individual lab.
* Please be sure to keep records of your cracked passwords, including password pot, screenshots, and logs in case you are questioned.
* When you provide your cracked passwords, provide a very brief explanation on what you did (e.g., password cracker used, wordlist, etc.)
* You are allowed to use as many password crackers and word lists that you want and that you can find.  That is, you are not limited to using John the Ripper; you can use any other password cracker.
* Do not send the entire `crackme.txt` to a password cracker, it will confuse it because of multiple hash algorithms used.  Separate the list of hashes by hash algorithm; crack each list separately.
* You are allowed to use any infrastructure to crack the passwords (e.g., Amazon Web Services, as many graphic cards that you can afford). Please note that you are responsible for all costs.
* While you have unlimited submissions, be sure to also submit previously submitted passwords.
* You are strongly urged to submit early and often. Only last submission will count.
* The number of passwords to crack in order to get full points on this lab won't be announced until the final week of the competition.
* This contest will end on Friday, March 15th at 11:59 PM PST.
* One last thing: if you crack all the password hashes (read: good luck with that), you will receive an automatic "A" in the course.