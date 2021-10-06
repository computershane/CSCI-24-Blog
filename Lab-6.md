# TryHackMe Lab 6VulnNet: Internal

<img src="vulnNet-lab-6.png"
     alt="vulnNet-lab-6_icon"
     style="float: left; margin-right: 10px;" />
     
Task 1  VulnNet: Internal

VulnNet Entertainment is a company that learns from its mistakes. They quickly realized that they can't make a properly secured web application so they gave up on that idea. Instead, they decided to set up internal services for business purposes. As usual, you're tasked to perform a penetration test of their network and report your findings.

Difficulty: Easy/Medium
Operating System: Linux
This machine was designed to be quite the opposite of the previous machines in this series and it focuses on internal services. It's supposed to show you how you can retrieve interesting information and use it to gain system access. Report your findings by submitting the correct flags.

Note: It might take 3-5 minutes for all the services to boot.

Author: MindOverfløw
Discord: MindOverfløw#0420

What is the services flag? (services.txt)

Statred Machine

Ran command `ls` found nothing.

ran `grep`, no luck

ran nmap

`nmap -T4 -A -v 10.10.41.125`

<img src="vulnNet-lab-6-1.png"
     alt="vulnNet-lab-6-1_icon"
     style="float: left; margin-right: 10px;" />
     
smbclient can be exploited.

`smbclient \\10.10.41.125/shares`

no password needed

<img src="vulnNet-lab-6-2.png"
     alt="vulnNet-lab-6-2_icon"
     style="float: left; margin-right: 10px;" />
     
What is the services flag? (services.txt)
 
 Answer-`THM{0a09d51e488f5fa105d8d866a497440a}`
 
What is the internal flag? ("internal flag") 

NFS on port 2049 found, let's mount the NFS fileshare

`sudo mount -t nfs 10.10.41.125: tmp`

tree command not working

ran command `sudo apt install tree`





 


