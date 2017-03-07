---
id: 91
title: Is Mavericks Screwing Up Your PDFs?
date: 2013-11-07T18:12:01+00:00
author: jimmy
layout: post
guid: http://localhost:8888/2013/11/07/2013117is-mavericks-screwing-up-your-pdfs/
permalink: /2013/11/07/2013117is-mavericks-screwing-up-your-pdfs/
categories:
  - Writing
tags:
  - Apple
  - Mac
  - Mavericks
  - OSX
  - PDF
  - Safari
  - Tips
---
OSX Mavericks is here.  It has been for a few weeks.  And it's still broken in places.

 

When you click on a PDF in Safari, you used to get a preview in the browser of the thing you clicked on.  Now, many are getting a page full of what looks like gibberish.  It's not, it's the code that makes the PDF, but users should never see that.


There's a quick way to fix it. 

1. Open Terminal (it's in your utilities folder in the Applications folder) 

2. Type this: (Copy and paste, if you like) 

{% highlight applescript %}
defaults write com.apple.Safari WebKitOmitPDFSupport -bool NO
{% endhighlight %}

3. Restart Safari.  All is well. 

This is such a simple fix, I don't know why the bug is still here after three weeks, but until they fix it, this will allow you to read all those ill-gotten comic books. 

 