---
title: 'A11y: An accessibility guide for Ember developers'
image: ''
authors:
  - melsumner_g2q1b4
date: 2017-05-03T22:28:12.000Z
tags:
  - accessibility
---
I've been writing code for 20 years now, and that time has mostly taught me that the internet is filled with pedantic assholes who will always tell me twenty-five ways I am wrong, and these individuals are historically incapable of critical thought and cannot comprehend anything not explicitly spelled out in painful detail. This, along with my painful awareness that I liberally misuse commas, has historically made me shy away from writing things on the internet.

However, I recently read a book called "Calculus Made Easy." This book (published in 1914), with its simple speech and frequent use of the word "fool," has inspired me to just be myself and share my knowledge. I will, in general, give you (the reader) the benefit of the doubt and assume that you are capable enough to infer the intended context from my writing.

So let us begin.

This will be the first in a series of guides for practical implementation of accessibility. The primary focus is developers working with Ember whose applications typically live in the enterprise/corporate space, develop in a Windows environment, and whose applications are subject to US laws and regulations. Why? Because I am an Ember developer whose applications typically live in an enterprise/corporate space, I develop on Windows machines and my applications are subject to US laws and regulations. I will refer to this context as The Reason Why™ so I don't have to keep typing it out each time.
<h2><strong>Getting started</strong></h2>
<h3><span style="text-decoration: underline;"><strong>The Technology</strong></span></h3>
There are three main combinations of browsers and assistive technology (AT):
<ol>
 	<li>IE + JAWS (Windows)</li>
 	<li>Firefox + NVDA (Windows)</li>
 	<li>Safari + VoiceOver (iOS)</li>
</ol>
For the purposes of this series, I will primarily focus on Firefox + NVDA. If I still maintain interest and energy over time, I will go back through and add the various notes and caveats for the others, but the TL;DR is this:
<ol>
 	<li>Both Firefox and NVDA are free to use, &amp; function on a Windows machine.</li>
 	<li>IE + JAWS: JAWS costs a considerable amount, and for good reason: it's fantastic. Definitely the luxury vehicle.</li>
 	<li>Safari + VoiceOver: Safari is typically behind in browser development (at least it is right NOW), and EC developer typically does not have the luxury of developing in this environment anyway.</li>
 	<li>There is also Chrome + Chrome Vox but at the time of this writing, Vox is terribad and useless, comparatively. Evaluate it at a later date.</li>
</ol>
<h3><span style="text-decoration: underline;"><strong>Reference Materials</strong></span></h3>
The WAI-ARIA group is doing a good job of making sure the reference materials you need to succeed are online. Here is a list of references to keep handy:
<ol>
 	<li>The WCAG 2.0 Guidelines: <a href="https://www.w3.org/TR/WCAG20/">https://www.w3.org/TR/WCAG20/</a></li>
 	<li>The "How to Meet WCAG 2.0" guidelines <a href="https://www.w3.org/WAI/WCAG20/quickref/">https://www.w3.org/WAI/WCAG20/quickref/</a></li>
 	<li>WAI-ARIA Authoring Practices: <a href="https://www.w3.org/TR/wai-aria-practices-1.1/">https://www.w3.org/TR/wai-aria-practices-1.1/</a></li>
</ol>
And by "references to keep handy," I mean, "no seriously, bookmark these, you will use them a lot when you are writing accessible code."

The gist of it is this: the WCAG 2.0 Guidelines are what the US Justice Department has decided the rules will be, until they get around to writing the rules (commentary withheld). Here's what you need to know:
<ol>
 	<li>There are three levels: A, AA, and AAA.</li>
 	<li>Each level includes the level below it. So A is the lowest level of accessibility. AA is the next level and includes the rules in A. AAA is the most stringent and includes both A and AA rules.</li>
 	<li>If you are including accessibility in your application and The Reason Why™ applies, you will probably be aiming for AA conformance.</li>
</ol>
<h3><span style="text-decoration: underline;"><strong>Ember Support</strong></span></h3>
<ol>
 	<li>Install some addons (because, obviously):
<ul>
 	<li>ember-a11y-testing</li>
 	<li>ember-cli-template-lint</li>
 	<li>ember-a11y is pretty cool too, but you'll need to evaluate it to see if it will meet your needs.</li>
</ul>
</li>
 	<li>Slack support - Join the #topic-a11y channel in the Ember Slack chat.</li>
 	<li>And, once you figure it out, why not join in the ember-a11y project too? <a href="https://github.com/ember-a11y">https://github.com/ember-a11y</a></li>
</ol>
&nbsp;

Okay, this will probably be enough to get started. So go start.

<p role="complementary"><em><small>Up Next: <a href="http://blog.melsumner.com/accessibility/understanding-structure-landmarks/">Understanding Structure: Landmarks</a></small></em></p>