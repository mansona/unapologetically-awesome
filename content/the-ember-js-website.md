---
title: 'Becoming an OSS Contributor: The Ember.js Website'
image: ''
authors:
  - melsumner_g2q1b4
date: 2018-01-15T16:38:28.000Z
tags:
  - ember
---
It's no secret that I have become an enthusiastic member of the Ember community. With my deep love of web standards and separation of concerns, Ember itself just ended up being a good fit for me- and the fantastic community upgraded a good fit to a <em>great</em> fit. One of the places I noticed I could contribute was to the Ember website itself- especially where accessibility standards are concerned!

In this article, I'll share my progress on an overhaul of Ember's public websites, and maybe there will be some tips for managing changes to a long-lived open source project along the way.
<h2>Goals</h2>
With such an open-ended project, it was important to define goals:
<ol>
 	<li>Improve the accessibility of the website (WCAG 2.0 AA standards)</li>
 	<li>Implement responsive (device-agnostic) design</li>
 	<li>Improving the CSS code by removing unused code and consolidating repeated code</li>
 	<li>Do all of this while keeping the website functional and using the constraints of the current project</li>
 	<li>Update/refresh the visual design</li>
 	<li>Document a visual design styleguide, so maintaining and contributing is even easier in the future</li>
 	<li>Use the documented styleguide to create components in both Ember (<a class="attrlink" href="https://github.com/ember-learn/ember-styleguide" target="_blank" rel="noreferrer nofollow noopener" data-target-href="https://github.com/ember-learn/ember-styleguide">ember-styleguide</a>) &amp; Glimmer(<a class="attrlink" href="https://github.com/ember-learn/glimmer-styleguide" target="_blank" rel="noreferrer nofollow noopener" data-target-href="https://github.com/ember-learn/glimmer-styleguide">glimmer-styleguide</a>)</li>
 	<li>Transform the website into an Ember app(and maybe some of the other apps into engines!)</li>
 	<li>Add content that will be helpful to prospective users</li>
</ol>
Very ambitious! Good thing this is Ember.
<h2>Project Management</h2>
Right now, I'm using Github's project feature to <a href="https://github.com/emberjs/website/projects/2">track the overall website project</a>, which has been useful to help me easily get a big picture view and make sure I'm at least tracking all of the ideas for the website that come my way. Here's a screenshot of that overview screen:

<a href="http://www.melsumner.com/blog/wp-content/uploads/2018/03/ember-project-overview.jpg"><img class="aligncenter wp-image-487 size-full" src="http://www.melsumner.com/blog/wp-content/uploads/2018/03/ember-project-overview.jpg" alt="Screenshot of github project. there are four columns- inbox, to-do, in-progress and done - that track multiple issues. " width="1661" height="896" /></a>

I like this method for a few reasons- I've used JIRA for a long time so this style of project management is familiar to me; Github has improved their projects feature and I like the automation of it. I can also spend time looking at this view and thinking about how I could break stories down into smaller stories, since we know that helps encourage new contributors.
<h3>The current process</h3>
<ol>
 	<li>Ideas for improvements or changes go into a card in the inbox. These can be my ideas, or ideas that I hear about from the Ember core team, or even just ideas that people post in the #team-learning channel on the <a href="https://ember-community-slackin.herokuapp.com/">Ember Community Slack</a> chat.</li>
 	<li>Once I have given those ideas enough details for actual work to begin, I convert them into issues, assign them to the correct repository, and they automatically end up in the "to-do" column. I also try to give them good labels, so other people can contribute!</li>
 	<li>If that issue needs to go into a different repository, I'll start the issue in that repository, but still track it here, that way I can keep tabs on the overall progress in one place. This was an accidental discovery for me, but was a very useful find. Here's what that looks like:  <a href="http://www.melsumner.com/blog/wp-content/uploads/2018/03/ember-project-trackotherissue-1.jpg"><img class="aligncenter wp-image-488 size-full" src="http://www.melsumner.com/blog/wp-content/uploads/2018/03/ember-project-trackotherissue-1.jpg" alt="a project card that shows the reference to an issue in a different org repository." width="298" height="250" /></a></li>
 	<li>I'll move an into the "In-Progress" column once I've started working on it or I know someone else is working on it.</li>
 	<li>Once an issue is closed or the code for that issue is merged, it is automatically moved to the "Done" column.</li>
