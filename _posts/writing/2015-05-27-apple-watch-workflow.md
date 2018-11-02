---
layout: post

link: 

date: 2015-05-27

category:  Writing 

tags: [Apple Watch, Mac, Automation, Launch Center Pro, iOS, Dropbox, Hazel]

via: 
source: 

subtitle: Do more with that little computer on your wrist

title: Using Your Apple Watch To Trigger Your Screensaver

---


I sometimes work in a corporate-y office. I also tend to walk around a lot, and leaving your computer unlocked can be dangerous. Naturally, I have a workflow that will allow me to lock my computer from afar when I've wandered off. 

<!-- more -->  

There are a few nerdy tools needed, but you should have these anyway.

  * [Workflow](https://geo.itunes.apple.com/us/app/workflow-powerful-automation/id915249334?mt=8&uo=6&at=1001l3C5), an awesome iOS automation app
  * [Hazel](http://www.noodlesoft.com/hazel.php), a great automated organizer app for your Mac.
  * [Dropbox](https://db.tt/UfENov5).
  * and of course, an iPhone, Apple Watch and a Mac.

First thing you will want to do is put a text file in an accessible folder on your Dropbox. I use [Launch Center Pro](https://geo.itunes.apple.com/us/app/launch-center-pro/id532016360?mt=8&uo=6&at=1001l3C5) for a lot of other automation, so I put the file in _Dropbox/Apps/LCP_ because I'm already monitoring that folder with Hazel. More on that in a bit. Name the file something creative, like **sleep.txt**.

Now go to your System Preferences and open Hazel. In the left pane, click the **"+"** button and add the folder your text file is in (mine is in _/Apps/LCP_, but yours can be anywhere on your Dropbox.) Then, in the right pane, click the other **"+"** button to add a new rule.

  * Name it something recognizable
  * If ALL of the following are met: 
      * Name IS sleep.txt
      * Date Least Modified IS IN THE LAST 1 minute
  * Do the following: 
      * Run AppleScript - embedded script
      


Then, paste in the following simple AppleScript, which starts the screensaver.

{% highlight applescript %}
	tell application "ScreenSaverEngine"
        activate
        end tell
{% endhighlight %}     


![Hazel Prefs](https://s3-us-west-2.amazonaws.com/www.jimmylittle.com/post-images/HazelPrefs.png)   


Great. What the hell just happened? You just told Hazel that if the **sleep.txt** file has changed in the last minute, then run this script that starts the screensaver. You can test this by just opening **sleep.txt** and typing a letter or two then saving. Once the save is complete, the Last Modified timecode changes to now, which is obviously in the last minute. So, the screensaver starts up. Pretty sweet. Now, to activate this from the Watch.

On your iPhone, fire up Workflow and create a new one. Make sure it's set up as an Apple Watch workflow. Choose an appropriate name and icon. Then build a simple two-step Workflow:


  * Text (can be anything, I use "Go to sleep")
  * Append to Dropbox File 
      * Mode: Append
      * File Path: /Apps/LCP/sleep.txt
      * Make New Line (optional, but I leave it on)
      
      
![Workflow Screenshot](https://s3-us-west-2.amazonaws.com/www.jimmylittle.com/post-images/WF-Sleep-Mac.PNG)      


Now, when you tap this Workflow from your Watch, a line of text is appended to the text file, which changes the modify date, which launches a screensaver. 

If you don't want to build it yourself, you can [download my Workflow here.](https://workflow.is/workflows/68cf1b5bc9864dc0882b5e39bf05583b) As an added bonus, you can also add this Workflow to your iPhone's home screen and run it from there, just select "Normal" in the workflow setup. The only limitation to this way of doing things is you can only trigger the screensaver once a minute.

Have fun with this. If you're using it, let me know on the [Twitter](http://www.twitter.com/jimmylittle)!