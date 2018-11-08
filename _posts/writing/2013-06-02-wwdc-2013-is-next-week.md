---

title: WWDC 2013 is Next Week
date: 2013-06-02T15:28:06+00:00
author: jimmy
layout: post
category: Writing
tags:
  - Apple
  - iOS
  - OSX
  - Rumors
  - WWDC

subtitle: Big changes are rumored.
  
---

<!-- more -->  

A lot of Apple bloggers are predicting major changes for iPhone and iPad in iOS 7. I am pretty happy with my iOS stuff, and understand that just because Scott Forstall is gone, it doesn't mean iOS is turning into Android. People are talking about flat design with less textures, more widgets, service toggles, and a bunch of other little stuff.

I would rather see some fundamental nerdly improvements that make the experience better. I am not an Apple blogger. I don't even consider myself a blogger. But, I use Apple stuff daily and know a bit about programming, so here is what I'd like to see, even if we keep the green felt in Game Center.

### Fix iCloud

First, let me say I use iCloud a lot. I use Safari's Cloud Tabs to open a web site on my iPad after walking away from my iMac. I use it to sync Pages and Numbers documents, I use it for text files between my [Byword](http://bywordapp.com) instances, and settings for a ton of apps that I use on iPhone and iPad. 

iCloud is great. When it works. Unfortunately, it doesn't always work. My beloved [Omni Group](http://www.omnigroup.com) apps choke on iCloud sync, because iCloud chokes on anything using Core Data. Individual documents work fine, but database centered apps can't rely on it. Omni Group has even started their own sync service to deal with this issue. Hopefully Apple can get their shit together with the iCloud. It's important.

And while you're at it, Apple, let's expand iCloud availability to vetted apps outside the App Store. Apps like [Hazel](http://www.noodlesoft.com/hazel.php) and [Moom](http://manytricks.com/moom/) are apps with TONS of settings that can't currently sync preference files because they are not in the App Store. 

### iCloud App

We are never going to see a real file system browser on iOS, and we shouldn't. There's really no reason for it.

What we should have is an iCloud Documents app. Assuming they fix the Core Data syncing issues, leave app-specific databases out of the app. Just give me an app that shows all the individual documents in my iCloud. I can save a PDF to iCloud on my Mac, but can't open it in a PDF app on my iPad. Let me see all the PDF's in iCloud, and let me choose where to open it. Let me see all the text files, and decide which app to edit them in. If I have a PDF on my iPad that I've edited in PDFPen, sent to GoodReader to upload to Box.net, now I have 3 copies of that PDF, one in each app's document bucket. That's ridiculous. If I edit a text document in ByWord, then open it in Elements, I now have two different text documents edited at different times. Wouldn't it be better for both of these apps to access the same text file? I know the sandboxing is important, but if I can manually send a text file between apps, why cant the OS know to send the text file to the app I want, then back to the iCloud bucket when I'm done? Isn't that the same thing?

### Siri Now

Google Now is awesome. It knows where you work and where you live. It reads your calendar and, if you religiously add accurate location information to appointments like I do, will alert you if you need to leave earlier because of traffic. It scans your email for travel info and adds your airline tickets to the list (on iOS, it would be in Passbook). If you search for `Red Sox Scores` a lot, it will just automatically add a scorecard to the list when there's a game on. It's smart. It's convenient. But it's also creepy.

Apple, on the other hand, could do all this without being creepy. Apple keeps your email private. They don't pepper it with ads. But they can (and do) still scan it for keywords. They know your iPhone location, but they don't broadcast it publicly, like Google Latitude does. (Yes, I know you CAN broadcast it on iOS using Latitude, FourSquare, Glympse or a ton of other ways, but it's not ON by default.) They know your address book. They have your calendar. They have maps. They can (and do) record what you search for in Safari. They keep all the creepy information Google does, they just don't use it. Yet. I think Apple can do the same predictive stuff Google Now does, but without giving all of your personal information to Google, which is an advertising company, not a services company. And make it an option to have Siri Now be my lock screen.

### Contacts and Mail on iOS

I'm lumping these together for one small thing: Let me type the name of a group into a To: field to email everyone in the group. It works on the desktop versions, there's no reason it can't work on iPhone or iPad. It's just silly to tap each member of a group to add the group to an email To: field.

### Require URL Schemes 

Some apps, like OmniFocus and [Drafts](http://agiletortoise.com/drafts/), use complicated [URL Schemes](http://wiki.akosma.com/IPhone_URL_Schemes) to share information between apps. Some apps, including several built-in apps, use them as well. Just type `tel:1-212-555-1212` into the URL bar in Safari, and it will dial the phone. also works with `sms:1-212-555-1212`. If you're a [1 Password](https://agilebits.com/onepassword) user, you can just put `op` in front of a standard web address, and it will open the page in a secure 1Password browser and input your credentials. Hundreds of apps use these schemes. All of them should. Even simple schemes like allowing my remote control app to open the TiVo app by creating a button with a `tivo://` is terribly useful. Everyone should do this.

I'm sure there's more, but we still have a few days until WWDC.  

---

**Update:**

After thinking about the iCloud "bucket of documents" idea that I talked about, I read a <a href="http://www.macrumors.com/2013/06/02/ios-7-may-include-airdrop-wireless-file-sharing-capabilities/" target="_blank">rumor</a> that Apple may be adding AirDrop to iOS 7.  Dropping a generic file on my AirDrop icon on my desktop and having the file show up in my iCloud document bucket would be pretty handy for one-off files.  Even better, AirDropping a file between iOS devices would save a lot of e-mailing and DropBoxing for sending simple pictures or documents.

Also, with the iOS-ification of the OSX, isn't it time for Apple to release a Maps app for the Mac, or at least a web interface?  Maps has it's issues, to be sure, but more users can only make it better.