---
title: Saving Instagram Posts to the Blog
subtitle: Just in case Facebook goes away
layout: post
category: Writing
tags: [Instagram, Shortcuts, iOS, Automation]
img: instagram-shortcut-to-blog.jpg
tn: instagram-shortcut-to-blog.jpg
date: 2018-11-
---

I'm not a super heavy [Instagram][insta] user, but I do occasionally post. When I do, I like to save that post to this blog. Why? Maybe because I'm not a huge Facebook fan and contemplate deleting all my Facebook-owned data weekly. Maybe because I like to see where my Instagram posts fit in with all my other random thoughts. Maybe a little of both.

I struggled for a while to try to figure out how to do this automatically, and I finally found the answer in the [Shortcuts App for iOS][shortcuts].

I have two main requirements for my Instagram Scraping Machine.
  1. It must pull the comment and picture and save it outside of the Instagram ecosystem. If Instagram goes away, I'll still have my images.
  2. It must also embed the original Instagram post in my blog post. As long as Instagram is around, this will allow the "native" view with all the comments and likes and whatnot.

There are a lot of things happening in this Shortcut, so buckle up. Here we go. If you want to follow along, [grab the shortcut here][icloudlink]. You'll also need my [Github Credentials][icloudlink2] sub-Shortcut if you're planning on storing this in Github, which I do for my Jekyll-powered site. That's a whole other story.

Create the shortcut, and set it to "Show in Share Sheet" and accept Safari Web Pages and URLs. This will prevent it from showing up in _every_ share sheet, but it will appear when you share a URL.

First action is to save the URL to a variable. I cleverly name it `url`.

Next, we add a couple of `Replace Text` actions that remove the URL part of the URL. The first removes `https://www.instagram.com/p/` and the second removes the trailing `/`. This leaves just the Instagram ID, which is saved as a variable. (Yes, I know Magic Variables are a thing, but I find it quicker to just create a variable than to rename a Magic Variable.)

Then, we send the `url` variable into the open Instagram API.

`https://api.instagram.com/oembed/?url=[your_url_variable]`

This pulls the embed code from Instagram. `Get Contents of URL` downloads the embed, which is partially JSON. Then, we `Get Dictionary from Input` and `Set Variable` as `apiDictionary` so we can call it back up a couple times.

To get the actual embed code, `Get Dictionary Value` of the `html` key. This value is saved as the `embedCode` variable. Then, we look through the embed code to find the date. There is only one date in the code, so we can pull that pretty easily using a regular expression.

`\d\d\d\d-\d\d-\d\d`

Save that as `date` variable. We'll use it in the YAML to set the blog post's date. I pull it from the Instagram API to make sure the date of the post matches the date of the Instagram, in case I don't run the Shortcut immediately.

Grab that `apiDictionary` variable again and get the value of `title`. This will be saved as the content of the blog post. Set a `comment` variable.

Then, we `Ask for Input` for the blog post title. I have it set to default to the title we pulled in the last step, but I usually change it. The titles on Instagram are sometimes too long. Type into the popup, and save it as a `title` variable.

Then, a couple `Replace Text` actions strip out spaces and punctuation, then `Change Case` to lowercase and save it as a URL `slug` variable.

`COPY REGEX INTO HERE`

Grab that trusty `apiDictionary` and pull the `thumbnail_url` key. This is the path to the thumbnail image of your Instagram post. It's not the full size image, but it's good enough for my purposes, which is a thumbnail image on the homepage of this blog.








[insta]: https://wwww.instagram.com/jimmylittle
[shortcuts]: addappstorelinkforshortcuts
[icloudlink]: geticloudicloudlink
[icloudlink2]: getotherlink
