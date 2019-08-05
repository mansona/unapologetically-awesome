---
title: Survey said so.
image: ''
authors:
  - melsumner_g2q1b4
date: 2018-04-29T14:32:45.000Z
tags:
  - tech
---
Any research data (survey or otherwise) should be better understood by people in tech.

While I was watching the <a href="https://twitter.com/hashtag/zeitday?src=hash">#ZeitDay</a> live feed, <a href="https://twitter.com/jamiebuilds">one of the speakers</a> had a slide that showed all of the things that go into their development process:

[caption id="attachment_540" align="aligncenter" width="1024"]<a href="http://www.melsumner.com/blog/wp-content/uploads/2018/04/dev-process.jpg"><img class="wp-image-540 size-large" src="http://www.melsumner.com/blog/wp-content/uploads/2018/04/dev-process-1024x544.jpg" alt="a list with 9 categories and 32 items" width="1024" height="544" /></a> Wow this is a big list![/caption]

Our seeming lack of ability to meaningfully interpret research data was still on my mind, and my immediate train of thought went something like this:

"<em>This is a great list. Wow that's a lot of things to know! Yay us. Wait, not yay us. How is it possible that we know how to do all of these things (including Accessibility, <strong>ahem</strong>) and still not understand how to interpret research results?</em>"

Since developers tend to live in echo chambers (sometimes out of willful ignorance, other times because we have too much to do already- refer to the list above), it's vital that we are able to think clearly when presented with survey data. Now, I'm not claiming to have this process down perfectly but I do have a grasp of the basics. My spouse is a research scientist (biomedical engineering), and we discuss this type of thing frequently.

Here are the steps I have found useful for the critical thinking process:
<ol>
 	<li>Understand the context</li>
 	<li>Understand the collection methods</li>
 	<li>Understand the backers</li>
 	<li>Understand why the research was even done in the first place</li>
</ol>
<h2>Understanding the context</h2>
Since a survey is only made up of the people who respond to it, let's examine ways we could understand the context more completely. For the purposes of this guide, we will be examining a claim:

<em><strong> "The survey data says that 50% of people who use X do Y."</strong></em>
<h3>Who took the survey?</h3>
Do you have a realistic number of the total number the survey was meant to reach, vs the number of folks who actually filled out the survey?

Let's compare two (of many) scenarios that might apply to this claim:
<h4><strong>Scenario A</strong></h4>
<ul>
 	<li>if we can approximate that 10,000 people use X</li>
 	<li>we know 1,000 people took the survey</li>
 	<li>the survey represents 10% of all users</li>
 	<li>the claim ("50%") represents 5% of all users who also did the survey</li>
 	<li>Ask yourself: if <strong>500</strong> people (50% of 1000) answered this way, out of the <strong>10,000</strong> total, do I think this is a statement that has enough significance for me to care about?</li>
</ul>
<h4><strong>Scenario B</strong></h4>
<ul>
 	<li>if we can approximate that 10,000 people use X</li>
 	<li>we know that 8,000 people took the survey</li>
 	<li>the survey represents 80% of all users</li>
 	<li>the claim ("50%") represents 40% of all users who also did the survey</li>
 	<li>Ask yourself: if <strong>4,000</strong> people (50% of 8,000) answered this way, out of the <strong>10,000</strong> total, do I think this is a statement that has enough significance for me to care about?</li>
</ul>
However, this <em>alone </em>isn't enough information to determine whether or not the data should be considered valid, because it *is* possible to get a small population that fairly represents the whole. So let's look at some of the other variables.
<h2>Understanding the Collection Methods</h2>
<ul>
 	<li><strong>Research should be reproducible.</strong> If the collection methods are not available, disregard the study entirely.</li>
 	<li><strong>Who can you contact?</strong> There should be someone you can contact if you have concerns about the data or the research. If no one is listed, it shouldn't be considered a viable study.</li>
 	<li><strong>How did they obtain survey respondents?</strong> This matters. Let's consider our example claim, and think about places where survey respondents could have been obtained (such as coding bootcamps, social media, meetup groups, users of a specific website, etc.)</li>
 	<li><strong>Did they obtain a survey population that accurately represents the whole? </strong>Again, it's possible to have a small sample of respondents that fairly represent the whole population, and it's important to be up front about that.</li>
 	<li><strong>Did they try to determine some sort of data normalization?</strong> Or did they address it if not? For example, a group of engaged coding bootcamp participants are more likely to answer a technical survey than a group of developers in a large enterprise organization.</li>
