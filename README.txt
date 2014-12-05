Kenneth Crowell and Shuyan Guo
Comp 116 
December 4, 2014
Assignment 5 - Forensics

Part 1

Image B is different from both image A and C. We found this out by using the diff command on the images. With this information we used steghide to determine what was hidden within this file. Without the password we had to brute force the file so we wrote a simple bash script to use a wordlist with steghide. After running this with a simple wordlist we found that the password was "disney". We used this password to extract a file named "runme". This file would not run so we used "chmod +x runme" to make it an executable. We ran it and it said to use my first name as an argument, so I then ran it again with my name and got the output "Kenny, you are doing a heckuvajob up to this point!".  

Bash script used:

#!/bin/bash

while read line
do 
steghide extract -sf b.jpg -p $line
done < $1


Part 2

1. The disk has two partitions of different formats: Win95 FAT32 and Linux.

2. T-mobile is involved in this case. We found this by searching the names of major providers and there was evidence of T-mobile being the provider.

3. Kali Linux 1.0.9.
   In /etc directory we found a file named debian_version, which contains information about the operating system.

4. There are a lot of applications that comes with Kali Linux, such as john, aircrack, nmap, etc. We found them in /bin and /usr/bin. Also, Iceweasel and Wireshark were found in /usr/share/applications. 

5. Yes, there is a root user, password = princess (found with john the ripper)

6. Yes, there are additional user accounts. All passwords were found with john
   Accounts   password 
   judas      00000000
   alejandro  pokerface
   stefani    iloveyou

7. Some incriminating evidence could be all of the pictures, list of upcoming tours and the videos (including an encrypted video) of Lady Gaga on the disk and also the fact that there are pdf files that explain how to use sqlmap to exploit a sql injection vulnerability.

8.  Three pictures named a15.jpg, a16.jpg, a17.jpg were deleted in /home/alejanro. From the .bash.history file in /home/stefani we also knew that a note.txt was deleted.

9.  There are 14 pictures found in /home/alejandro.

10. Yes. We found the file /home/root/lockbox.txt is an encryted zip archive file rather than a text file. Using the password we guessed - gaga, we successfully extracted the zip file and found a video of Lady Gaga's performance.

11. Under /home/stefani, we found sched.txt containing the upcoming tour dates and locations where the suspect may want to see the celebrity: 
    12/31/2014: The Chelsea at the Cosmopolitan of Las Vegas Las Vegas, NV 9:00 p.m. PST
    2/8/2015: Wiltern Theatre, Los Angeles, CA, 9:30 p.m. PST
    5/30/2015: Hollywood Bowl, Hollywood, CA, 7:30 p.m. PDT

12. Lady Gaga (real name: Stefani Joanne Angelina Germanotta)
