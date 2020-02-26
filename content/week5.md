---
title: "Week5"
date: 2020-02-23T14:04:44+11:00
draft: false
dropCap: false
---
# Sprint 5: Tackling OpenAdmin
This week we were assigned to tackle an easy HacktheBox box. This was a week to use all the built up knowledge I’d gathered so far to crack a box blindly – there were no walkthroughs or write-ups allowed for these challenges.
For the box, I chose OpenAdmin just like many others in my class. Going into it, all I had was an Ip address and a lot of research ahead of me…

This week involved:
+ Cracking a box with minimal help (no write-ups online!)
+ Presentation from Cybersecurity Analysts from Deloitte
+ Getting stuck a lot and researching a lot of commands + concepts
### What is HacktheBox?
On Monday, I was informed that I was to tackle a HacktheBox Challenge by the end of this week. These challenges would have no write-ups and minimal relevant resources available online, and was significantly more difficult than the challenges I’d faced on TryHackme. 

According to my tutors Jason and Larry, though they were throwing us in the ‘deep end’ with these challenges - the hard work we put in to overcome this would pay off many times over in knowledge and improved proficiency. Furthermore, engaging in the site has some ‘official’ payoff, as attaining prominence on the leaderboard and engaging in challenges could potentially lead to gaining the notice of cybersecurity recruiters -> therefore opening new doors to future careers.

I was also told that I wouldn’t be able to comment or publicly release a writeup for any HacktheBox boxes I solved before they expired and were removed from the site. So as much as I’d like to comment on the commands I used and my struggles in detail here, I’ll instead gloss over them and focus on my experience instead.

### The First Hurdle
The first hurdle began then, as we found we couldn’t join the HacktheBox site so easily. In order to make an account, we needed to exploit the login page to create an access code. The solution was right in front of my eyes, but I still puzzled over the login page’s source code for quite some time. The solution was only slightly different to CTFs I’d encountered before, but this slight difference had me stumped for a few hours until I received some hints that opened my eyes.
My tutors suggested that we chose an easy box, such as Traversec, Postman or OpenAdmin. As many of my classmates immediately chose OpenAdmin, I decided to choose the same so that I’d be able to collaborate with them, and help each other if we became stuck. 

![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/5/invite.png)
##### Above: Invite code required to get into HackTheBox

I found that immediately, many of my classmates who had done more boxes in the past weeks, or had more pentesting knowledge, sped ahead with motivation and direction – and finished their box at a far faster pace than me. Particularly amazing was David, who spent 2 days staying up to 2am before he got root on Wednesday.

For me, I began Tuesday by trying to finish ‘Biohazard’ - the box Dylan and I hadn’t finished last week. We’d previously become stuck upon decrypting some codes that needed 2-3 levels of decryption – which would become incredibly time consuming if we went through every form and base manually. However, today we discovered that in the ‘Favourites’ options menu of Cyberchef, there was a ‘magic’ option. 

![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/5/magic.png)
##### Above: Magic Tool on Cyberchef


This option would perform most forms of decryption and return the result of all of them – but was also capable of decrypting multiple levels of a decryption at once! With this discovery, we were able to crack the codes we’d been previously stuck on, and get FTP user and password as a result. We found the next section was a cryptography section involving analysing image files and their file descriptions. 
I came into the drop-in on Wednesday, wherein I told my tutor Jason this, and learned that cryptography was limited in usefulness mostly to CTF challenges. It was not commonly applied in the real world or HacktheBox challenges (which simulated real world scenarios). Dylan and I decided then to leave Biohazard there for the week, and to prioritise OpenAdmin until the end of the week, as any further knowledge gained from Biohazard wouldn’t help us here.

That said, progress on OpenAdmin was not on my side on Wednesday. Though I stayed in the drop-in class for over 4 hours, I achieved what could’ve been done in 5 minutes or so with only managing to get one nmap scan and some recon scans in that entire time. My HacktheBox vpn continually failed to function (possibly due to interference on the site or with UTS wifi configurations), and prevented me from finding any meaningful information. I was incredibly frustrated to be stopped before I could even get to any parts of complexity.

Nathan and Pieter came in and explained their jobs. Their presentation involved explaining misconceptions about ‘hacking’, and discussing how their cybersecurity jobs 'actually worked'. In my view, the highlight of their presentation was their discussion on how Cybersecurity was split into three parts, Physical (cameras, doors), Social (phishing, social engineering) and Cyber (the actual ‘hacking’). This framework, alongside their descriptions of their day to day consultancy for Deloitte, reminded me that Cybersecurity ultimately invovles protecting a business, and involves a mindset that is more than just 'cracking code on a website', but also security in all forms, physical or no.

![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/5/deloitte.jpg)
##### Above: Class working on a box Deloitte provided for us

From Thursday to Sunday, I made steady progress on OpenAdmin. There were many times I became stumped on the usage of certain commands or what files to look for. My saving grace was being pointed many times in the right direction by classmates such as Dylan and Hayden, who helpfully pointed out that some exploits were plastered as the first search result on Google. They also hinted heavily when I was stumped on my direction upon reaching flags and sort of commands I would need to use next.

Thanks to this I was able to get user.txt on the box by Sunday morning (after being stuck since mid-Saturday), and got root in approximately 20 minutes after some pointers on Monday morning. I’d probably spent 3-4 hours each day since Thursday just staring and looking at semi-relevant documentation on Google, but I each hint I got accelerated my process tenfold it seemed. 

### Thinking back on how much help I got...
My biggest weakness this week was relying on advice and getting the feeling that for some parts of the box, I’d breezed too quickly through and hadn’t gotten there with my own effort. Admittedly, at those parts I was hopelessly stuck, and it would’ve taken me a day, or several days worth of research to figure out my problem. Yet regardless, I learned a lot going through this box - help or no.

For the future, I want to continue pentesting and increasing my technical expertise, so that I can easily gather information and tackle boxes entirely on my own. For this week, there were many times I caught myself reading irrelevant documentation for many hours, and could not easily find the solution to my problem. Yet as a result, I learnt much more about specific commands and how they worked - and upon getting hints and working with friends, I managed to talk about ways to exploit things in ways I wouldn't have thought before.

