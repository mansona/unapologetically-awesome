---
title: Web Fonts - Consider Mobile
image: ''
authors:
  - melsumner_g2q1b4
date: 2014-09-16T12:42:43.000Z
tags:
  - my-css3
---
Despite having earned the nickname "Mobile Melanie," there are still some ways in which I forget about mobile completely until someone reminds me OH HEY YOU HAVE TO PAY ATTENTION TO THAT. I get caught up in the loveliness of font pairings, and some user is left swearing at my page load times as a result.

Now this is not to say that I don't follow the conventional rules- only use the weights that you need. Try to combine etc where you can. But even after all of that, you can either go async and get the dreaded flash of unstyled text, or it just takes forever. Neither of these are cool.

I reminded myself that I need to write my @import rules properly in my css - for my work, my rule is that if it's not a tablet size, then don't import my fancy fonts, please.
<code>
@import url(http://fonts.googleapis.com/css?family=Open+Sans:400,600) (min-width:768px);
</code>