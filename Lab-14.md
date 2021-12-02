# MiroCon

# Speaker `Shane Roush` aka `ComputerShane`

Hacking fileVault 2 Encryption

# Abstract 
`In this demonstration, I will show how to dump the fileVault 2 encryption hash from an APFS formatted mac drive running Mac Os Catelina. 
I will use the Target disk mode on the victim client as well as use an attacking pc running Ubuntu 20.04.3 LTS.`

# Bio 
`MY background is many years in IT from multiple MSP's, Public sector government, and  Cyber freelance contractor to name a few. 
I have extensive knowledge in cyber forensics, and for fun i like wiping my drives, and then using file carving extraction methods 
for retrieval of my own data for proof of concepts.`

# Detailed Outline
`Step 1`, Create Bootable USB flash drive with Ubuntu

`Step 2`, Boot Ubuntu on attacker PC

`Step 3`, Install tools `(APFS-fuse)` needed to complete the atatck

`Step 4`, Install Dependencies `(fuse3 libfuse3-dev libbz2-dev cmake git libattr1-dev zlib1g-dev)`

`Step 5`, compile each binary and/or dependancy

`Step 6`, Boot victim MacBook with FileVault Drive Encryption 2 in Target Disk Mode, `hold T while booting`

`Step 7`, Detirmine Disk name using command `cat /proc/partitions`

`Step 8`, Acquire Hash by using command ` sudo ./apfs-dump-quick /dev/sdb log.txt`

`Step 9`, Arrange Hash respectively `$fvde$2$16$<Salt_Here>$<Iterations_Here>$<KEK Wrpd_Here>` then save to hash.txt

`Step 10`, Use HashCat to crack password with command `hashcat -a 0 -m 18300 -o cracked.txt /usr/share/wordlists/rockyou.txt`



# Confrences 

`N/A` This is my first.