</ol>
<h3>Creating a Styleguide</h3>
<a href="https://codepen.io/">CodePen</a> has been a really helpful tool for prototyping the styleguide. I can work out static designs and get feedback from other members of the learning team before implementation. It also allows me to make sure I've designed pieces that will work with the overall flow of the entire website. It also lends itself to discussion with the other members of the learning team- we can talk about a proposed element and make changes while we're having the discussion. Here's an example, using the call to action (CTA) components part:

<a href="http://www.melsumner.com/blog/wp-content/uploads/2018/03/ember-project-styleguide.jpg"><img class="aligncenter wp-image-489 size-full" src="http://www.melsumner.com/blog/wp-content/uploads/2018/03/ember-project-styleguide.jpg" alt="screenshot of a codepen that describes call to action elements and how they should be used." width="1651" height="787" /></a>

It's <a href="https://codepen.io/melsumner/pen/9d551738a81e319a773395a2cfa1a82e">still a work in progress</a>, so there are definitely ways for anyone to contribute- look for issues with the tag "design".
<h2>Completed work</h2>
It's been a bit of a recursive adventure to figure out not only what we <em>wanted</em> to do, but how best to approach it. The core website was built with Middleman - &amp; I've never worked with Ruby before, so it's been an adventure. On top of that, it took some detective work to figure out how to get it to build on a PC (my dev environment of choice). The guides, API, and builds app are all separate apps that are hooked into the core app- and I had to learn how all of those things fit together.

Here are some specific items that have been completed:
<ul>
 	<li>figured out how to organize the project &amp; wrote it down</li>
 	<li>page layouts have been (mostly) normalized to use semantic HTML and correct ARIA-* roles where required.</li>
 	<li>updated the color palette to at least pass WCAG 2.0 AA color contrast tests</li>
 	<li>determined the <a href="https://codepen.io/melsumner/pen/b09957277ef32aa0626bf6c227a4e961">site hierarchy</a> and how we wanted to organize the pages in the navbar (both in the interim and long-term)</li>
</ul>
<h2>In-Progress Work</h2>
Right now, we're working out the best way to integrate some of the design changes into the <a href="https://github.com/ember-learn/guides-app">Guides</a> and <a href="https://github.com/ember-learn/ember-api-docs">API</a> apps. I'm also working on the navbar, because we'd like to have dropdowns and a better mobile navbar. We're also working to finish the styleguide, so we can better support those who wish to contribute.

One new addition to the website is the "<a href="https://github.com/emberjs/website/projects/2#card-6523432">Why Ember</a>" section, new content that will be added to help engineers and executives consider the reasons Ember might be a perfect choice for their next project. This is in active development &amp; there is room for contributions. I think this part in particular will be a great community effort!
<h2>Planned Work</h2>
Here are some of the planned but not-yet-implemented items:
<ol>
 	<li><a href="https://github.com/emberjs/website/projects/2#card-5469907">convert the website</a> to an Ember app</li>
 	<li>break out the common parts into components (ember-styleguide)</li>
 	<li>improve the <a href="https://github.com/emberjs/website/projects/2#card-5481727">site's SEO</a></li>
 	<li>improve the <a href="https://github.com/emberjs/website/issues/3131">"Teams" page</a></li>
 	<li>develop, document and implement process for the <a href="https://github.com/emberjs/website/projects/2#card-6701592">statusboard</a></li>
</ol>
<h2>How this affects the website</h2>
<b>You may notice some changes</b> as you continue to visit and use the website ("wait...this didn't look like this yesterday..."). You might love the changes, but you might find something we missed, or something that doesn’t look quite right. If that happens, please <a class="attrlink" href="https://github.com/emberjs/website/issues" target="_blank" rel="noreferrer nofollow noopener" data-target-href="https://github.com/emberjs/website/issues">report it as an issue</a>. Thank you for your patience!
<h3>You can be a contributor too</h3>
There is also opportunity to become involved! Please come to the <a href="https://ember-community-slackin.herokuapp.com/">#team-learning channel on Slack</a>, or check out any of the repositories I've mentioned in this post. There are multiple ways to contribute- project management, content (writing and editing), marketing, QA, design, and development. Everyone is welcome!

&nbsp;

<em>Note: <a href="https://github.com/jenweber">Jen Weber</a> reviewed this post for content and accuracy. Thank you, Jen! </em>