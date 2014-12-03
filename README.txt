Kenneth Crowell and Shuyan Guo
Comp 116 
December 4, 2014
Assignment 5 - Forensics

Part 1

Part 2

1. Disk formats: Win95 FAT32 and Linux
2.
3. Kali Linux 1.0.9.
   We looked in the /etc directory for "release" files, a file named /etc/debian_version was found, which contains information about the operating system.
4.
5. Yes, there is a root user, password = /root (found in file /2/var/log/auth.log)
6. Yes, there are additional user accounts.
7.
8.
9. Yes. We found the file /home/root/lockbox.txt is an encryted zip archive file rather than a text file. We guessed a few times and found the right password: gaga. Inside the archive is a file named edge.mp4, which is a video of Lady Gaga's performance.
10.
11. It appears the suspect wanted to see the celebrity at some upcoming shows:
12/31/2014: The Chelsea at the Cosmopolitan of Las Vegas Las Vegas, NV 9:00 p.m. PST
2/8/2015: Wiltern Theatre, Los Angeles, CA, 9:30 p.m. PST
5/30/2015: Hollywood Bowl, Hollywood, CA, 7:30 p.m. PDT
(found in file /2/home/stefani/sched.txt)
12. Lady Gaga (real name: Stefani Joanne Angelina Germanotta)
