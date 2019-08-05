---
title: Legitimizing the gatekeepers
image: ''
authors:
  - melsumner_g2q1b4
date: 2019-01-28T22:03:35.000Z
tags:
  - development
---
<!-- wp:paragraph -->
<p>The first tech meetup I went to was a disaster. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>After finishing my time as an intelligence analyst in the US Navy, I briefly considered going into the information security branch of tech, as it seemed a reasonable next step for my skill-set at the time. So I decided to go to a meetup. I'm not an extrovert meetup kind of person, but I was determined. So I went. I opened the door resolutely and… was met with the curious faces of a room filled with men. They were <em>all</em> older white men. I was determined to be there since I’d taken the trouble to <em>go</em> there, so I went in anyway and sat at a table.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><em>“Are you sure you’re in the right room, sweetie?”</em><br></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Despite being simultaneously crushed and livid, I smiled brightly and said yes, I thought I was- the information security meetup, right? I cracked a joke about my (very bright red) hair, that it might make it <em>seem</em> like I was out of place, and my self-deprecating joke went over well enough. By the end of the night, I’d won some of them over with my generally affable nature and artistic note-taking style- but I felt the whole time like I was performing. Proving I belonged there. Proving that my being there had value.&nbsp;<br><br>I never went back.&nbsp;<br><br>Today, many years later, I am happy to say that things are not the same.  I found an inclusive place in Ember- not only as a community, but as a philosophical approach to web development. I’m proud of the Ember community and what we’re trying to do- bring sensible abstractions and defaults to web development. Ember respects separation of concerns, and the best ideas eventually end up in Ember. They are discussed, reasoned about, and implemented. There is a commitment to backwards compatibility too, something that is practically unheard of elsewhere in the JS landscape.<br>&nbsp;<br>I’m not proud of web development as a whole, though. Look, I know the super-trendy thing is to sub-tweet and make some vague random statement about how everyone is shit and the internet is yet again on fire, but I’m too old to be that cool.&nbsp;<br></p>
<!-- /wp:paragraph -->

<!-- wp:image -->
<figure class="wp-block-image"><img src="https://d2mxuefqeaa7sj.cloudfront.net/s_8A04D9756ADC50C9301EE057C9B1940798EA1280073E2180C77E0D2BD0BF9F0F_1548709930620_image.png" alt="A tweet that suggests that we stop considering JS-based CSS solutions to be a failure of developers to learn CSS- a tweet that I strongly disagree with."/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>I skip most of the web developer drama- I purposefully work to engage in a positive way with positive things. But this one bothered me on a deeply personal level. Developers who fail to learn CSS or advocate for hiring a CSS specialist <em>are</em> failing. I strongly believe that. I also I want to take some time to write out an explanation for <em>why</em>. <br><br>Web development is supposed to have layers. It's always had layers. We started out with one layer and kept adding layers and it was working out pretty great. Somewhere along the way, though, business managers decided that “really, I only care about the functionality, let’s just hire JS engineers.” <br><br>Instead of a well-balanced team that has overlap but still maintains depth in their own area of expertise, the folks that write the checks decided that they were only going to hire developers who could provide the functionality because that is where the <em>true</em> value was (or so they thought). They could hire someone later "to make it pretty." <br><br>Web developers decided that it wasn't their job to get involved in things like that (heaven forbid communication skills be part of their job!), and the way teams were built changed. <br><br>So instead of this (or something similar):</p>
<!-- /wp:paragraph -->

<!-- wp:image -->
<figure class="wp-block-image"><img src="https://d2mxuefqeaa7sj.cloudfront.net/s_8A04D9756ADC50C9301EE057C9B1940798EA1280073E2180C77E0D2BD0BF9F0F_1548710437687_image.png" alt="four circles that are all distinct yet overlap with the previous- design, front end, back-end, and sys admin."/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>We’ve ended up with something more like this:&nbsp;<br></p>
<!-- /wp:paragraph -->

<!-- wp:image -->
<figure class="wp-block-image"><img src="https://d2mxuefqeaa7sj.cloudfront.net/s_8A04D9756ADC50C9301EE057C9B1940798EA1280073E2180C77E0D2BD0BF9F0F_1548710527517_image.png" alt="three distinct, non-overlapping circles- design, full-stack and sys admin."/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>No overlap. No cross-knowledge. Any kind of overlap does end up happening is accidental. Everyone blames everyone else for the performance issues or inconsistent design. And fuck accessibility, because do disabled people really even exist? Do they even need to use the internet? Nah, prolly not. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Who pays for all of these terrible decisions?</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><li>The people trying to use the stuff we've built </li><li>The developers hired after us, who are trying to make sense of our code</li><li>the accessibility consultants called in to fix things because there might be a lawsuit</li><li>hiring managers, because how do you even look for someone who can do all the things? </li><li>anyone who applies to the job</li></ul>
<!-- /wp:list -->