</ul>
<h2>Understanding the backers</h2>
<ul>
 	<li><strong>Who funded this work?</strong> If you can't figure that out, throw away the entire study. Scientific research is required to say who funded the study in the paper (it's usually the last section of the paper, or in the footnote if it's printed in a journal). It usually goes hand-in-hand with a conflict of interest statement. In general, if it's the most amazing thing you've ever read, but you can tell that the person who funded the research will somehow profit from these results, then you should be careful when interpreting the results.</li>
 	<li><strong>Who benefits from this work?</strong> It's easy to tweak any results to reflect what we want it to say.</li>
 	<li><strong>Who did the research?</strong> If the research was meant to be, say, a study about the community at large, but then only has committee members from a specific circle of that same community, assume implicit bias.</li>
</ul>
<h2>Understanding why</h2>
<ul>
 	<li><strong>Why was this research done in the first place?</strong> If it was a survey, what was the survey trying to determine? What outcomes or goals do they have? Is this research meant to only target an internal community, or a larger group of technologists?</li>
 	<li><strong>Are the reasons likely to produce a viable set of results?</strong> Consider some potential goals:
<ul>
 	<li>We want to show that X is more popular than Y</li>
 	<li>We want to demonstrate a new technology &amp; someone had the idea that doing a survey and putting those results on a website would be a fun thing</li>
 	<li>We do an annual survey</li>
</ul>
</li>
</ul>
<h2>Concluding thoughts</h2>
These are my own reasons for writing this guide:
<ul>
 	<li>I am disappointed with a few surveys that have gone around, such as <a href="https://insights.stackoverflow.com/survey/2018/">this one</a> and <a href="https://stateofjs.com/">this one</a>.</li>
 	<li><a href="https://twitter.com/sarahmei/status/988530872088387584">A tweet</a></li>
 	<li><a href="https://twitter.com/seldo/status/990006705080619009">Another tweet</a></li>
 	<li>because <a href="https://www.reddit.com/r/emberjs/comments/73v17i/is_ember_dying/">this happens</a> way too often</li>
 	<li>because <a href="https://twitter.com/jackiehluo/status/990285243776053249">this happens</a> way too infrequently</li>
 	<li>because it's important to keep learning and be <a href="https://www.ted.com/talks/john_green_the_nerd_s_guide_to_learning_everything_online">part of a community</a> who continues to learn</li>
 	<li>because <a href="https://store.dftba.com/products/about-the-test-poster">there will be a test</a></li>
</ul>
Here are some resources for more learning that I found interesting:
<ul>
 	<li>Redefining statistical significance: <a href="https://psyarxiv.com/mky9j/?_ga=2.29887741.370827084.1500902659-399963933.1500902659">https://psyarxiv.com/mky9j/?_ga=2.29887741.370827084.1500902659-399963933.1500902659</a></li>
 	<li>The Vox article about it: <a href="https://www.vox.com/science-and-health/2017/7/31/16021654/p-values-statistical-significance-redefine-0005">https://www.vox.com/science-and-health/2017/7/31/16021654/p-values-statistical-significance-redefine-0005</a></li>
 	<li>John Oliver- realistic-but-funny take on Scientific Studies: <a href="https://www.youtube.com/watch?v=0Rnq1NpHdmw">https://www.youtube.com/watch?v=0Rnq1NpHdmw</a></li>
 	<li>Test your implicit biases: <a href="https://implicit.harvard.edu/implicit/takeatest.html">https://implicit.harvard.edu/implicit/takeatest.html</a></li>
</ul>
We could do better in this area, and we can! Consider this: it <strong>may</strong> take a person less time getting up to speed on how to better interpret research results than it would take to figure out how to use that shiny new JS framework. Or something.