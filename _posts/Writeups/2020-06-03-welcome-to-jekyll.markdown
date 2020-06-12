---
layout: post
title:  "Lian_Yu Writeup"
date:   2020-06-03 10:29:40 -0400
categories: Writeups
permalink: "/Writeups/Lian_Yu"
---
## Welcome this is a writeup for the TryHackMe.com room [Lian-Yu](https://tryhackme.com/room/lianyu)
![LianYuCard](Images/Lian_Yu \Card.PNG "Lian Yu Room card")
While doing this room i ran into some interesting challenges that made me really think hard! i would recommend it for any beginner!
We start by doing a basic nmap scan

[![NmapScan](/pathpending "nmap scan of the machine")]

we can appreciate 3 ports that will become of interest such as port **21, 22 and 80** now that we see port 80 is open we should head over there to check out what we're working with

[![LianYuWebsite](/pathpending "Website of the room")]

Seems innocent enough, so let's start!

\#2 What is the Web Directory you found?
This is easy enough just run a web directory search tool on the ip till something pops up and sure enough (i'm using gobuster cuz i like it you can use something else)

`$ gobuster dir -u machineip -w /wordlistpath` 

[![LianYuHiddenDirectory1](/pathpending "Hidden sub directory")]
Well gobusterfound a hidden directory and it seems to be a pretty simple site giving us a code word but it can't be seen but using the command `curl -i machineip` we get a result very much like the next:

[![LianYuCurl](/pathpending "Curl of hidden site")]
and we can see the hidden message 

