---

title: Using Keyboard Maestro for Print Layout in Sketchup
date: 2014-05-09
author: jimmy
layout: post
categories:
  - Writing
tags:
  - Automation
  - Keyboard Maestro
  - Mac
  - SketchUp
  - Tips
---
In my "real job" as a carpenter, I use <a target="_blank" href="http://www.sketchup.com">SketchUp</a> pretty heavily to do quick and dirty drawings and 3D models to visualize complex pieces. 

[![Prelim Sketch](https://s3-us-west-2.amazonaws.com/www.jimmylittle.com/post-images/sketchup-keyboard-maestro/prelim.png)](https://s3-us-west-2.amazonaws.com/www.jimmylittle.com/post-images/sketchup-keyboard-maestro/prelim.png)This is a preliminary sketch, so no judgey-wudgy there, Picasso.

  I'm currently working on a playroom, and need a [Tansu](http://en.wikipedia.org/wiki/Tansu)-inspired stair-step storage unit.  That's not the point. I draw it up in Sketchup and get something like the picture above.


  The problem is, there are pretty terrible print layout options in SketchUp.  You basically can set a scale, then print what's in the window.  So, I always have to resize the window to be about the size of a sheet of paper in order to get the right proportions.  

![pitiful options](https://s3-us-west-2.amazonaws.com/www.jimmylittle.com/post-images/sketchup-keyboard-maestro/printsetup.PNG)



What do I do when I have to do something more than once or twice?  

**Automate it!**

 

For this, I use the ever-more-useful-to-me <a target="_blank" href="http://keyboardmaestro.com">Keyboard Maestro</a>.  It's a Mac app that can do a metric crap load of stuff.  It does keyboard shortcuts, window management, it can run AppleScripts, run multiple clipboards, and more.  Actions are triggered by hotkeys, time, wifi connection, USB connect/disconnect, or just about anything else you can do to a computer.

For this fun bit, open the Keyboard Maestro editor and follow these steps:

  1. Make a new macro by clicking the little "+" at the bottom.  
  2. Choose "**Triggered by&#8230;**" Choose **This hot key**
  3. Pick a hot key.  I use **^⌥⌘L**.  As you can see by the screenshot, I smash those three down for all my window actions.
  4. Click in the dotted box that says "**No Action**" to get the action sheet.
  5. Drag "**Manipulate a Window**" onto the No Action Box
  6. In the "**Scale Size By**" drop down, choose **Resize To.**
  7. Fill in 1190&#215;1050.  It seems out of proportion for an 11&#8243; x 8-½" box, but this includes the menubar and title bar.  The actual drawing area will be just about letter-sized. [1]
  8. To limit it to SketchUp, choose SketchUp from the "in" drop down at the bottom.  If SketchUp is running, it will appear in the list, if not choose from the "Other" menu.
  9. That's it.  It should look a little like this:

[![Keyboard Maestro settings](https://s3-us-west-2.amazonaws.com/www.jimmylittle.com/post-images/sketchup-keyboard-maestro/KMsettings.png)](https://s3-us-west-2.amazonaws.com/www.jimmylittle.com/post-images/sketchup-keyboard-maestro/KMsettings.png)

Now, smashing ^⌥⌘L resizes the Sketchup window to letter-size so I can arrange the drawing appropriately and print.

[![That's better](https://s3-us-west-2.amazonaws.com/www.jimmylittle.com/post-images/sketchup-keyboard-maestro/FinalSketchupPrint.png)](https://s3-us-west-2.amazonaws.com/www.jimmylittle.com/post-images/sketchup-keyboard-maestro/FinalSketchupPrint.png)

[1] Yes, this is for US letter sized paper.  If you're using A4 or legal or whatever, adjust the proportions appropriately.  Also, the 1190&#215;1050 is nice on my 27&#8243; iMac, you may need to scale it down for your display.