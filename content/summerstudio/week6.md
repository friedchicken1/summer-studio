---
title: "Summer Studio: Week 6"
date: 2020-03-01T14:04:47+11:00
draft: false
dropCap: false
---
# Sprint 6: Tackling Traverxec
This week was the last week of the Summer Studio, and was filled with the chaos of finishing another HacktheBox challenge, preparing to present at UTS's Summer Studio showcase, and writing final writeups, reflections and portfolios before a final due date.

As I was struck by sudden illness during the week, I found it difficult to juggle, and was off schedule until the end.

This week involved:
+ Cracking another box with minimal help (no write-ups online!)
+ Preparing to present about OpenAdmin at the Summer Studio Showcase
+ Finalising writeups and portfolio for this studio
### First Preparations
By Monday, I and other students in the class were well accustomed to the rhythmn of this Summer Studio, and were well aware as to what we had to accomplish this week. At our final 'stand-up scrum', most of us reflected that we'd gained a decent grasp on the workings of pentesting, and a more resilient mindset towards problem-solving(surprisingly and funnily, my classmate Mihailo had realised the importance of calming his anger after much struggles and frustrations from pentesting). 

We were ready to begin work on our respective boxes positively and smoothly organised ourselves into groups to present on Thursday for the Summer Studio Showcase.

I began to work on the box Traverxec on HacktheBox (which caught me off guard as it began slightly differently to OpenAdmin), and joined a group with Hayden, Dylan and Nick to present upon the box we'd completed last week (OpenAdmin) for the showcase. We assigned portions of the pentesting process to cover from the '3 Es' (Enumeration, Exploitation and Escalation) to even the workload amongst members and agreed to meet again on Tuesday to lock down everything for the presentation.

![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/6/script.png)
#### Above: Script for Enumeration portion of presentation

I and other group members had been previously been informed by our tutors of the nature of the showcase; of how our onlookers would be constantly coming and going, and were people with varying levels of knowledge of pentesting. 

Our audience wouldn't typically be predisposed to long conversations about how the box worked in detail, in fact the opposite - they would likely be overwhelmed by a lot of information if they weren't familiar with the subject. We had to capture their attention and show them something interesting before they moved on with their day!

Keeping that in mind, we knew that we would do well to keep explanations informative but most importantly succinct. I was to cover the Enumeration portion of the Pentesting challenge, and for Monday, I focussed on streamlining down explanations of recon tools such as nmap and how/why we used it with our box.

On Tuesday, we met together from 11am to early afternoon to discuss and prepare for our presentation. However, our meeting suffered from the fact that we didn't have a clear agenda, and rather than further discussion on the logistics of the presentation, we ended up working on our own respective parts for most of the time we were together. 

However, it was decided soon after the meeting that Hayden, who had the most experience in pentesting, would record a demo for the box. We would use this recorded demo to demonstrate and explain the box on the day, and would similarly avoid any unwanted problems from running a live demo. Dylan would edit said demo, while Nicholas and I would create and polish informative slides for the presentation. Everything was set out and running smoothly.

However, during the meeting, I'd begun to develop a quite bad sniffle, and felt increasingly cold despite warm temperatures on the day. I'd originally planned to attend the Sectalks Ninja Night event that night - a Capture the Flag event periodically hosted at Google - but I felt like I was in no condition to attend after our group meeting. While I'd RSVPED over a week prior, I sadly cancelled it before heading home early.


I found by the next day that the sniffles had developed into a cold, and I was especially sick and feverish for the next two days. I had some difficulty working on my part for the presentation and Traverxec challenge due to some headaches and constant sniffling. Before the end of Wednesday, I'd gone for a checkup with my local GP where I was diagnosed with a common cold. I was able to obtain a medical certificate and contacted my tutor Larry on whether I should still attend the Showcase. 

![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/6/medical%20cert.png)
#### Above: Communication with Larry about attendance to the Showcase

