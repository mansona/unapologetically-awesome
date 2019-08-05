---
title: 'Understanding Structure: Landmarks'
image: ''
authors:
  - melsumner_g2q1b4
date: 2017-05-07T13:43:54.000Z
tags:
  - accessibility
---
[caption id="attachment_506" align="aligncenter" width="1024"]<img class="size-large wp-image-506" src="http://www.melsumner.com/blog/wp-content/uploads/2018/03/william-bout-103533-unsplash-1024x596.jpg" alt="a lighthouse juts out into the water, perched on the edge of a cluster of jagged rocks" width="1024" height="596" /> Photo by William Bout on Unsplash[/caption]

The structure of a page rendered to the browser is important. If you already understand this, and why, then ignore this next part, it's not for you. Maybe you don't think it's important because you've been putting everything into divs and spans and HEY THAT'S WORKED OUT OKAY MEL. If by "okay" you mean "it builds" then <em>technically</em> you're correct, given that limited definition, but it's still not okay. HTML is implicitly error-tolerant, which means it'll still work no matter what you do to it. That level of error tolerance doesn't mean HTML is <em>less</em> important, it means it's <em>different</em> important- and quite frankly, to consider it as <em>less</em> important makes you a jackass, even if I can empathize with why you might think that way.

HTML markup isn't meant to <em>make it work</em> in the same way our JS files make it work. HTML is meant to give the content semantic meaning. This matters to assistive technology. Assistive technology (AT), like a screen reader or browser plugin(!), uses landmarks to programmatically identify sections of a page. It gives users a way to choose how to navigate the content of the page.

