---
layout: post
title: "Beginner's Guide to Classes in JavaScript"
description: Demo post displaying the various ways of highlighting code in Markdown.
modified: {}
tags: 
  - sample post
  - code
  - highlighting
image: 
  feature: "abstract-10.jpg"
  credit: dargadgetz
  creditlink: "http://www.dargadgetz.com/ios-7-abstract-wallpaper-pack-for-iphone-5-and-ipod-touch-retina/"
published: true
---



So what are Classes in JavaScript? And why do we have them? What is their usage? 

First, a prerequisite for understanding this blog post is a knowledge of how Objects in JavaScript works. I will spend a couple of paragraphs here for anyone who doesn't know. 

Objects can be seen as a container. A data container. Much like how you would have a plastic container for you socks, underwear, etc. And they look something like this :

{% highlight javascript %}
var shelf = {
	socks : 5,
    underwear : 3
};
{% endhighlight %}

And you can assign new "shelves" by the dot notation :

{% highlight javascript %}
shelf.jeans = 10;

//now the 'shelf' object looks like :
shelf = {
	socks : 5,
    underwear : 3,
    jeans : 10
};
{% endhighlight %}

So what are classes then? And what are they used for? 

First, I will say upfront that Classes are a modified version of an Object. 

What do I mean? 

Let's say that you are running a supermarket in JavaScript. That's right, in JavaScript. Let your imagination go wild with this one. 

And you need 10 cash registers. As we all know, cash registers have multiples of functions some of which are : adding up all the items, processing payment, and opening the cash drawer. 

How would I build 10 of these in JavaScript? 

I guess I can do something like :

{% highlight javascript %}
var register = {
	opendrawer : function() { ... },
    closedrawer : function() { ... },
    money : 50
}

var register1 = {
	opendrawer : function() { ... },
    closedrawer : function() { ... },
    money : 60
}

var register2 = {
	opendrawer : function() { ... },
    closedrawer : function() { ... },
    money : 15
}
{% endhighlight %}

And on down the line. That could certainly work. But it isn't the most efficient. If computers are not going to be efficient for us, why did we even create them in the first place? ;)

So that's where Classes come in.

Classes let us build right-out-of-the-factory-line cash registers. 

Take a look at this code here:

{% highlight javascript %} 
var registerMaker = function() {
	var register = {};
    register.opendrawer = function() {...};
    register.closedrawer = function() {...};
    return register; 
};
{% endhighlight %} 