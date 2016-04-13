---
title: Tips to keep your sanity while working with Adobe Experience Manager (AEM)
author: Fredrick Dominy
layout: post
comments: true
tags:
- AEM
- CMS
- tips
---

SO I just recently joined a the wonderful Seattle branch of [R2integrated](http://www.r2integrated.com/). R2integrated is an awesome company to work for and the people are great! I'm two weeks in and loving it!

I was hired on primarily due to my experience with Adobe's Experience Manger (AEM), which is a marketing content management system for large companies that want an integrated marketing campmaign for their new product or service offerings. AEM is the best of the best.

One snag however is this: Developing in AEM can be a little persnickety, especially if someone (like me) hasn't developed on it for about six months. So here is a short list of things that have helped tremendously to keep my AEM development sanity. 

---

* Sit next to an AEM expert.  (This one is absolute gold, and should be non-negotiable if you are new to AEM development)
* My friends Ryan Chapel and Tristan Hughes offer a few tidbits (They are both experts):
    * The documentation is good - learn how to reference it - hint, it's not as easy as googling it, you have to read and understand.
    * Follow the blogs of Adobe's AEM experts.  They have lots of tips and tricks. 
    * Test your code with the CRX/DE to see it work quickly

---

* Learn how to trick AEM to resetting itself:
    * Rename components (Trick Gourang Mehta showed me) when for some reason AEM wouldn't recognize a change.
    * Add random queries to the end of the url (page.html?2332) or similar
    * Restart the AEM (local) server
    * Check, doubleCheck, Recheck, aND CheckAgain the casing that you applied to sightly variables.
    * Shut the computer down, turn off all of the software, turn around three times while whistling dixie backwards. (This is a last resort - if you're here, likely there is something you're not seeing. Get someone to look over your shoulder and see if anything jumps out.)

---
* Maven will sometimes fail the build&deploy for no good reason. Try it again. This works for me quite a bit.
* Any work to a java file necessitates a rebuild and deploy.
* Compare against similar entries: are there any missing fields? Was this a copy paste gone wrong? I missed a sling:resourceType once that cost me 40 minutes. :(