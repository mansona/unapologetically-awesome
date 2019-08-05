---
title: CSS Grid - Use Case
image: ''
authors:
  - melsumner_g2q1b4
date: 2017-02-22T19:57:52.000Z
tags:
  - my-css3
---
[caption id="attachment_519" align="aligncenter" width="1024"]<img class="size-large wp-image-519" src="http://www.melsumner.com/blog/wp-content/uploads/2017/02/bryan-colosky-168816-unsplash-1024x681.jpg" alt="a closeup of a building that looks like a giant grid" width="1024" height="681" /> Photo by Bryan Colosky on Unsplash[/caption]

I'm looking forward to CSS Grid for a lot of reasons.

At first, I admit that I found them really confusing and even decided that they will really only be useful for the kind of sites that I don't get to work on. I'm an enterprise application developer, living in the land where 70% of my users are on IE, and even just using Flexbox is considered revolutionary.

But there are some things that I think will really be made easier with Grid, even here in enterprise land. Flexbox is intended for uses where even spacing is desired in one dimension - either horizontal or vertical. Grid, however, is intended to alleviate even spacing for both horizontal and vertical use. Exciting, right? I don't know about you, but I get chills just thinking about it. Even if it doesn't excite you to the point of goosebumps, it still should intrigue you.

Here is a specific, real-world use case that I am dealing with in a current project:

I have a task list in a sidebar, one that is divided up into three tabs.
<ul>
 	<li>the tabs are spaced evenly across the width of the side bar</li>
 	<li>the application is available in many different languages, which means I can't always predict the width of the words. Nordic Languages, for example, can have really long words. Russian letters can take up more width than an English "m" or "w".</li>
</ul>
This means that I can have a set of tabs look very different, depending on the language.

[caption id="attachment_315" align="alignleft" width="358"]<img class="wp-image-315 size-full" src="http://melsumner.com/blog/wp-content/uploads/2018/03/tabs-good.jpeg" width="358" height="408" /> HAPPY PATH: In this screenshot, you can see that I have enough width and the text fits nicely.[/caption]

[caption id="attachment_314" align="alignleft" width="291"]<img class="wp-image-314 " src="http://melsumner.com/blog/wp-content/uploads/2018/03/tabs-bad.jpeg" width="291" height="403" /> UNHAPPY PATH: In this screenshot however, you can see that if a word wraps, then I have visual ugliness because the heights don't match.[/caption]

<div style="width: 100%; display: block; clear: both;"></div>
<div style="width: 100%; display: block; clear: both;">This is one area where design &amp; development doesn't need to be so complex!</div>
I know that there are current methods to solve this problem- a bit of JavaScript, some CSS magic, etc. But these current methods are verbose and add a level of irritating complexity to managing CSS in a large project.

Grid, however, will solve this problem.

I'll work to get a code sample for how this would be solved with CSS Grid; in the meantime, how about checking out <a href="https://rachelandrew.co.uk">Rachel Andrews'</a> or <a href="http://jensimmons.com/">Jen Simmons'</a> excellent tutorials and talks on the subject?