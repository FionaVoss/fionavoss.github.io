---
layout: post
date: '2018-06-08T02:23:29.419Z'
title: 'iOS double tap mystery solved'
tags: JavaScript
redirect_from: /2018/06/07/8609
excerpt_separator: <!--more-->
---
Fixed a fun front-end bug yesterday:

I had an image that was supposed to change to another image on hover, and link to another page on click. My original implementation used two image tags: one hidden, one visible. Visibility was toggled on hover using JavaScript.

This worked fine on desktop, but in Safari on iOS, you had to tap twice: the first tap turned on the hover effect, and the second tap activated the link.

<!--more-->

[This post from CSS Tricks](https://css-tricks.com/annoying-mobile-double-tap-link-issue/) got me on the right track, even though it&#39;s about CSS and my problem was in JavaScript. Turns out this behavior is a &quot;feature&quot; in iOS: since touch interfaces don&#39;t have hover states, Apple decided to make the first tap trigger the hover effect, and the second tap trigger the click event.

Key detail: this behavior doesn&#39;t happen with all hover effects. It only happens when the `display` attribute is changed by hovering.

The fix: only use one image tag, and instead of toggling the visibility, toggle the `src` attribute. Now, with a single tap, the hover effect appears briefly, and then the link takes you to the next page.
