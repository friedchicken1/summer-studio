
---
title: "TryHackMe: Biohazard Writeup"
date: 2020-02-16T14:04:31+11:00
draft: false
dropCap: false
---
# Biohazard
This writeup is still a work in progress. I’ve spent daily sessions of 2-3 hours.(including procrastination) for 3 days with my friend and classmate Dylan Tchan working through this box. We both are relatively new to pentesting and are going through everything for almost the first time. 

As of now, we have yet to complete this box, but we aim to complete it soon!

## This challenge may be found [here](https://tryhackme.com/room/biohazard#)
#### Note: Ip Addresses in the URL may change, as the box was redeployed several times throughout the course of this writeup
Starting from the Biohazard webpage on TryHackMe.com, I joined the room, initiated TryHackMe’s OpenVpn and deployed the box.
 ![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/writeup/nmap.png)
Starting off by using an nmap scan, I was able to find 3 open ports. Port 80 was open: a port normally reserved for HTTP communication. This suggested that I could run the challenge normally through visiting the website’s HTML webpage.
 ![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/writeup/front.png)
The first page contained the team name: of Stars Alpha team, and a hyperlink to the next page, /mansionmain/.
 ![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/writeup/mansion.png)
There is nothing apparent upon entering the Mansion, but upon inspecting source code, I found a comment stating the next room was the /diningRoom/
 ![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/writeup/dining.png)
Within the Dining room, a hyperlink provided me with an emblem: emblem{fec832623ea498e20bf4fe1821d58727}
 ![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/writeup/emblem.png)  
A form input appeared, but inputting the emblem did not work as of yet. There was nothing apparent to use this for at this time, so I saved this for future use.
After checking source code in /diningRoom/, I found a comment which I decoded using the website CyberChef, from Base 64.
 ![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/writeup/dinehint.png)
  ![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/writeup/dinehintde.png)
The decoded output directed me to the /tearoom/, where apparently ‘The nightmare begin’
![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/writeup/lock.png)
This room contained yet another hyperlink, which provided me with a lockpick:
lock_pick{037b35e2ff90916a9abf99129c8e1837}

Again, not sure what to do with this at this time but I kept this information. I moved onto the art room as the text suggested me to do.
The art room contained a hyperlink to a page with a list of rooms, called a ‘maproom’.
![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/writeup/map.png)
This was essentially a directory pointing to a bunch of new rooms which I would explore from here out. I began with the barRoom, which was next on the link. 
![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/writeup/bar.png)
A ‘piano’ is contained in this page, which requires some sort of flag I have obtained.
Underneath this input, is a hyperlink which provides a music note.
![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/writeup/barnote.png)
Putting this through a base 32 decoder provided me with a music sheet flag
music_sheet{362d72deaf65f5bdc63daece6a1f676e}
![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/writeup/barnoteen.png)
I put this music sheet into the piano input, which directed me to a /secretBarRoom/
![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/writeup/secretbar.png)
This secret bar room contained a hyperlink providing a gold emblem.
gold_emblem{58a8c41a9d08b8a4e38d02a4d7ff4843}
![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/writeup/goldemblem.png)

I inputted the original emblem that I retained from the dining room into the new input that appeared on this page, which gave me ‘rebecca’.
![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/writeup/rebecca.png)
I initially assumed this was a ‘user’, and saved it for future use.
As the original emblem I just used came from the dining room, vice versa, I assumed the gold emblem I had just received from the secret bar room could be used back there.
Inputting the gold emblem into the diningRoom form, I received a jumble of words. klfvg ks r wimgnd biz mpuiui ulg fiemok tqod. Xii jvmc tbkg ks tempgf tyi_hvgct_jljinf_kvc
![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/writeup/diningemblem.png)
After some trial and error, I placed this into the Cyberchef websites as a vigenere cipher, using Rebecca as a key. The key required only letters, and the jumble of letters was already contained within the input, so this was what I found to be successful.
![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/writeup/shieldde.png)
The output suggested that I should add the_great_shield_key to the url back in the diningRoom, which provided me with the shield_key. This would be used later for rooms requiring said key.
![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/writeup/shieldkey.png)
I continued down the list to diningRoom2f, which contained no hyperlinks. 
![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/writeup/dining2f.png)
However, upon inspecting element I found a comment.
This took a great while of trial and error, but I was able to decode it from rot13. Apparently the gem could be find by appending /sapphire to the diningRoom url:
blue_jewel{e1d457e96cac640f863ec7bc475d48aa}
![alt text](https://raw.githubusercontent.com/friedchicken1/summer-studio/master/data/img/writeup/bluejewel.png)
This would be used in the subsequent Tiger statue room


Entering the Gallery room and checking out its hyperlink revealed the next stage of this challenge. I was to find 4 crests in total, with the second provided here.
The criteria of solving this crest was that I had to decode it twice, and the output was of length 18 characters.

Through extensive trial and error with Cyberchef, I found that it was to be decoded from base 32 and then base 58: 
h1bnRlciwgRlRQIHBh -crest 2
I saved this and set out to get other crests.

The Attic
Using the shield key from earlier, I was able to enter this room.
This contained a hyperlink which lead to crest 4. It appeared that this had no criteria to decode unlike crest 2. 

gSUERauVpvKzRpyPpuYz66JDmRTbJubaoArM6CAQsnVwte6zF9J4GGYyun3k5qM9ma4s

Armour Room
Similarly to the attic, I was able to use the shield key and enter this room. This room contained a hyperlink which led to crest 3, which was to be decoded thrice.
