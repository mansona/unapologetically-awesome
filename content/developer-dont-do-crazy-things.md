---
title: 'Developer, don''t do crazy things'
image: ''
authors:
  - melsumner_g2q1b4
date: 2014-10-09T14:51:33.000Z
tags:
  - security
---
I attended "SQL Saturday" in Raleigh last month. More of a wolf in sheep's clothing I suppose, since the conference was specifically for database administrators, something that was highlighted with a session called "Crazy things that developers do." I went, of course, because I like to make sure I'm not in the "developer who does crazy things" category.

First up, the predictable-yet-always-hilarious XKCD joke, "Exploits of a Mom":
<img class="img-responsive" src="http://imgs.xkcd.com/comics/exploits_of_a_mom.png" alt="" />

The speaker quoted a statistic that SQL injection attacks were up 69%. I don't really know where he got that number, and we all know that stats can be strategically manipulated to give you mostly whatever number you want, but still, 69% is higher than it should be. He demonstrated a site that he was able to hack in three steps- but really, it mostly made me sad that developers like that are out there. Because the way he was able to hack - really WAS a stupid developer thing to do.

Here are a few basics, which may help you avoid earning the "developer who does crazy things" title:

1. Please limit the number of characters on form inputs. No one needs 255 characters for their last name or first name or anything, really.

2. Always use the correct data type. Don't set it to <code>varchar</code> when it is really <code>int</code> or <code>datetime</code> or something else that explicitly matches the type of data you are asking the user to enter.

3. Never trust the user. I know, sounds mean. Cynical. I don't care, though. Sanitize inputs. Use query parametrization- the cheat sheet on OWASP.org can get you started: <a href="https://www.owasp.org/index.php/Query_Parameterization_Cheat_Sheet" target="_blank">https://www.owasp.org/index.php/Query_Parameterization_Cheat_Sheet</a>

4. Don't leave your database administer user as "root" or leaving your SA user/role on your server after you've set everything up. Check out what can be done with an "execute as" command. If it's the first time you've read it, don't worry- nightmares for weeks is an appropriate reaction.

5. Please set up a "read-only" role for your app that does just that- permits read only. This is good when you need to display data from your database, but you don't need anything else. Ideally- create a view for your data, and have your read-only user/role be what calls it up to display it. The point, really, is to minimize database permissions.

6. Use Client-side validation. Don't let the data get to the server to validate, because, obviously. HTML5 actually has a few additional bits to help with this and they are already built in. Use them! There are also things like escaping characters (even built in for WP, awesomely enough) and pattern matching. Give your inputs the appropriate amount of client-side validation.

7. You might have an awesome Systems Administrator (you do remember to regularly bring them cookies, right? RIGHT?) but you might be running your own show and wearing your Systems Administrator hat yourself. If you are, then regularly CHECK YOUR ERROR LOGS. Look for SA login attempts.

The thing is, the talk shouldn't have really been called "crazy things developers do." We all know this. It should have been "Lazy and irresponsible things developers do." The developer has a responsibility to make sure that basic safeguards are in place, and that's just part of what it means to be a developer.