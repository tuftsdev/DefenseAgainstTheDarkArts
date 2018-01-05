# Lab: Working with a Hypervisor and a Virtual Machine

## Overview

Throughout this course, you will be doing most of your work on a virtual machine.  A virtual machine is a software computer that, like a physical computer, runs an operating system and applications.  Say that your laptop runs Mac OS X, you can run a version of Windows as a virtual machine (the "guest") on top of Mac OS X (the "host").  The value of using a virtual machine is logically separation between machines.  Theoretically, a virtual machine is isolated from the host.  That is, mistakes made on a guest (e.g., malware) will not escape to host --with a few exceptions including file sharing between host and virtual machine.  To run a virtual machine, you will need a hypervisor, also known as a Virtual Machine Manager (VMM).  Hypervisors also provide a very handy feature: taking snapshots of running virtual machine, and rolling back to a snapshot when necessary (i.e., when mistakes are made).  The purposes of this lab are to get you set up using a hypervisor, a Kali Linux virtual machine, and be familiar with important Linux commands.

## Instructions

1. Download Kali Linux ISO from https://www.kali.org/downloads/.  Most of you should be using the 64 bit version, some may need to use the 32 bit version (for older computers).  This ISO contains a full and custom Debian 8 operating system and many security tools.

2. Download a hypervisor software.  Two options:

* VMware Fusion for Mac OS X or VMware Workstation for Windows or Linux
* VirtualBox: Free and open source

While I use both, I prefer VMware Fusion for Mac OS X or VMware Workstation for Windows or Linux as VMware is commonly used by security practitioners and is well-known for its performance and features.  Please do not use VMware Player as you will not be able to create virtual machines.

3. Create a virtual machine with the Kali Linux ISO.  I recommend reserving 2 GB (or 2048 MB of RAM) for the virtual machine.

4. Make sure that networking (i.e., Internet access) is available on your host.  Turn on the virtual machine.  When you turn on the virtual machine the first time, you will be presented with a boot menu.  Select the first option (e.g., "Live (amd64)")

5. Play around with the environment.

### Answer the questions below.

Because this is largely a hands-on course, it is essential that you learn many of the fundamental Linux commands, an important skill for any good security practitioner.  Please learn and tinker with the commands below and answer the questions below.  Many commands will require flags.

Commands: `ls, rm, mkdir, rmdir, cd, pwd, ln, chmod, umask, ping, cut, sort, which, grep, whereis, finger, w, who, whoami, last, file, strings, top, ps, nice, nohup, kill, signal, more, less, ifconfig, arp, nslookup, cat, uname, history, netstat, ifconfig, traceroute, dig, man, lsof, whois, crontab, nc, uniq, id, groups, df, du, touch, ip`

1. How would you find the path to the python command?

2. What command can you use to find out your IP address and MAC address?

3. What command can you use to show all the processes that are running on the system?

4. What command can you use to get more details about running processes listening on ports?

5. What command with flag could you use to list every file, including hidden files, on the entire system, showing their owner, location, and access time? Please also note the flags that you used with command.

6. Assume you found a file named `warrent.pdf`.  What command could you use to find out what type of file this was?

7. So you discovered that `warrent.pdf` is a binary executable.  What command could you use to extract any readable information from the file without running it?   Also, try this on a compressed file such a ZIP or JAR

8. What command can you use to find the IP address-to-MAC address mappings for systems on the local network?

9. Consider the following IP address: 111[dot]72[dot]252[dot]91. Where is the computer with that IP address located --in what country?

10. For the previous question, what command did you use to determine the location of the computer?

11. In the terminal, run the command `setoolkit` and play around.  Describe what this tool is.

12. When using Kali Linux live, what access privileges or permissions do you have on the virtual machine?

13. In your home directory in the virtual machine, use the touch command: run `touch list.txt`. What happens?

14. In your home directory in the virtual machine, run `touch list.txt` again. What happens?

If you are using Kali Linux live ISO, turn off the virtual machine.  Turn it back on.  What happens?  Look at your home directory?  What do you observe? When you turn back on, you should see the boot menu again.  If you do not, check it the Kali Linux ISO is "connected" to the virtual machine.

## References
1. https://www.howtogeek.com/66734/htg-explains-what-is-a-hypervisor/
2. https://security.stackexchange.com/questions/9011/does-a-virtual-machine-stop-malware-from-doing-harm