<!-- wp:heading -->
<h2>Looking for a solution</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>It’s less and less feasible for a front-end developer who specializes in HTML &amp; CSS to find work- <em>of course</em> they have to know JS. We’ve all read about (or experienced) the “front-end” interviews that asked us to whiteboard algorithms. We’ve experienced books like “JavaScript for Designers” because of course designers should want to learn about that (although to be fair to the author, I think it was a life-preserver to anyone who found it, and it was good that they took the time to write it). <br><br>Then, CSS-in-JS showed up, brought to us by the same kind of people who think HTML is shit (“divs and spans are all the elements you need!”). Why is this problematic? Well, it's problematic because it mandates their <em>own</em> skill-set as legitimate, entry-level skills- despite them <em>not</em> being entry level at all. It effectively blocks out everyone who never had to do that before. Who has absolutely no desire to even start to learn that, because what for the love of god is that mess even? Do you specialize in HTML and CSS? Have a deep knowledge of ARIA? Forget about it. All you need is JS.  _________-in-JS <em>if ya</em> <em>nasty</em>. <br><br>It’s messy, it’s not sustainable, and it’s lazy. Long-term, deep-in-the-bones lazy. It’s lazy because it’s easier to invent something “new” than to have a conversation. It’s easier to look like you’re delivering value by developing a complex solution (that only you or people like you can use, much less understand). It’s easier to ship this convoluted thing instead of learning the basics, because you’re better than the basics, you’re a computer scientist. It’s easier to tout this convoluted thing as the answer, because then you don’t have to recognize the expertise of anyone else that doesn’t look like you. That doesn’t do things exactly the way you do things. You don’t need to learn what they do anymore, because you can force them to learn your way.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>When the balanced product team went away (or in some cases, just never existed), it became <em>not</em> okay to specialize in HTML and CSS as a front-end developer anymore. Somewhere along the line, a business person convinced us that we should shove the CSS to the designers and the JS devs decided that divs and spans were just fine, and the genuine craft of front-end development was eviscerated. <br><br>To make matters worse, folks have started trying to legitimize this "JS-all-the-things" behavior by calling for them to be invited to the table to discuss their ideas- and I’ve just had enough. I very strongly think that doing this is legitimizing gate-keeping behavior, and it’s total bullshit.  <br><br>Developers- we need to <strong>advocate</strong> for more well-rounded teams. We need to <strong>push back</strong> on a business model that insists that we ship it yesterday. We need to <strong>be willing to learn</strong> the things that have come before, so we can build for a better tomorrow. We need teams that have a strong makeup of all skill sets, and that respect the skill set of each team member.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Furthermore, we need to have the fortitude to point out that gate-keeping is wrong.</p>
<!-- /wp:paragraph -->

<!-- wp:image -->
<figure class="wp-block-image"><img src="https://d2mxuefqeaa7sj.cloudfront.net/s_8A04D9756ADC50C9301EE057C9B1940798EA1280073E2180C77E0D2BD0BF9F0F_1548711450685_image.png" alt="Tweet by Estelle Weyl: &quot;Next time I get asked to write a recursive function on a white board during a job interview, I'll reply: sure right after you list 320 CSS properties on the whiteboard. Oh, and you can't look anything up either!&quot;"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>JavaScript is <em>part </em>of the answer. It does a lot of wonderful things and I’m so glad it exists! But it’s not the only thing that exists and <strong>it must not be considered the only solution.</strong> <br></p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><li>HTML for document structure (and accessibility!)&nbsp;</li><li>CSS for document style (and accessibility!)&nbsp;</li><li>JS for document functionality (and accessibility!)&nbsp;</li></ul>
<!-- /wp:list -->

<!-- wp:image {"align":"center"} -->
<div class="wp-block-image"><figure class="aligncenter"><img src="https://d2mxuefqeaa7sj.cloudfront.net/s_8A04D9756ADC50C9301EE057C9B1940798EA1280073E2180C77E0D2BD0BF9F0F_1548712133041_triquetra.jpg" alt="a triquetra-a three-sided shape that all works together to make one single shape. "/></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>If the CSS-in-JS crowd wants to keep doing their thing, I don’t care. “God bless them, and keep them far away from us.” And I really mean that.&nbsp; </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The second we legitimize it though? Heaven help us.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong><em>Here's my call to action:</em></strong> If you are a developer who specializes in JS, advocate for a more balanced team if the only skills you see on your team are the same as yours. Find another developer that <em>complements</em> your JS skills with their HTML and/or CSS skills, and form a life-long friendship with them. Talk about the value that their knowledge brings to your product. Trade knowledge with them. Figure out where things can overlap and live in harmony without being insulting or exclusive. Advocate for the hiring of front-end specialists to your boss.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Having different types of talent on your team does not lessen your importance, it helps create a better product. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>We can do this. We have the technology. </p>
<!-- /wp:paragraph -->