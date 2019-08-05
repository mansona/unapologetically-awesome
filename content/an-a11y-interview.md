---
title: An A11y Interview
image: ''
authors:
  - melsumner_g2q1b4
date: 2017-03-02T17:16:18.000Z
tags:
  - accessibility
---
These are the accessibility-related questions I would ask at an interview*:
<ol>
 	<li>Let's talk about accessibility. Do you know what that is?
<strong>Looking for:</strong> General awareness. I've been given answers like, "that means your site will work in every browser," which surprised me the first time I heard it.</li>
 	<li>Where does accessibility fit into the site/app(product) process?
<strong>Looking for: </strong>from the very start! It should consistently be an integral part of the process.</li>
 	<li>Are you aware of any laws that effect whether or not a product has to be accessible?
<strong>Looking for:</strong> discussion should be specific for the area of the globe, should include references to WCAG 2.0 A/AA/AAA</li>
 	<li>What types of users would use assistive technology(AT), or what are some of the common use cases for accessible products?
<strong>Looking for:</strong> the basics, at the least. Awareness regarding various levels of sight, hearing, physical abilities, and cognitive abilities. Would prefer extended awareness to include types of color-blindness, vestibular disorders, and seizure awareness.</li>
 	<li>If you were tasked with making sure that the code you developed was accessible, how would you approach it?
<strong>Looking for:</strong> references to the W3C <a href="https://w3c.github.io/aria/aria/aria.html">WAI-ARIA spec</a>. Bonus points if they mention the a11y Slack chat, and <a href="http://w3c.github.io/aria-practices/">WAI-ARIA authoring practices</a>.</li>
 	<li>How important is valid HTML?
<strong>Looking for:</strong> <a href="http://w3c.github.io/aria-in-html/#rule1">"Essential."</a> Would like to hear discussion about native functionality available in the browser when semantic elements are used.</li>
 	<li>What is tabindex? (or, talk about tabindex and keyboard navigation, to gauge their knowledge level)
<strong>Looking for:</strong> awareness that tabindex is native on interactive elements, how tabindex -1 works, how arrow keys typically work or what needs to be programmed in. Bonus if they know more and can talk about how to program custom keyboard interactions and know the details of that.</li>
 	<li>How would you visually hide an element on a page in a way that made it still visible to users with assistive technology?
<strong>Looking for:</strong> thought process beyond <a href="https://css-tricks.com/places-its-tempting-to-use-display-none-but-dont/">CSS's display: none</a> or visibility: hidden.</li>
 	<li>Have you ever personally used assistive technology like a screen reader? If so, can you tell me about your experience with that?
<strong>Looking for:</strong> Honesty! Personally, the first time I used a screen reader, I hated it. It felt really claustrophobic (I have noise-related quirks. As in, I hate tons of noise). But it's increased my empathy and my design/development skills, and I can't imagine ever developing a product without one now.</li>
 	<li>What browser(s) do you use while developing(to include testing)?
<strong>Looking for:</strong> expanded awareness beyond just Chrome developer tools. Would like to hear Chrome, FF, and IE mentioned at the least.</li>
 	<li>Are you aware of the assistive technology platforms that exist for that(those) browser(s)? If so, which ones?
<strong>Looking for:</strong> Awareness that there are different browser/AT combinations. Bonus if they are already aware of the common combinations like Firefox and NVDA, IE and JAWS, and Safari and VoiceOver.</li>
 	<li>What are some methods you could use to ensure that a color blind person could still use the product in the way it was designed?
<strong>Looking for:</strong> thought process to include "not just color, but additional methods that indicate purpose"</li>
 	<li>Are you aware of the accessibility efforts in Ember (or your environment-specific area) that already exist?
<strong>Looking for:</strong> awareness of <a href="https://github.com/dequelabs/axe-core">axe-core</a>, <a href="https://github.com/ember-a11y">ember-a11y</a> (or <a href="https://docs.angularjs.org/guide/accessibility">ng-Aria</a> if using Angular), etc.</li>
 	<li>What would you do to make a video accessible?
<strong>Looking for:</strong> add captions, provide a description, don't autoplay.</li>
</ol>
Other items that I'd like to hear talked about:
<ol>
 	<li>some understanding to differentiate among the ideas of ADA compliance, <a href="https://www.w3.org/TR/WCAG20/">WCAG 2.0 conformance</a>, and full accessibility</li>
 	<li>comfortably talking about building a <a href="https://modelviewculture.com/pieces/building-accessibility-culture">culture of accessibility</a>.</li>
 	<li>some of the self-training they've done - <a href="https://www.youtube.com/watch?v=gf_BrfCZT7c">youTube</a> videos, <a href="https://egghead.io/lessons/tools-building-forms-with-accessibility-in-mind">egghead.io</a> (or similar) course, local #A11y Meetups, <a href="https://shop.smashingmagazine.com/products/inclusive-design-patterns">books</a>, etc.</li>
</ol>
This list is subject to change; I will probably refine it over time and with your lovely suggestions! But I think this would be a good place to start.

<small><em>
*I use Ember to help build enterprise applications that have a legal requirement to be WCAG 2.0 AA conformant.</em></small>