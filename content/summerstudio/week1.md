---
title: "Summer Studio: Week 1"
date: 2020-01-23T14:04:22+11:00
draft: false
dropCap: false
- name: featuredImage
  src: "Filename of the post's featured image, used as the card image and the image at the top of the article"
---
## Sprint 1: Creating a Blog
In this first week of the Cybersecurity Summer Studio, I was tasked with creating a blog to record my thoughts and reflections for the following weeks.

I'd never created a blog before, and initially I was pretty confused as to where to start and what this involved. 

### Thinking about Installation
As with working with anything I.T related for the first time, there were many things to install before I could even begin on my actual work and blog content. This affected my time management as the time it took for setup far exceeded my initial expectations, and slowly began to overtake the time I had allocated for writing blog content.

For this blog, I setup:

- Hugo (a static site generator that uses markdown syntax)

- Chocolatey (a package manager that I used to install Hugo)

- a Github repo (to store the files that constituted the webpages of my blog)

- Netlify (create a site based on my Github repository)

- a Namecheap Domain (free from Github Education pack)

#### But how did it all come together? 
By Wednesday (22/01) I had become thoroughly lost and overwhelmed by this list despite reading and rereading the Wiki provided on the Studio's Google Teams group. I resolved to ask for clarification before I proceeded. At this point I had no knowledge of what exactly was required to setup, and how it functioned together to make a working static site. The next day, on Thursday (23/01), I asked my tutor, Jason Ko - who brought me to the whiteboard and explained the whole process.

![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/1/whiteboardexplain.jpg)
##### Above: Whiteboard explanation of process by Jason Ko

He explained that everything I'd found in the list to setup was connected - in order to build and deploy this static site. 

The structure and look of the site would be built using Hugo, my files would be stored online in a Github repo, and this repo would be used by Netlify to create a site. This site wouldn't be publicly available until I setup a custom domain - to that end I acquired a domain name from Namecheap. 

Everything was so much clearer after understanding this framework. I now worked on setting everything up individually, and I was supported by my knowledge of how everything was meant to link together.

### Unexpected Problems
For the most part of my setup, I followed a Step by Step guide which was incredibly helpful and self-explanatory, until Sunday night (26/01), when it wasn't.
![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/1/hugo%20orig.png)

##### Above: Step 5 of the guide, my main resource for setup for my static site (https://www.netlify.com/blog/2016/09/21/a-step-by-step-guide-victor-hugo-on-netlify/#building-your-site)

### This configuration did not work for me, as my Netlify deploy Failed :(
![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/1/netlify%20error.png)
##### Above: Status badge indicating failure of Netlify deployment

Despite copy pasting the error output and error number into Google, try as I might I was unable to find a working solution. To solve this problem (which I hoped was simple enough -it was likely a single command or directory name holding me back), I asked a fellow student from the Summer Studio, Nicholas Zay, on his solution to this problem. 


![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/1/hugo%20fix.png)

His difference - he just used 'Hugo' as the build command (which was the correct command). While I was able to later confirm that this was the correct build command, it yet did not eliminate all of my errors at this time.


Stuck again, I again asked one of my tutors - Jason for help on the error and found that the fix was adding a missing environmental variable. This hadn't been mentioned in the Step by Step guide - and I had not arrived to this solution in my copy-paste searches of my error codes. 

However, it did work, and thankfully this was my last fix. 


![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/1/environmental%20variable.png)


Immediately after I was able to build the site successfully, but that was to be my last work for Sunday night. The content of this blog was left to be written on Monday, a day on which I was also working. While I had planned on running some of the wargames recommended to the class by Larry before Week 2, I'd run out of time by Monday night to complete them. 

#### Perhaps, in reflection, I could've managed my time better.

I could've asked all of my questions early, such as by Thursday or Friday night. Friday and Saturday were days I'd made minimal progress on this task, and I'd planned my work for this subject into a set amount of tasks per day. I'd simply run out of days by Monday to run the wargames I'd really wanted to try before the tutorials.

## Learning Contract
![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/1/learning%20portfolio.png)