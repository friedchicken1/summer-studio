---
title: "Summer Studio: Week3"
date: 2020-02-09T14:04:31+11:00
draft: false
dropCap: false
---
## Sprint 3: Self-study with pentesting and Web-based Attack 

This week, I was given an overview document of how to structure my learning by my tutor Jason, and had the time and resources to self-study. I was introduced to OWASP Juice Box and Natas - as testing resources, and worked on a group presentation wherein I detailed one of OWASP's top 10 web vulnerabilities.

![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/3/jasonstudypath.png)
##### Above: Overview document from my tutor Jason, of how to structure my learning

Last week, I'd been disaapointed that I hadn't put my time and resources outside of class to great use. This week, while I'm happy with the amount of effort I put in during classtimes and with my group presentation, I feel like I've frustratingly gone back to the pattern of procrastinating and doing what feels like the minimum outside of classtimes. 

This week involved:
+ Introduction to new pen-tester websites and learning resources
+ Performing a group presentation detailing Broken Access Controls

### New learning resources
 On Tuesday I was introduced to the OWASP juice box. This was an environment for testing web vulnerabilities, gamified into a list of challenges. Each challenge was ranked from 1 to 3 stars according to difficulty. My initial feeling in working on these challenges was like being thrown into deep water to fend myself – the environment dud bit inherently teach us how to solve its challenges, and the general knowledge I had acquired in the past few weeks did not help me here.
 Alongside my other classmates who seemed to be in the same boat, I used my common sense and what resources I could find off Google and Hacksplaining to solve what challenges I could.

A challenge I took on was ‘Retrieving the photo of Bjoern's cat in "melee combat-mode‘. This challenge meant that I was to reveal an image of a cat in the 'Photo wall' page of the Juice shop website. Currently the image was not displaying, and was replaced by placeholder text.

I quickly became stuck in this challenge. From what basic tools I knew t o use, I viewed page source and inspected elements on the page. Despite this, I wasn't able to properly interpret everything I read given my limited technical knowledge at this time. From what I could see - I had no idea what to do to reveal the picture, or what was wrong, so I eventually I caved and searched Google for a solution.

I discovered that while I was inspecting the placeholder for the image, I was to replace instances of # in the url with %23. The answer was that the browser was interpreting these as HTML anchors, rather than part of the URL, and the solution was to URL-encoded as %23. I wouldn't have understood this solution had I not read it, so though I felt guilty for not being able to get it on my own, I felt that this was a viable way for me to learn everything for the first time.

![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/3/revealingcat.png)
##### Above:The cat image revealed (leftmost image)

The next challenge I undertook was to give the website a 0 star review. For this case, now having the knowledge that things may be amiss if I inspect certain elements on the page, I attempted to inspect individual buttons and rating stars on the page. I found the review submit button was greyed out, and the form would not submit if I did not select any stars (1-5 stars). I thought the problem was with the stars, so I at first attempted to select 1 star, then edit the element html of the star element so that it's highlighted state would change to 'false'.

Visually, this meant that there were no stars highlighted on my page, and I was also able to submit since I'd previously chosen a star rating from 1-5 stars. However, the change was entirely visual and client-side. and it didn't actually alter the rating that I submitted. 

Temporarily, I was lost for solutions, but overheard my classmate sitting 2 seats away, David, worrying about this challenge as well. We continued interaction with the page, and found that the submit button's state was disabled unless we selected a star rating, wrote a comment and finished the captcha.

![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/3/0%20star%20rating.png)
##### Above: Button disabled state was 'true' unless we filled out these 3 parts of the form

Not by editing the stars, but by editing the button's disabled state to 'false' we were able to disable the client-side authentication on the form and submit without touching any star rating. And thus completed the 0 star review challenge. 

### Access Controls
I worked on a group presentation detailing the OWASP web vulnerability of Broken Access Controls, with my fellow members Anthony and Dylan. The presentation was to be given on Thursday morning, and had a time limit of 6 minutes.

We agreed to use Google teams to communicate, with Anthony recommending Notion to manage our workflows and Dylan insisting on Canvas as our presentation medium. While I knew Canva could not be edited concurrently by multiple people, and I'd never used Notion before, I saw that both were visually appealing applications and were easy and intuitive to use. So I agreed to using both Notion and Canva happily.

![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/3/teams.png)
##### Above: Google Teams Chat to facilitate initial communication

