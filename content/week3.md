---
title: "Week3"
date: 2020-01-23T14:04:31+11:00
draft: false
dropCap: false
---
## Sprint 3: Self-study with pentesting and Web-based Attack Last week, 

I’d lamented that I hadn’t put the learning resources I’d been recommended by my tutors to greater use. I’d resolved that for this week, I’d improve on my own motivation in running these resources outside of class hours.  I’d also sought to make the group presentations that I participated in more organised and to maintain better communication between members.

This week involved:
+ Introduction to new pen-tester websites and learning resources
+ Performing a group presentation detailing Broken Access Controls

### New learning resources
 On Tuesday I was introduced to the OWASP juice box. This was an environment wherein we were to test for web vulnerabilities, gamified into a list of challenges and ranked from 1 to 3 stars according to difficulty. This sort of environment was like being thrown into deep water to fend myself – the environment itself did not teach us how to solve its challenges, but we were to use resources such as Google and the Hacksplaining website to figure out successful exploits. 
owasp juice shop
https://spacesnottabs.herokuapp.com

A challenge I took on was ‘ ‘
I wasn’t sure how to tackle this challenge. I viewed page source and inspected elements on the page, but wasn’t sure how to progress with this challenge given my limited technical skillset at this time.  I couldn’t imagine what to change to reveal the picture – and out of options, I ended up searching Google for a solution to this exercise. I discovered that I was to change parts of the url, specifically I was to replace a # with %23, as html was unable to read it. I knew I wouldn’t have been able to even think or understand this solution without the help of an answer from google, so I treated this as a learning experience. I would feel worse if I encountered a similar problem in the future and didn’t know how to handle it, however. 
The next challenge I undertook was to give the website a 0 star review. For this case, I attempted to inspect each individual button and rating on the page. The review form would not submit if I did not select an amount of stars from 1-5, so at first I attempted to edit the html on one of the star elements, and change the its highlighted state to ‘false’. However, I think that change affected only on the client side, from a visual standpoint – and it didn’t actually alter the rating that I submitted. I found the solution after overhearing fellow classmates struggling on the same challenge, and together we found from continual interaction with the page, that the ‘submit’ button element gained a 