![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/6/presentation%20chat.png)
#### Above: Informing my group of my unfortunate absence on Thursday

On Wednesday night, I informed my group that I wouldn't be able to attend the Showcase with them, but continued to do my best to contribute by joining our group's final preparation Discord Call to offer opinions and feedback on the box demo and script. I also wrote and created most of the content for our group's presentation slides on Canva.
![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/6/canvapresent.png)
#### Above: All of the slides from our Canva Presentation

While devastated that I would not be able to attend what felt like the natural conclusion of my Summer Studio experience, I'd still done my best to contribute to my group's preparation on that night.

![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/6/enumerationslide.png))
#### Above: One of the slide's I'd created, aimed to be as succinct for ease of understanding from onlookers

On Thursday, I was thus unable to attend the Summer Studio Showcase, and recovered at home. With the showcase passing without my attendance, I rested and did not make meaningful progress until Friday night and Saturday, where I was able to make decent progress in Traverxec and ultimately find root. As with the previous week, I was able to work with classmate Dylan to research exploits to enter the system and find vulnerable files within the system. We used a Discord call to communicate, and Hayden and Nick regularly joined and worked through it with us. I really felt like I was able to learn better with all of our minds working together.

Traverxec was significantly easier than OpenAdmin as a whole, and I was greatly aided by the knowledge and commands I'd learnt from cracking OpenAdmin the week before. Due to the similarity of many parts of these two boxes, I found that I took almost less than half the time I'd taken to crack OpenAdmin to crack Traverxec this week, though I was stuck on the gimmicky nature of finding root for quite some time.

However having achieved root by Saturday night, I was able to rejoice thatI'd accomplished all the pentesting I'd needed to do for this subject, and able to begin to to focus on more literary components. Though I had a prior commitment on Sunday, I had all of Monday to polish up my reflections, writeups and begin my final portfolio for this studio! - and I had mostly recovered from my cold by then and was in a healthy physical state too.

While an entire day sounded like a large timeframe at the time, I found that I had greatly underestimated the amount of time I would require. My biggest error was my bad habit of not writing my writeups of my HacktheBox challenges as I went, and I spent easily 3x as much time as I'd originally set aside. I found that I easily forgot parts of a box I'd done but days before, and regularly redid parts to refresh my memory as I continued writing. I was also forced to redo research and read extra in-depth to be able to verbosely annotate each command I used. 

There were many commands (especially the multi-lined netcat remote code execution exploit) that I'd simply found as online scripts and understood generally, but were unable to explain. I put in quite some time to iron out my understandings of the workings of certain commands and how they worked in relation to other simultaneous commands.

### A busy week, and I was unable to address my weaknesses from previous weeks.
I feel like this was quite an unfortunate week, and my schedule was thrown off quite early by my sickness. This meant that I was unable to work everyday on my box as I'd resolved to in earlier weeks, and I was able to make meaningful progress only at a later date in the week after recovering adequately.

As an improvement over last week however, I was able to overcome Traverxec in much less time, and regardless of my resolution to work through a box alone last week, I ultimately learnt a lot through mutual research and cooperation with classmates this week. I found that there were incredibly resilient, positive mindsets to keep presssing problems, and a spirit of cooperation in working together to find exploits that I was exposed to and benefitted from only because I had the privilege of working on the box alongside others. I myself was surprised with the speed that I learned and progress thanks to this.

Three resolves from previous weeks lay unachieved:
1. To work through a box entirely with my 'own' power and research. 
2. To complete work at a consistent rate throughout the week
3. Achieve more communication with stakeholders, including tutors but also presenters/attendees to the Showcase 

It's a shame that this last week brings with it a lack of resolution to these three things. Now that the studio is coming to a close, I wish there was another week for me to prove to myself that I could overcome these resolutions! But ultimately, I'm happy with the fact that I was able to successfully crack Traverxec and contribute adequately to my group's presentation this week this week - if not for my illness I could've done this and more!


