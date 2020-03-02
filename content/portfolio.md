---
title: "Final Portfolio"
date: 2020-03-02T14:04:27+11:00
draft: false
dropCap: false
---
## Who am I?

I'm Tyrone Huang, a 3rd Year UTS student studying I.T and International Studies. I'm majoring in Interaction Design, with a submajor in Enterprise Systems Development. I pushed myself to take this Summer Studio relating to Cyber Security to expand my horizons outside of programming subjects, and to test the waters in which career path I would like to take in the future!

## SLO 1 - Engage with stakeholders to identify a problem
#### “The art of war teaches us to rely not on the likelihood of the enemy's not coming, but on our own readiness to receive him; not on the chance of his not attacking, but rather on the fact that we have made our position unassailable.” Sun Tzu

In the second week of this Summer Studio, guest speaker Robert Mitchell ended his presentation with this quote. This quote about war, while from a man who has been long dead for over 2000 years, could be used to summate the experience of a Cybersecurity analyst in the modern age. Though the quote mentions a 'position that is unassailable', it alludes to the opposite - to the problem idea that most positions, and most systems, are in fact 'assailable', or 'crackable'.

Prior to beginning this Summer Studio, I always had a slight prejudice - that 'hacking' or cyber attacks were purely malicious acts, that trying to recover or prevent these attacks was lawful. Yet upon understanding the concept of 'pentesting', and hearing the testimonials of experts such as Robert Mitchell or Pieter and Nathan from Deloitte, I begin to realise that lawful individuals (such as Cybersecurity analysts) can indeed use what might be the 'evil' act of hacking for good.

In relation to that, my biggest shock from Pieter and Nathan's presentation was of how many avenues of attack they used on their own system. The mentioned of three parts of Cybersecurity - Physical (cameras, doors), Social (social engineering) and Cyber (actual 'hacking'). Each day, they devise new ways to break into their own systems through any means possible - because it is possible, one way or another. And they just need to find out how and why.

The problem, I've found after listening to all these experts - is the extricable link between red teamers who 'attack', and blue teamers who 'defend', in creating something that is secure and 'impregnable.' A successful penetration test should still aim to improve the effectiveness and efficiency of the existing security controls in place. There is no denying the significance of an 'Offensive Mindset' in cybersecurity when attempting to create something impregnable and secure.

## SLO 2 - Apply design thinking to respond to a defined or newly identified problem
My understanding of challenges and applications of design thinking to overcome them changed greatly throughout the course of this subject. Each week, my understanding of how the pentesting process changed slightly as I was difficulty rose, learning firstly unix commands from Bandit and Natas, of Web Vulnerabilities from OWASP, until I became familiar with tackling CTF challenges from TryHackMe and HackTheBox.

The more I was exposed to, the greater my scope grew, and the research I needed to complete each step increased exponentially. What began at straightforward as entering a system with a provided password, and learning the 'ssh' command in bandit lvl 1, soon became an interation through the greater structure of pentesting as a whole: 

![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/4/process.png)
#### Above: Pentesting Procedure as depicted in tutorial slides

I found myself regularly applying this procedure as I went through more complicated boxes in TryHackMe and HackTheBox. While there are many variations of this procedure (Enumeration, Exploitation, Escalation), they boil down to using certain tools to achieve information gathering or exploitations at certain stages.
Enumeration: nmap, netdiscover, gobuster/wfuzz
Exploitation: 
Escalation: sudo

## SLO 3 - Apply technical skills to develop, model and/or evaluate design
I found that in this studio, I was given every opportunity and resource to succeed, with the tutors just one message/call away for aid. Each and every week, I was challenged to tackle something entirely new, feeling entirely out of my depth each time, and yet I was somehow able to push myself and overcome it every single week. Now that I look back on it, I've come a far way in terms of technical skills and self-expectations.

#### Week 1:
I created a Static Webpage that I used as a blog for the rest of this subject, requiring: 

- Hugo (a static site generator that uses markdown syntax)

- Chocolatey (a package manager that I used to install Hugo)

- a Github repo (to store the files that constituted the webpages of my blog)

- Netlify (create a site based on my Github repository)

- a Namecheap Domain (free from Github Education pack)

#### Week 2:
I began to engage with Wargames on OverTheWire:

- Kali Linux (a Linux Distribution aimed at penetration testing, run from a VM on my desktop)

- OvertheWire: Bandit (a basic series of wargames aimed at absolute beginners that allowed me to practice basic Unix skills)

#### Week 3:
I delved further into Web-based attacks with the introduction of: 

- OWASP Juice Box (an environment for testing web vulnerabilities, gamified into a list of challenges)

- OvertheWire: Natas (a series of wargames teaching me basics of server side-web-security)

#### Week 4:
Tackling basic CTF challenges (and honestly reading a lot of walkthroughs to understand each and every command):

- Vulnhub (Basic Pentesting)

- TryHackme (Vulnversity - an informative box that helped me understand each step of the pentesting procedure, and Biohazard - a CTF based on popular video game Resident Evil)

#### Week 5:
Tackling boxes on HacktheBox with minimal helpful resources online
- Attaining an invite code to HacktheBox through exploiting the login page
- OpenAdmin (an easy-level HacktheBox challenge, which used an actual OpenAdmin application)

