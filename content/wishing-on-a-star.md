---
title: Wishing on a Star
image: ''
authors:
  - melsumner_g2q1b4
date: 2018-05-02T20:24:23.000Z
tags:
  - ember
  - tech
---
<blockquote>The Ember project has opened a <a class="markup--anchor markup--p-anchor" href="https://emberjs.com/blog/2018/05/02/ember-2018-roadmap-call-for-posts.html" target="_blank" rel="noopener nofollow" data-href="https://emberjs.com/blog/2018/05/02/ember-2018-roadmap-call-for-posts.html">Call for Blog Posts</a> to help inform the first ever EmberJS project roadmap! Read my thoughts below, then share your own with the hashtag <strong class="markup--strong markup--p-strong">#EmberJS2018</strong>.</blockquote>
This is my wish-list for the things I'd like to see happen in the Ember ecosystem in 2018! The overall theme of how I imagine things <em>could</em> be? "Developer ergonomics."
<h2>Accessibility</h2>
My #1 goal for this year is to see us figure out how to tell assistive tech that the view has changed (even if the URL hasn't). No framework solves this problem out of the box yet. It might be bigger than a framework- it might take coordination with browsers and folks to work on assistive tech. BUT, I'd like us to figure this out- and <a href="https://speakerdeck.com/melsumner/ambitious-for-all-slides-only">I definitely believe this is possible</a>. I believe we can be magnanimous and inclusive and get this done for EVERYONE.

I also really like <a href="https://twitter.com/jgwhite">Jamie White's</a> RFC that addresses the need for <a href="https://github.com/emberjs/rfcs/pull/327">Semantic Test Selectors!</a> The idea of Ember providing the well-lit developer path for more inclusive development is something that I am completely on board with. Developers don't want to have to think about this sort of thing- so making it there by default is super helpful!
<h2>Ember Engines</h2>
The <a href="http://ember-engines.com/">ember-engines</a> model for "how to giant apps" is absolutely incredible, especially for companies with globally distributed teams. It allows teams to build individually but then it all comes together without name-spacing issues. It's so.fucking.cool. Right now, dependency management is very difficult though. It's hard to explain to globally distributed teams that "yes you can build in isolation but if you want it all to work when it comes together you really need to plan your dependency versions better" because I then get the response of "then what's the point of using engines at all?" (which ugh but okay)

Things that would explicitly make my day job easier:
<ul>
 	<li>teams could not have to care about what versions of dependencies were in peer engines (say, as long as the major release was the same, maybe?)</li>
 	<li>there would be some sort of exploration phase of the build, so that dependency tree-shaking could happen a bit more intelligently.</li>
 	<li>the documentation would be more clear about the problems you would see if you chose to do things weirdly- this might seem like a weird ask but when you think about the types of issues that an enterprise team would face, and that the use case for ember-engines is well-suited for the enterprise environment, it will start to make sense why this is an explicit wish-list item.</li>
 	<li>there would be an increased number of use cases around ember-engines so more experimentation can be done</li>
 	<li>the testing story being clearly defined (and maybe finished!)</li>
</ul>
<h2>Better Evangelism</h2>
Developers that love Ember really love Ember....but after the 100th time you hear "wait Ember is still a thing?" it gets pretty old. It's especially frustrating to see newer frameworks trying solutions we already know won't work, or shouting that they've invented something new when it already exists in Ember. It's discouraging to see devs not understand how Ember frees you from needing to care about the inconsequential decisions that are maybe fun to work on, but will get in your way when you're trying to ship business value. It's irritating to be rejected in a conference CFP because you used Ember in your examples, and not (anything else).

I want everyone who loves Ember.js to <a href="https://airtable.com/shrDbeo2Y80OPG0kC">speak up and be counted</a>, with a strong bias toward action. Be present, loudly but not obnoxiously. I want our internal community to feel so supported that they don't have any complaints to begin with, and if they do, they'll come <a href="https://airtable.com/shrsgB80mALIPXj7j">talk to someone about it</a> first.

This June, it will be 22 years since my Uncle Paul gave me my first computer and told me, "learn how to write code for websites- and not just how to use a GUI tool. Write the actual code. That's the future." I started writing code then and I'm still writing it now and I can say beyond a shadow of a doubt, that <a href="https://emberjs.com/">Ember.js</a> is the thing I've been looking for all my life- and I'm here to help it be everything we have ever imagined.

[caption id="attachment_554" align="aligncenter" width="707"]<a href="http://www.melsumner.com/blog/wp-content/uploads/2018/05/be-magnanimous.jpg"><img class="wp-image-554 size-full" src="http://www.melsumner.com/blog/wp-content/uploads/2018/05/be-magnanimous.jpg" alt="be magnanimous" width="707" height="397" /></a> #EmberJS2018[/caption]