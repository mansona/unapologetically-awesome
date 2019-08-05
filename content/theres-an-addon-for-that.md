---
title: There's an addon for that.
image: ''
authors:
  - melsumner_g2q1b4
date: 2017-05-24T12:23:52.000Z
tags:
  - accessibility
---
Now that you understand the TL;DR basics (and more if you've followed the links) about landmark roles, it's now time to tell you that there's an addon for that.

My Mother's Day gift was <em>time</em> (seriously, best gift ever), and I had the entire day to myself to work on personal code. I used part of that day to build an Ember addon that will help with landmark roles: <a href="https://github.com/MelSumner/ember-a11y-landmarks">ember-a11y-landmarks</a>.
<h2>How it works</h2>
This template code:

<img class="alignnone wp-image-431 size-full" src="http://melsumner.com/blog/wp-content/uploads/2018/03/a11y-landmark-code-sample-1.jpg" alt="screenshot of handlebars template code to use the Ember A11y Landmarks addon" width="390" height="86" />

Renders into this:*

<img class="alignnone wp-image-432 size-full" src="http://melsumner.com/blog/wp-content/uploads/2018/03/ember-a11y-landmarks-1.png" alt="screenshot of rendered html" width="497" height="271" />

You'll notice a few things:
<ol>
 	<li>It's meant to be used as a containing block.</li>
 	<li>the appropriate ARIA role is determined and added automatically.</li>
 	<li><a href="http://melsumner.com/blog/accessibility/understanding-structure-landmarks/">Remember when you learned</a> that certain landmark roles don't have to have roles attached if they are direct children of the body element? Yeah, that doesn't really work in Emberland, because there's always that div element around everything. BUT, this made the addon a bit easier to write.</li>
 	<li>"But what about a form element that's got the role of search?" I'm so glad you asked!</li>
</ol>
<h3>Form vs Search</h3>
Since the form element can have either role=form or role=search depending on use, you'll need to define both in this case.

So this template code:

<img class="alignnone size-full wp-image-424" src="http://melsumner.com/blog/wp-content/uploads/2018/03/a11y-landmark-form-code-sample.jpg" alt="screenshot of HBS template code for setting up a form that is used as a search" width="575" height="137" />

Renders into this:*

<img class="alignnone size-full wp-image-425" src="http://melsumner.com/blog/wp-content/uploads/2018/03/a11y-landmark-form-code-sample-rendered.jpg" alt="screenshot of rendered html of a form element with the search role" width="531" height="102" />
<h2>Guardrails</h2>
This addon might not be everyone's favorite. It doesn't allow the usual indulgence that a lot of JS Engineers are typically used to having, due to HTML's implicit tolerance. Accessibility, however, really depends semantic HTML! This addon helps you achieve that for your elements that should have landmark roles, and the console log error messages will help you do the correct thing. So maybe it will BECOME your favorite.
<ol>
 	<li>You must define a tagName OR a landmarkRole.</li>
 	<li>You shouldn't define a tagName AND a landmarkRole, unless you're using tagName=form and landmarkRole=search.</li>
 	<li>If you try to use non-valid values, it will throw an error (and tell you what the valid values are)</li>
 	<li>If no tagName is defined, a div is used as per (Ember) usual.</li>
</ol>
<h3>Valid tagName values</h3>
<ul>
 	<li>aside</li>
 	<li>footer</li>
 	<li>form</li>
 	<li>header</li>
 	<li>main</li>
 	<li>nav</li>
 	<li>div (default)</li>
</ul>
<h3>Valid landmarkRole values</h3>
<ul>
 	<li>application</li>
 	<li>banner</li>
 	<li>complementary</li>
 	<li>contentinfo</li>
 	<li>document</li>
 	<li>main</li>
 	<li>navigation</li>
 	<li>region</li>
 	<li>search</li>
</ul>
You'll notice that "form" is not a valid landmarkRole here, and that's because the tagName=form should be set instead. Again, a friendly Ember.assert will help you here, too.
<h2>Considerations for use</h2>
Building this addon was more about me learning all of the little details that go into building an addon. I've thusfar worked on other addons but have never built one from start to publish on my own. As such, I'm not unrealistic about the simplicity of it.

There is also still an issue where I haven't decided how to handle the role=application/role=document issue. I have to think more about that and probably will ask for some advice from the community about it, because there really should be specific checks in place that help that use case be successful.

But if you wanted to try it out, then feel free to `ember install ember-a11y-landmarks` and give it a go.

You can also tell me all the ways my code is wrong <a href="https://github.com/MelSumner/ember-a11y-landmarks/issues">here</a>, or contribute a PR <a href="https://github.com/MelSumner/ember-a11y-landmarks/pulls">here</a> (thank you to <a href="https://github.com/endangeredmassa">@endangeredmassa</a> and <a href="https://github.com/ksin">@ksin</a> for being great early contributors!).

&nbsp;

<hr />

<small><em>*Your search sample code probably looks better. I know.</em></small>