If you're still struggling with coming to terms with why/how this matters, here's one way to think about it: You like having options, right? You like the ability to choose things. How would you feel if that was taken away from you? How would it feel if you knew others could choose, but you were prevented from choosing?  Think about that for a little bit.
<h2>Landmark Roles</h2>
Okay, now that we've gotten that out of the way, let's talk about landmarks so we can understand how to use them. Here are a few tips:
<ol>
 	<li>The landmarks indicate the primary content items on the page.</li>
 	<li>All content should be in a landmark (to make an over-simplified analogy: all children need parents. I know. It's not perfect. Feel free to come up with your own.)</li>
 	<li>Landmarks can be nested (It makes your life easier if you avoid this until you understand it better).</li>
 	<li>Landmarks should be labeled (aria-label or aria-labelledby).</li>
 	<li>Don't use the landmark role in the landmark label, because AT already reads out the role after it reads out the label.</li>
</ol>
There are 8 landmark roles:
<ol>
 	<li>banner</li>
 	<li>complementary</li>
 	<li>contentinfo</li>
 	<li>form</li>
 	<li>main</li>
 	<li>navigation</li>
 	<li>search</li>
 	<li>application</li>
</ol>
<h3><span style="text-decoration: underline;">Banner &amp; Contentinfo</span></h3>
<ol>
 	<li><strong>TL;DR: put role="banner" on the header, and role="contentinfo" on the footer. Use them just once.</strong></li>
 	<li>If in the context of the &lt;body&gt; element, if you use the &lt;header&gt; element then you don't need the role="banner". Same goes for &lt;footer&gt; and role="contentinfo". BUT if you've nested these in sectioning elements, they will not have this default role.</li>
 	<li>Level up: Since you can nest document/application elements, you could <em>theoretically</em> have more than one banner &amp; contentinfo. But don't try this at home until you have fully embraced semantic HTML and really know how it works.</li>
</ol>
<h3><span style="text-decoration: underline;">Complementary</span></h3>
<ol>
 	<li>This is used for "a supporting section of the document" that is at the same DOM level as the main content, but is still meaningful when you separate it from everything else.</li>
 	<li>The content that goes in the element marked complementary should still be related; if it's not, then use a different role.</li>
 	<li>If it's an &lt;aside&gt; element, you don't have to put role="complementary".</li>
</ol>
<h3><span style="text-decoration: underline;">Form &amp; Search</span></h3>
<ol>
 	<li>For the &lt;form&gt; element (shocking, I know)</li>
 	<li>If the form is not a search, use role="form"; if the form IS for a search, use role="search".</li>
 	<li style="text-align: left;">The form should have a visible label, which can be indicated through the use of aria-labelledby, like this:
<img class="alignnone wp-image-393 size-full" src="http://blog.melsumner.com/wp-content/uploads/2017/05/form.jpg" alt="a code sample for an accessible form. " width="463" height="104" /></li>
 	<li>Did you see that I didn't include role="form"? That's because it has a label.</li>
 	<li>Here's how you'd do a search:
<img class="alignnone size-full wp-image-394" src="http://blog.melsumner.com/wp-content/uploads/2017/05/form-search.jpg" alt="code sample for an accessible search form" width="534" height="117" /></li>
 	<li>"But there's no visible label!" <em>Au contraire, mon ami</em>. The button says search and is the visible label in this context. YAY!</li>
 	<li>On a form, you could also use the title attribute. I don't recommend it because this tends to be not consistent on mobile devices. Because Android and stuff.</li>
 	<li>Now, as you already know, Ember provides an ID (<a href="https://emberjs.com/api/classes/Ember.ViewMixin.html#property_elementId">https://emberjs.com/api/classes/Ember.ViewMixin.html#property_elementId</a>). This means you could do all of this in your component code via attributeBindings (<a href="https://emberjs.com/api/classes/Ember.ViewMixin.html#property_attributeBindings">https://emberjs.com/api/classes/Ember.ViewMixin.html#property_attributeBindings</a>) and then not think about it anymore. Which I think makes it sooooo much easier.</li>
</ol>
<h3><span style="text-decoration: underline;">Main</span></h3>
<ol>
 	<li>The main content of a document or application.</li>
 	<li>If you use the &lt;main&gt; element, you don't have to put role="main".</li>
 	<li>Have <strong>one</strong> of these. Yes, the documentation says you can nest and therefore have more and....yeah, but no. If The Reasons Why™ apply to you, then just have one. We picked Ember because we're building really complex stuff in the first place, and this is an easy win to make your architecture more meaningful and this is one area where you don't need the added complexity, nor will I really give in to any excuses. I've never seen a legit use case for using more than one of these.</li>
</ol>
<h3><span style="text-decoration: underline;">Navigation</span></h3>
<ol>
 	<li>If you use the &lt;nav&gt; element, you don't need to add role="navigation"</li>
 	<li>if you have more than one &lt;nav&gt; element on your page, then it needs to have a unique label.</li>
 	<li>if you have two navigation elements on your page that have the same content (but why tho?) then they should have the same label.</li>
</ol>
<h3><span style="text-decoration: underline;">Application</span></h3>
<ol>
 	<li>This word does not mean what you think it means.</li>
 	<li>I'm going to do a whole post just on how to use this and not lose your mind. So I'm not going to go into it here.</li>
</ol>
<h3><span style="text-decoration: underline;">Bonus Role: Region!</span></h3>
<ol>
 	<li>The role="region" is the catch-all for "something that really should be in its own landmark but the other ones don't really fit it.</li>
 	<li>If you find yourself using this too much, rethink the design.</li>
</ol>
<h2>Navigating Landmarks</h2>
This part is pretty cool, you should try it yourself. Especially if you like to be super pro keyboard user, you can be zipping around pages in no time. I'm only going to cover a couple, so you might have to look it up if you use something different.
<ol>
 	<li>There are some browser extensions that will allow you to navigate landmark regions on a page. Explore.</li>
 	<li>NVDA + Firefox (Windows):
<ol>
 	<li>D will go to the next landmark</li>
 	<li>SHIFT + D will go to the previous landmark</li>
 	<li>NVDA + F7</li>
</ol>
</li>
 	<li>VoiceOver on iOS
<ol>
 	<li>W will go to the next landmark</li>
 	<li>SHIFT + W will go to the previous landmark</li>
 	<li>CTRL + OPTION + U will give you a list of landmarks (that you can keyboard navigate through/to)</li>
</ol>
</li>
</ol>
Okay, that's it for now. Hopefully this guide has given you a clear path forward for using landmark roles and helped you see ways that HTML5 &amp; Ember already help you do this.

<hr />
<p role="complementary"><em><small>Up Next: <a href="http://blog.melsumner.com/accessibility/application-vs-document-roles/">Application vs Document Roles</a></small></em></p>