By the end of class on Monday, we'd agreed to meetup on Wednesday to get our assignment knocked out together at uni. The time would be from 10am to whenever we needed, and we'd divied our parts and sorted out what parts we would be working on that day.

![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/3/notion.png)
##### Above: Our Notion workflow  

Knowing that, I busied myself with other commitments until Tuesday night, when I finally hopped back onto my desktop and was shocked to see my Google teams full of notifications that I hadn't seen. My teammates had been communicating frequently, and since I'd not had regular access to my desktop - I had seen nothing. I prompt'y installed the Google Teams phone app and continued communication on both Messenger and Teams. We were able to iron out the exact times and booked a study room for the next days work.

![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/3/messenger.png)
##### Above: Messenger conversation confirming our meetup time

On Wednesday we came into UTS from 10am and worked until 5am. Around 11am, we discovered that some of our points overlapped, and Dylan had gathered some information that could've been used by Anthony (who was covering 'What the attack was'), who was to explain 'How our attack worked'. 

However, since we had met in person, it took only a short conversation to restate ourpoints and finalise exactly what we were covering. Dylan ended up giving that section to Anthony, and I was able to eliminate parts of my research that I found was being covered by the two of them.

We used Notion to write our scripts, which let us view each others edits in real time, and share useful URLs we found during research. Canva was only editable by one person at a time, so as we finished our parts, we communicated to each other IRL and took turns to edit the presentation. Despite this inconvenience, we were able to smoothly complete the slides and script, and went home before timing ourselves (we reached about 5:30-5:40 approximately), finalising presentation formatting and checking over a few versions of Anthony's voiced over demo slide.

![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/3/impactcanva.png)
##### Above: Opening slide of my section of the presentation in Canva

When the presentation came on Thursday, it ran smoothly. We were given 15 minutes prior the presentation to prepare, and that proved essential. We practiced twice, the first time taking roughly 6 min 5 seconds (overtime), and prompting us to cut the fat from our scripts. I was able to identify unnecessary, wordy parts of my presentation and culled them, as did my groupmates, and we cut the second time to 5 minutes and 30 seconds which was more than enough. Overall it was a pleasure to work with Dylan and Anthony in this presentation, and we were able to get everything done and iron things out quite early.

![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/3/script.png)
##### Above: My script on Notion for the presentation. After the practice on Thursday morning, I removed the example for each Escalation category to save time.

### Natas and self study
From Thursday to Sunday, I worked on Natas on the OvertheWire website, and used Hacksplaining and OWASP lists to make notes about the basics of Pen testing.Unlike Bandit, Natas did not seem to require Linux, nor for me to run a Virtual machine. Initial levels were solvable by viewing page source, and finding passwords in comments.

A notable level was Lvl 2, wherein viewing page source didn't immediately give me the password. However, appending /files to the url, and opening the files directory did reveal an additional .txt file that contained the password.
![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/3/lvl%203.png)

I hit a wall with Lvl 3, where the page source and page revealed nothing at all. Having been recommended to try Burp (which I had not touched as of yet), I spent the final hour or so of class installing said application. Initially, I was confused as to how intercept worked, and was frustrated when I couldn't open any webpages while I had Burp running and my proxy enabled. After asking my tutor Larry, I found that it was infact an intended functionality to read and intercecpt traffic, and I was to forward through all of the intercepted traffic before I reached a webpage. I tested this on Youtube, and while slow, it did work as intended. Having achieved this, I packed up and went home.

Therein lay my mistake. After Thursday, I feel that I failed to schedule a time each day to dedicate myself to learning Pen testing. Come Sunday, I found that the guilt of not having done anything for the past 3 days was killing me, so I told myself to start off easy - and following from Jason's recommended study path, took notes detailing OWASP's top 10 and ran through a bit of Hackersplain.

![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/3/notes.png)

### Problem lies in scheduling and motivation
While I'm overall satisfied with my in-class efforts and group contribution from Monday-Thursday, I'm wholly unsatisfied with how much I studied outside of class, from Thurs-Sun. I wanted to work on my practical skills much more, and make discernable progress in a pentester testing lab of some sort, as I feel my practical skills are still preliminary.

I was able to increase my understanding of Web application pen testing and web vulnerabilities thanks to research his week. But I feel that my practical skills are behind, and will continue to lag behind my cohort if I do not regularly commit myself to study from now on. The next week may be rough if any new tools are introduced, and if I don't force myself to catch up and learn at a consistent pace.