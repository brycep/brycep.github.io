---
layout: post
title: "Using CSS Animations"
date: 2014-12-08 21:35:54 -0800
comments: true
categories: [CSS, UI]
---
One of the reasons I started this blog is to have a platform to experiment with UI design.
Octopress is amazingly flexible.  You can change almost every aspect of it, and even if there's something the
author hadn't thought of, you have all the source, so you can implement whatever you want.

After playing around with the side, I decided I wanted to try to use CSS to animate the sidebar expanding and
collapsing.  CSS transitions are part of the CSS3 set of specifications.  They're a remarkably simple yet powerful
way to put simple animations into your static HTML pages.

When I dug into the Octopress HTML, I found the sidebar expands and contracts when the JavaScript code toggles a
CSS class called "collapse-sidebar".  The "collapse-sidebar" class moves the right margin of the sidebar back and forth
from a negative value to 0.  By specifying a CSS transition on the right margin, you can make the browser animate
when it applies the new class.

The CSS transition property has 4 parts to it:

    transition: <property> <duration> <transition style> <delay>;

In my case, I want "margin-right" to animate for .7 of a second.

Adding the following code to the #content class makes any change to the margin-right property become animated

    #content {
      transition: margin-right 0.7s;
    }

Give it a try.  Click on the arrows at the top of the sidebar on this page and watch the sidebar slide in and out.

Find more information about CSS3 transitions at the link below.  They're a lot of fun to play around with!

(https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Using_CSS_transitions)
