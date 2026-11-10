# Lab: Technical Risk Analysis

## Objectives
1. Perform a technical risk analysis of a vulnerable system.

## Instructions

You will need to download the entire CTF game source code. Link: https://www.cs.tufts.edu/comp/116/ctf-fall2026.zip (`SHA256(ctf-fall2026.zip)=ea43618cd604998ed6d7aa6240646b4a8e02b66205d89a06240be6c1c2f2e80d`). This file contains the website including web files.

**10 points.** While the goal of our CTF game was to find and exploit vulnerabilities in a system (i.e., flags), you also performed a number of activities, not limited to:

* Penetration testing
* "Ethical hacking"
* Conducting research
* Gathering artifacts
* Interviewing people

Imagine that you are a managing consultant for a major security company or the Chief Security Officer (CSO) for the company that owned the system, and assume that the business context of the system is critical, perform a technical risk analysis of the Capture The Flags (CTF) system. That is, you are to apply a general risk management framework (largely taken from Cigital's Risk Management Framework). This framework can be used by managers and software engineers to identify, track, rank, monitor, and understand risks for a project or system. The output of this activity shall be a table with eight columns:

| Column Name | Information | Example (an actual example you can use) |
|-------------|-------------|-----------------------------------------|
| *Risk ID* | A sequential identifier for risk | 1 |
| *Technical Risk* | Brief description | User authentication to the WordPress blog can be brute-forced. |
| *Techical Risk Indicators* | Evidence of the risk occurring. | Number of incorrect logins for accounts seen in logs; performance of login server has been degrading. |
| *Related CWE or CVE IDs* | Use comma to separate multiple IDs | CWE-521: https://cwe.mitre.org/data/definitions/521.html  |
| *Impact Rating* | Use NIST standard: (H)igh, (M)edium, (L)ow | H |
| *Impact* | Possible results of the risk, impacting the goals of the product. | Increased load on login server; slower performance; possible denial of service |
| *Mitigation* | Action taken to reduce the probability of the risk actually occurring or how to actually fix the bug. There may be more than one way to mitigate a risk. | Lock out user account on 5 incorrect password tries by setting account lockout flag to true. |
| *Validation Steps* | How do you ensure that risk was mitigated? | Account lockout flag set for user account on 5 incorrect password tries. |

In practice and in industry, the technical risk analysis table is used to correlate with business risks. Your job is to produce a technical risk table for the entire CTF game. Each of the vulnerabilities that you found in the CTF game should be a technical risk.

Table shall be submitted in one PDF file.

Important: be sure to review the CTF game source code as there are other vulnerabilities that were not visible via playing game.