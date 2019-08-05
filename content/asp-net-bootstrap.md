---
title: ASP.NET and Bootstrap
image: ''
authors:
  - melsumner_g2q1b4
date: 2014-09-22T18:52:22.000Z
tags:
  - net
  - bootstrap
---
Part of my job is re-factoring outdated asp.net code.

Most people would be like, UGH. I'm like <em>YAY</em> because I get to take this old really ugly thing and give it new life...I get to fix it! This means, of course, using my most favorite developer tool- Bootstrap!

Sometimes, though, it's tricky to figure out just where to add in the classes. Just in case you have to do it too, here's something I figured out today.

On a regular HTML5 form, you add the css class to the select, like this:

<code><select class="form-control">
  <option>1</option>
  <option>2</option>
  <option>3</option>
</select></code>


In .net however, you add the form-control class to the DropDownList element instead of the Panel holding the DropDownList:

<code><div class="form-group">
  <asp:Label runat="server">Fund Type:</asp:Label>
    <asp:Panel ID="Panel1" runat="server" TabIndex="4">
       <asp:DropDownList ID="cboFundType" CssClass="form-control" runat="server">
       </asp:DropDownList>
  </asp:Panel>
</div></code>