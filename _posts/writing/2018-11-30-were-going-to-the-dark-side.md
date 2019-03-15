---
title: Mojave Dark Mode in Safari
subtitle: Come to the dark side
layout: post
category: Writing
tags: [Safari, Dark Mode, CSS, Jekyll]
img: darkmode.jpg
tn: darkmode.jpg
---

If you haven't heard, macOS Mojave has a dark mode. A lot of apps support dark mode, and there are hooks in [upcoming version of Safari][1] that will also support dark mode. Now, Cocktails and Coffee will support dark mode as well
<!-- more -->

I'll be honest, I'm not a huge fan right now. It's a little buggy, not all apps support it, and on a non-Retina screen like my 2012 (ahem, _EARLY_ 2012) iMac, text looks a little fuzzy. I'm sure it looks great on a Retina screen, but I have a 2012 iMac and a 2011 MacBook Air, so I don't get that luxury.

That being said, I like to stay on top of trends, so I've implemented dark mode here on _Cocktails & Coffee_. It was a lot easier than I expected.  It took just 43 lines of CSS to make it happen, and that's probably more than you need to deal with.

Now, let's not fool ourselves. There are probably 4 people on the planet who will see this post in dark mode in 2018. You need to be on Mojave, and you need to be running Safari Technology Preview, you need to be in dark mode, and you need to be reading this blog. That's a pretty fucking tiny percentage of the world right now. But we persist.

### Here's How It Happens

You just need to add a CSS tag to your site's CSS file to let Safari know to ask the system what color scheme it's in. This is a simple `@media` CSS property:

`@media (prefers-color-scheme: dark) { ... }`

Then, you just add whatever CSS you need to edit between the curly brackets and if your system is in dark mode, your website will be in dark mode also. I didn't have to change too much to get a reasonable dark mode. Here is all of the CSS necessary to change this blog to dark:
	/\* Dark Mode \*/
	@media (prefers-color-scheme: dark) {
	  body {
	color: $dm-white;
	background-color: $dm-dark-gray;
	  }
	  .sidebar {
	background-color: $dm-light-gray;
	color: $dm-white;
	}
	  .about .author-name, .contact .contact-title, .post .read-source a {
	color: $dm-white;    
	}
	  .post {
	background-color: $dm-light-gray;
	border-color: $dm-light-gray;
	}  
	  .article-page {
	border-color: $dm-light-gray;
	} 
	  .page-cover-image {
	background-color: $dm-dark-gray;      
	}
	  .wrap-content {
	background-color: $dm-dark-gray;
	}   
	  .related-posts h4 {
	background-color: $green;
	color: $dm-white;
	}
	  .tags li a {
	color: $dm-white;
	border: none;
	background-color: $purple;
	}
	  .tag-count {
	color: $yellow;    
	}
	  .tag-list span a {
	color: $dm-white;    
	}
	  .highlighter-rouge {color: $yellow; background-color: $dm-dark-gray; border: 1px solid $yellow;}
	  }
	
	
	

### Using Variables
I use a Jekyll blog engine on Github, and I've set my site up to use a variables file.[^1]() If you're using Jekyll and not using variables, you're missing out. To make dark mode easy for me, I basically just stole macOS's colors. I used the dark gray and light gray background colors, and the slightly off-white text color from the system to make my site look natural in dark mode. Because I use a variables file, I just set up a few new colors:

	/\*  Dark Mode Theme Colors \*/
	$dm-dark-gray : #292a2e;
	$dm-light-gray : #2e2f33;
	$dm-white: #dddddd;
	

and that was it. When I added the CSS rules for dark mode, I used these three new colors, along with the original color variables, and made a passable dark mode that took me less than a half an hour to implement.  The reason I use a variables file is: If I ever want to change my color scheme, I edit one variables file, and all the instances change. For example, if I want to change my dark gray color, I just edit the `$dm-dark-gray` hex value in the variables file, and everywhere the color is used, it gets updated.

### If You Want To Get Fancy With Scroll Bars
You can also pretty easily change the scroll bar colors when going to dark mode. Just add these CSS properties to your dark mode CSS
	
	::-webkit-scrollbar {
	width: 10px;
	}
	
	::-webkit-scrollbar-track {
	background: $dm-dark-gray; 
	}
	 
	::-webkit-scrollbar-thumb {
	background: $dm-white; 
	}
	
	::-webkit-scrollbar-thumb:hover {
	background: $dm-white; 
	}
	

Again, using variables means that if I ever decide to change my page's `dm-dark-gray` background color, the scroll bar background will change with it.

Fancy.

Finally, here's how it looks when we go to the dark side:[^1]

<img src="https://www.cocktailsandcoffee.com/assets/img/post/darkmode.gif" align="center" width="75%">

---- 

[^1]:	Yes, I know it's not perfect, but it's pretty damn good for a few minutes work.

[1]:	https://developer.apple.com/safari/technology-preview/
