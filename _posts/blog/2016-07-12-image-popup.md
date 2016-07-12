---
title: "Image Popup Test"
date: 2016-07-12
layout: post
subtitle: "Let's play with CSS"
category: Writing
tags: [TEST]
image:
  feature: https://s3-us-west-2.amazonaws.com/www.jimmylittle.com/post-images/iMacUpgrade/Image.jpeg

---

{% capture images %}
	https://s3-us-west-2.amazonaws.com/www.jimmylittle.com/post-images/iMacUpgrade/Thegoods.jpeg
{% endcapture %}
{% include gallery images=images caption="This is the good stuff" cols=1 %}
{% capture images %}	
	http://upload.wikimedia.org/wikipedia/en/2/24/Lenna.png
	https://s3-us-west-2.amazonaws.com/www.jimmylittle.com/post-images/iMacUpgrade/Dismantled.jpeg
{% endcapture %}
{% include gallery images=images caption="Test images" cols=2 %}

