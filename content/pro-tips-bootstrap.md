---
title: 'Pro Tips: Bootstrap'
image: ''
authors:
  - melsumner_g2q1b4
date: 2014-09-19T20:30:18.000Z
tags:
  - bootstrap
---
When you're getting started with Bootstrap, it's easy to overlook some of the handiest of classes. I attended a "HTML5 and Bootstrap are super cool, you should use them" type of talk today, and noticed a few things that I'd like to share with the class:

1. Don't use inline styles. FOR THE LOVE OF GOD PLEASE DON'T USE INLINE STYLES.
2. Remember to wrap your tables in a div with this class: <code>.table-responsive</code>
3. There's a <code>.img-responsive</code> class. Please use it.
4. Learn the helper classes! Especially <code>.hidden-xs</code> and what it means. It will be a good friend.
5. Bootstrap documentation says (or it did last time I was reading it) to put your column classes in order from smallest screen size to largest....So <code>col-xs-12 col-sm-6</code> instead of <code>col-sm-6 col-xs-12</code>


If you're on a .net platform, there are a few more considerations for Bootstrap, and I'll try to blog about specific solutions I've discovered for the .net platform...quirks.