#### Week 6:
Tackling more boxes on HacktheBox
- Traverxec (practicing my skills on another easy-level HacktheBox challenge, which caused me to spend hour and hours reading over commmands and documentation)

I never expected to be able to successful in completing all these challenges laid before me in this subject, but I found that constant failure, frustration and research really forced me to read documents and code like I never expected to, and opened my eyes to concepts that now seem exceedingly obvious. For me, it seems like each spike of difficulty I was stuck on was impossible at the time, and obvious upon looking back, but after all of it has been said and done it truly has been a rough learning experience of almost two months that helped me develop my technical skills. Simply being at a level now where I understand the very basics of pentesting, makes the past seem so simple and smooth-sailing in comparison.

## SLO 4 - Demonstrate effective collaboration and communication skills
I feel that within this Summer Studio, this SLO was the one that I found greatest difficulty in hitting consistently. In earlier weeks, I felt thoroughly out of my depth and unqualified to ask questions and engage others on what they seemed to already know. In a One-on-One session in Week 2, I remember reporting that I 'didn't know what questions to ask', and feeling like 'I didn't know what I didn't know. Which was everything.' There were many times when I would be taught a new concept, but from a lack of exposure to the context of said concept, I would fail to understand its importance and how it functioned in the process of pentesting.

However I really feel that my cohort and tutors in this Summer Studio were incredibly friendly and encouraging - often pushing me into depths of unknown knowledge that I was too afraid to tread myself.
From early weeks I was introduced to many platforms with which to communicate and cooperate with my cohort.

### Google Teams 
Which I used to communicate for my first group presentation on a cybersecurity tool 'Nikto', and which I used to contact my helpful tutors for help or advice, even late into the night at times.

### Notion
A note-taking application that my second group used to prepare scripts to present on OWASP vulnerability 'Broken Access Controls', and eventually, seeing the useful commands and usable UI of this app, I started using this for my HacktheBox writeups. This application was especially useful as multiple people could collaborate and write at the same time, allowing us to share ideas and edit each others work seamlessly.

### Canva
A design platform that my second group used to create Presentation slides for 'Broken Access Controls', and which I used to display content for my presentation group for Summer Studio Showcase. While its templates were visually attractive with little need for configuration unlike Microsoft Powerpoint, it's main drawback was of an inability for multiple people to edit at a time. I found the visual appeal was worth the wait for my groupmamtes, though.

### Discord
Ultimately, most of my collaboration and communication throughout this Studio was conducted on Discord, where I was able to conduct voice chats, text messages and livestreasm with other classmates with the aim to collaborate during CTF challenges and prepare for group presentations. I was able to work simultaenously on CTF challenges such as Vulnversity, Biohazard and OpenAdmin with my classmate Dylan, which was a learning and useful experience for both of us as we were both relatively new to pentesting. I found we often were forced to research independently when we were stuck during a CTF, but were able to share resources or scripts we found through Discord's chat service, allowing us to ultimately discuss and share our combined knowledgeknowledge, and progress through challenges that one of us might not have had the patience to weather alone.

I found by later weeks into the Studio, I was altogether comfortable speaking with both my cohort and tutors with any problems or fears I had at the moment. I still found it difficult however to ask questions on the spot to stakeholders such as guest speakers, and didn't always know the right questions to ask when I was stuck in a challenge, so I do think I could improve in those areas by being more proactive in my questioning. I do think, all in all, that I have gained a large amount of confidence to communicate with my peers thanks to the closeness of this studio.

## SLO 5 - Conduct critical self and peer review and performance evaluation
I found myself critically analysing myself each and every week, and I feel like this may have been one of the SLOs I engaged the most. I was very aware while moving forward each week, of the things that I had achieved or failed to achieve, and of concepts that I had grasped fully or which I had begun to forget already. 

In the beginning, I was aware that the studio was learning at a speed relatively fast pace, owing to the fact that I then knew nothing, and everything was a new experience. I'd come into this subject ready to absorb everything as a blank slate which had not had much prior experience with Cybersecurity, and found myself very self-critical at times when I did not achieve goals at a timely rate for the fear that I would fall behind.

I feel that work ethic and procrastination was a plague to me for completing goals regularly throughout this studio, but this was not for lack of motivation - after several weeks playing with the basics and concepts of pentesting, I began to understand the rhythmn of weekly sprints and the commitment it took to engage in challenges and CTFs. While my aptitude for finishing boxes was not the highest, and I was never first to achieve root, I did find it fulfilling to take my time and learn about each step and each command/exploit one at a time - sometimes excruciating painfully.

While I spent a lot of time reflecting on my shortcomings of last week, I never really took the time to imagine how far I could go, or how much I could learn in a week. Looking back, one, two, three weeks, I realise that I was blind to the progress that I was making, and things that I imagined to be impossible only weeks before, were becoming normal with each passing week. (like getting root in Traversec, I NEVER would have believed myself if I thought I would've been able to just weeks earlier)

# Conclusion
I really did learn so much in these 6 weeks, achieved and learnt far more than I thought I could have, and was able to thrive in an environment which was so open, friendly and helpful (with both students and teachers). I feel like I haven't experienced such a class in UTS ever before, where knowledge was so freely shared, introspection so valued and progress so celebrated.
