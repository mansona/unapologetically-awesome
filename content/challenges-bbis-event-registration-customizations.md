---
title: 'Challenges: BBIS event registration customizations'
image: ''
authors:
  - melsumner_g2q1b4
date: 2014-09-01T11:37:00.000Z
tags:
  - my-bbis
  - javascript
---
I'm working through customizing event registration parts in BBIS 2.94. Here are the challenges:
<ol>
	<li>Attributes (platform-specific) must be used to display registration option preferences.</li>
	<li>Each attribute will show up for every single registration option, even if it doesn't apply to that particular registration option (I know, /facepalm). In this particular instance, I'm working on a golf tournament event with a dinner registration component- but I don't want to be asking a golfer what his dietary restrictions are, nor do I want to be asking a dinner registrant what their handicap is.</li>
	<li>JS must be triggered - still working through the exact details on this one.</li>
	<li>A lot of the elements don't have any classes or IDs</li>
</ol>
So far, I've worked out a way to hunt for the specific attribute label, identify the "parent" registration option, look for a specific string, and if that string exists, hide the row that contains the attribute I don't want.

Remaining challenge: understanding how to get this JavaScript to fire at the appropriate time- since the whole thing is on an asp.net platform, the event registration part itself is a wizard, and the panels are updated when you hit <em>previous</em> or <em>next</em>. On top of that, two different (and not very current) versions of jQuery are loaded at run time (although I thought that one would just override the other, but maybe I am misunderstanding jQuery somehow), and while there is also an ajax script manager in the compiled DLLs (yes, I decompiled all of the DLLs so I could understand it better) and various postback scripts firing- all with variables for specific situations.

Now, the input buttons do have IDs (a rare relief). I just have to try to figure out what combination of syntax to use to get the attention of events so I can make the JS work properly.

Update:

I've added button click functionality, although it's still conflicting with the pre-existing event registration form, so there's more to figure out.