---
title: BBIS event registration form attribute "fix"
image: ''
authors:
  - melsumner_g2q1b4
date: 2014-09-02T20:19:37.000Z
tags:
  - my-bbis
  - javascript
---
Turns out there IS a way after all. Had to add some functionality that I didn't even know existed, and translate the JavaScript into jQuery, but it works!

<div data-height="268" data-theme-id="8230" data-slug-hash="mFoly" data-default-tab="js" data-user="melsumner" class='codepen'><pre><code>var prm = Sys.WebForms.PageRequestManager.getInstance();
prm.add_endRequest(EndRequest);

function EndRequest(sender, args) {
    AttributeCustomizations();
}

$(document).ready(function () {
    AttributeCustomizations();
});

function AttributeCustomizations() {
    $(&#39;table[id*=&quot;dgRegistrationsList&quot;]&#39;).children().not(&#39;:first&#39;).each(function () {
        var dietPref = $(&quot;label:contains(&#39;Dietary Restrictions&#39;)&quot;, this).parent().parent();
        // set a variable
        var toptable = dietPref.parent().parent().parent().parent().parent().children();
        // alert to see content for debugging
        //alert(toptable.html());
        // find dinner label
        if (toptable.find(&#39;td[class=&quot;EventItemRegistrantsHeader&quot;]:contains(&quot;Dinner&quot;)&#39;).length &gt; 0) {
            dietPref.show();
        } else {
            dietPref.hide();
        }

    });
}</code></pre>
<p>See the Pen <a href='http://codepen.io/melsumner/pen/mFoly/'>mFoly</a> by Melanie Sumner (<a href='http://codepen.io/melsumner'>@melsumner</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
</div><script async src="//codepen.io/assets/embed/ei.js"></script>