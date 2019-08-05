---
title: Application vs Document Roles
image: ''
authors:
  - melsumner_g2q1b4
date: 2017-05-24T01:12:12.000Z
tags:
  - accessibility
---
<em>This is a post in this series (A11y: An Accessibility Guide For Ember Developers). Here's a link the first post, <a href="http://blog.melsumner.com/accessibility/a11y-accessibility-guide-ember-developers/">Getting Started</a>, and the second post, <a href="http://blog.melsumner.com/accessibility/understanding-structure-landmarks/">Understanding Structure: Landmarks</a>. At least reading the first post will be important to understanding the target audience, and some of the shorthand terminology I've implemented for the purpose of this series.</em>

<hr />

[caption id="attachment_509" align="aligncenter" width="1024"]<img class="size-large wp-image-509" src="http://www.melsumner.com/blog/wp-content/uploads/2017/05/rawpixel-com-594846-unsplash-1024x709.jpg" alt="a closeup of a man's hand on his laptop keyboard, with an application on the screen." width="1024" height="709" /> Photo by rawpixel.com on Unsplash[/caption]

When I first read the specification about landmark roles, they seemed rather obvious to me. Especially the application landmark role. "Oh that's easy, I build apps, I'll use that." I couldn't have been more wrong, though. When to use, or not use, the application role seems to be a thing that can really trip developers up- especially JS framework developers. Especially if The Reasons Why™ apply. A lot of us have some variation of "Application Developer" in our job title, and that's exactly what we do. We just happen to make them available via browser.

As far as assistive technology is concerned, however, "application" does not mean what you think it means. Okay maybe you are smarter than I am, and it will totally make sense to you from the start, but it was an excuse to use a Princess Bride quote and ALWAYS DO THAT.

I make no apologies for that digression.

Anyway.  <strong>The TL;DR is this: don't use role="application" because it doesn't apply to you.</strong> Probably.

Wanna know why? Let's look.
<h2>So, Basically...*</h2>
Use role="application" when you want to control ALL of the keyboard navigation. I really mean "all" here. You're telling the browser, "hey I got this." The screen reader will STOP intercepting keystrokes. This is typically bad.

It is a pretty silly thing to do, because you now have to implement all of the things that the browser AND assistive technologies (AT) typically give you for free.  This, again, is why we use native HTML5 elements! Interactive elements....yes! you remembered! They have built-in tabindex.
<h2>Focus. Browse. Focus. Browse.</h2>
NVDA** has a focus mode and a browse mode. Let's go through that.
<ol>
 	<li>web pages are in browse mode by default. When the user enters something like an input field (interactive element!), NVDA automatically switches to focus mode.</li>
 	<li>focus mode allows the user to quickly navigate to all of the interactive elements on the page using the arrow keys, instead of their default behavior (scrolling up and down the page).</li>
 	<li>Keyboard shortcut: [NVDA + SPACE] toggles between modes.</li>
 	<li>Pro-tip: For easier development, go to NVDA &gt; Preferences &gt; Browser Mode and un-check the box that says "audio indication of focus and browse modes". Here's a screenshot:
<img class="alignnone size-medium wp-image-413" src="http://melsumner.com/blog/wp-content/uploads/2018/03/screenshot_nvda-browse-mode-300x294.jpg" alt="nvda browse mode menu screenshot" width="300" height="294" />
You'll then see "focus mode" and "browse mode" in the speech viewer, like this:
<img class="alignnone size-full wp-image-414" src="http://melsumner.com/blog/wp-content/uploads/2018/03/screenshot_nvda-browse-focus-speech-viewer.jpg" alt="screenshot of NVDA speech viewer showing browse and focus mode toggle" width="300" height="300" /></li>
</ol>
<h2>But I really gotta use it!</h2>
In the incredibly rare case that you DO need to use role="application", here are the rules:
<ol>
 	<li>Do not use it on the body element (I'm pretty sure Ember won't let you do that anyway, but maybe that's just something I haven't tried to do yet)</li>
 	<li>Use it directly on the component's container.</li>
 	<li> If there are nested components that would benefit from the native browser or AT browsing functionality, put role="document" on that inner component.</li>
 	<li>Yes. You can nest landmark roles. You could really have a <a href="https://www.youtube.com/watch?v=EmLHOGT0v4c&amp;list=RDEmLHOGT0v4c">ridiculous Russian doll situation</a>. But please don't.</li>
</ol>
<h2>No, you really probably don't.</h2>
I think of it this way: recognizing that my application is really probably 99.99% considered a document for accessibility reasons, is a fantastic way to keep me humble.

Here's some further reading for the unconvinced:
<ul>
 	<li><a href="https://www.w3.org/TR/wai-aria/roles#application">The WAI-ARIA specification: Application (role)</a></li>
 	<li>Using ARIA: 2.11: <a href="http://w3c.github.io/using-aria/#using-application">Using ARIA role=application</a></li>
 	<li>Article: <a href="https://www.marcozehe.de/2012/02/06/if-you-use-the-wai-aria-role-application-please-do-so-wisely/">If you use the WAI-ARIA role "application", please do so wisely!</a> by Marco</li>
</ul>
&nbsp;

&nbsp;

<hr />

<small>
<em>* saying "so, basically" is one of my pet peeves and guarantees that I will start to be cranky if you use that around me a lot, because in my experience the people who use that phrase are total self-absorbed jerks who love to hear themselves talk but have never finished a damn thought properly or cohesively in their lives but somehow they are the better developer than I am. Not that I am traumatized or anything, as I prove by my ironic use of the phrase. So ha! Or something.</em></small>

** remember to scan your AT of choice to see how it does something similar.

<hr />

Up next: <a href="http://blog.melsumner.com/accessibility/theres-an-addon-for-that/">There's an addon for that.</a>