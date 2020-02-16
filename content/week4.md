
---
title: "Week4"
date: 2020-02-16T14:04:31+11:00
draft: false
dropCap: false
---
# Sprint 3: Writeup of a boot2root machine
This week, we were assigned to choose one vulnerable VM to exploit and get root user on. This was the week to really get my hands dirty, and where I would learn a few practical skills on hacking.

Last week, I'd vowed to be more consistent with my work, and to catchup with Bandit and Natas in any spare time that I had. This week, I was able to fit in a little more consistency with my work, and found that I really had my hands full with pentesting. I had no time for catching up with wargames - which would have been useful, but instead I learnt a lot as I began to get down to actual pentesting with boxes.  

This week involved:
+ Learning the process of Pentesting
+ Producing a write-up after working on a box from Tryhackme.com

### Getting a hold of the process
On Monday, I was informed of my task for this week being: completing and creating a writeup for a box found on tryhackme or vulnhub. My first introductions to said boxes this week came in the form of a demonstration done by my tutor Jason.

The box was named, [Wakanda](https://www.vulnhub.com/entry/wakanda-1,251/) and was found on Vulnhub.
In short, the demonstration covered:
+ How to download and open the box as an .ovf file on Kali
+ Using netdiscover to ping for the IP address
+ Using Nmap to find open ports.
+ Finding exploits and running commands from relevant cheatsheets until successful
+ Using gobuster to go through direcotires
+ Using cyberchef to decode
+ Finding reverse shell which would give him access to devops
+ Running a chron job to gain root privileges

This process laid out in the demonstration, while I didn't know it at the time, would become more and more familiar as I interacted with other boxes. I saw that a pattern began to develop, which can also be seen in this slide from this week's learnings.

![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/4/process.png)
#### Above: Pentesting Procedure as depicted in tutorial slides

Despite seeing that demonstration however, I felt like I had only gained a surface level understanding of the pentesting process, and any insights that I'd not fit into my hastily typed notes flew out of my brain quickly. I needed to try it for myself to properly understand, but I was not confident in starting.

On Tuesday, I attempted to work on a recommended easy box: [Basic Pentesting 1](https://www.vulnhub.com/entry/basic-pentesting-1,216/) on Vulnhub. There were not many instructions, and I genuinely had no idea what I was doing. Though Jason had demonstrated how things such as how to begin with nmap and searching for ports, at this time I couldn't fully understand everything I needed to do, and why I was doing them - so I needed a more indepth tutorial to explain each step as it went.

Luckily, when I came into the classes' drop in session on Wednesday, I found Anthony and Dowson (classmates) working on a box namd tryhackme named [Vulnversity](https://tryhackme.com/room/vulnversity). They recommended this to me as I was similarly as lost as them, and this box guided us sequentially through the process of cracking a box.

## Recon and locating directories
I started off using nmap: I primarily used the command nmap –sV to display the version of the server, alongside various details about open ports. However, continually I found that 0 hosts were up, though the I.P address was correct. After using nmap-Pn to search through every port to find which ones were up, I found that my host was detectable, but ultimately I still could not display open ports for said host using nmap –sV, nor could I connect to the webpage.

![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/4/nmap%20down.png)
#### Above: nmap -Pn and -sV saying different things about hosts

I found that the problem was a basic and fundamental one: I had not been using the tryhackme website’s vpn: OpenVpn. The box required me to connect to the website's vpn to connect. This was a quick fix once I was informed of it, but I would continually have to reconnect to this vpn every few hours, whether it was due to interference with my UTS wifi or some other unknown problems that forced me to redeploy my box.

 Using Nmap, I'd found an exploitable port (port 3333), which I then used in Gobuster to find a hidden directory on the webserver. Gobuster recommended me to use wordlists to identify if there were any available wordlists. However, the provided gobuster command did not work as intended.

 ![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/4/gobuster.png)
 #### Above: Gobuster Command that runs for an hour
 
 The provided gobuster command would take over 1 hour (without interruption) to provide an output, in addition to thousands of error messages. In cooperation with classmates Anthony and Dylan, we were able to configure the gobster command to use more threads (thus speeding up the process and eliminating a few errors) and began filtering for desiredstatus codes (such as 301). Despite this effort, the gobuster command sitll took far too much time. Eventually, Anthony, after asking one of our tutors was able to find a more efficient command.
 re
wfuzz -w /usr/share/wordlists/wfuzz/general/common.txt http://10.3434:3434/FUZZ

 ![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/4/internal.png_)
#### Above: Finding the Internal Directory
This displayed every directory alongside its status code – most of them being 404. After sorting through these manually, I found that the ones that were available (301) were html, css, js and internal. In this case, internal was the hidden directory I was looking for.


On Thursday, I was treated to a demonstration of another box by Jason of [Basic Pentesting](https://tryhackme.com/room/basicpentestingjt). I found that my progress on Vulnversity gave me some basic knowledge that really improved my comprehension of this demonstration, and I could see a repeat of what I had done yesterday. He began finding ports using Nmap, putting in the server version of Apache into exploit.db to search for exploits, and attempted to use gobuster to find vulnerabilities – finding one in the development directory. 
Upon reading text files contained within the directory, Jason was able to find that SMB (Samba) could be exploited for this box. Samba essentially facilitated the sharing of files to anyone on a network with implicit trust.
He attempted to exploit samba using enumerating – infinitely looping and executing linux commands one after another. However, this process took an immense amount of time and Jason was unable to finish the box before lunchtime. However from seeing this demonstration, I was reminded of the similarities in process to Vulnversity, and the basic structure of going about web pentesting began to cement in my mind. 

## Working together 

I continued going through Vulnversity with Dylan, and he suggested we join forces and tackle an intermediate box together. A writeup for this box would be our deliverable for this week. We chose [Biohazard](https://tryhackme.com/room/biohazard#), an intermediate level box which was approved by our tutor Max. 

On Thursday and Friday, we finished off Vulnversity in preparation of starting Biohazard late Friday night.
A large obstacle in finishing that was of Burpsuite, in that both me and Dylan had never used it, nor its Intruder feature before. This feature was used to intercept a file uploaded with a file extension blocked by the server, and changed its extension before sending it and 'getting it past' the server's security. I encountered a minor issue that prevented me from progressing: in the form of an error stating that my payload was empty. Through continually clearing and re-adding payloads, I was able to get past this error, but I find that I cannot constantly replicate this success.

 ![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/4/chat.png)
Above: Communication with classmate Dylan relating to Open VPN and Vulnversity

Both Dylan and I then used Netcat for the first time to execute a reverse shell. Though the process was ultimately short, I had a misunderstanding in how netcat worked which greatly extended the amount of time I spent on this stage. I ran the netcat command expecting and awaiting an output that never came. I didn’t understand that Ncat itself was waiting for a payload that I executed by reaching the following ip address:
http://<MACHINE IP>:3333/internal/uploads/reverse-php.phtml
to generate a netcat session. When eventually I realised this and netcat output appeared, due to my newness to everything, I did not yet understand that I was on the reverse shell/the filesystem of the server. I took some to to research what exactly a reverse shell, and realised that I was already there, I could press any key to see that I was on the machine's filesystem..


I was then to find where SUID files were stored, and had no idea what to look for. I was forced to look up a guide and use a find command to go through directories wherein permission were no denied. The answer was systemctl, but I did not understand the reasoning why. With Dylan, we went through the process and researched SUID, finding that the reasoning was that the directory was the more recently created directory, and had a naming convention of system ctl that related to how SUID altered the system. The next step to gaining root access after finding this SUID reminded me of the demo that Jason did on Monday of Wakanda box. We located this folder and added a script within it, which te server would run for us even though we did not have execute permissions. This was referred to as a cron job. 

From Friday to Sunday, I got together with Dylan and communicated through Discord and Messenger to organise nightly sessions where we went through the box together.

 ![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/4/discordchat.png)

We worked for 3 hours per night from 9 or 10pm to 12:30am. We found that our lack of knowledge and newness to pentesting held us back from progressing at a faster rate, but we learned much on the way. For me, the biggest obstacle was encoding, and I began to realise that there were many different types of encodings and bases, which I needed to some further research on to understand.

#### Above: Photos of communication

 Upon starting the box we went through the regular procedure of running Nmap, and connecting to the server with the right port (it was a regular HTML port 80)
 
The initial rooms involved inspecting page source and decoding codes in a game-like setting. Initial rooms puzzled me with decoding from base 64, but subsequent rooms completely stumped me as I was to decode two or three times with different bases.
 Progressing from these, the box began to focus more around finding several emblems in different HTML pages. 

An entirely text-based code : klfvg ks r wimgnd biz mpuiui ulg fiemok tqod. Xii jvmc tbkg ks tempgf tyi_hvgct_jljinf_kvc
Revealed to me that not all of cybersecurity was simply using tools, but involved trial and error and recognising patterns in code. This code was deoded as a vigenere cipher, with a key provided previously in another room.

Due to time constraints and delays caused by unfamiliarity with all of these encodings, Dylan and I were unable to progress further on our box on Sunday. As a total coincidence, I was busy on Sunday and went Indoor Rock Climbing, where I happened to meet Jason (tutor), who egged me on to boulder a wall that I unsuccessfully attempted many times, and encouraged me to go home and finish this reflection after I was done climbing.

 ![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/4/googleteamsclimbing.png)
 Above: Asking Jason for help in Rock Climbing after meeting him there by chance

### A week of growth

This week all in all was characterised by a building of my knowledge of the web-pentesting procedure, and lots of hands-on exploitation of boxes together with my classmates.

This week I thankfully put in consistent work everyday, which allowed me to pace myself and make regular progress. However, despite my cooperation with another student (Dylan),I (and we) did struggle greatly in the later stages of Vulnversity and with encoding in Biohazard. We really spent as much time progressing, as we did backstracking, researching and reading walkthroughs.

Though my self-motivation has improved, and I am happy with the amount of progress I made this week, I want to be more consistent with putting in hours of research and completing exercises even when I'm not working on a box together with another person. I still procrastinate on completing writeups and reflections on the day that I complete tasks, and I should take notes while I'm going through each task, and finalise my summary of these notes at the end of each day.

For next week, I would like to continue learning and building on the foundations of pentesting knowledge that I now have. I'd like to ask questions that are not so involved with the small configuration and technical issues that bothered me in the beginning of the week, and delve more into complicated exploitations.

