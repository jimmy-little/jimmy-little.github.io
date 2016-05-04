---

title: Mavericks and TextExpander
date: 2013-10-24T19:54:05+00:00
author: jimmy
layout: post
categories:
  - Writing
image:
 feature:   
tags:
  - Apple
  - Mavericks
  - OSX
  - TextExpander
  
subtitle: "Sometimes, security is hard.  Not this time"  
---

![Accessibility Settings](https://s3-us-west-2.amazonaws.com/www.jimmylittle.com/post-images/SysPrefAccSettings.png)

I love me some Text Expander.

When I upgraded to Mavericks, it stopped working.  Here's why: 

Mavericks has some fancy new security features that make it a bit harder for apps to control your computer.  This is inconvenient for exactly 10 seconds.  

**Here's how to fix it:**

 1.  Open System Preferences

 2. Click on "Security and Privacy"  and choose the "Privacy" tab. 

 3. Click the lock in the lower left and enter your password

 4. Choose "Accessibility" in the sidebar

 5. Check any apps you would like to allow to control your computer. 

That's it.  Text Expander (as well as apps like Moom, screen sharing apps, and apps that simulate keyboard and mouse inputs) use Accessibility features in OSX to work, and you now need to explicitly allow them to control your machine.  This is not a bad thing.  While you're in the Security and Privacy section, check out what other apps are using OSX features.  I found out 11 different apps are using my Contacts.