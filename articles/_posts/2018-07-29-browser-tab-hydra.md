---
layout: post
date: '2018-07-29 10:51:00 -0700'
title: 'Taming the browser tab Hydra'
tags: UX
excerpt_separator: <!--more-->
---
There's this great [article from the Nielsen Norman Group about page parking](https://www.nngroup.com/articles/multi-tab-page-parking/)&mdash;a form of tabbed browsing&mdash;which [I've microblogged about](http://fionavoss.blog/2018/06/28/60647) [multiple times](http://fionavoss.blog/2018/05/26/68520) because I find it completely fascinating.

The article contrasts page parking with parallel browsing. In parallel browsing, the user keeps many tabs open in order to easily switch between tasks. For example, they might keep their email in one tab, Twitter in another, Facebook in a third one, and so on.

<!--more-->

In page parking, however, the user employs many tabs to fulfill a single task. It's common when shopping online or viewing search results. I might search for a product in an online store, rapidly open each result in a new tab, and close the tabs as I narrow down my choices.

In the interest of working toward a complete taxonomy of types of tabbed browsing, I want to describe a third form, which I haven't seen Nielsen Norman write about&mdash;ironically, since theirs is a website I often do this on. I call it the Hydra.

# What is the Hydra?

The Hydra will be familiar to any curious person who's ever browsed Wikipedia or [TV Tropes](https://tvtropes.org/). It can happen on any content-heavy site whose articles contain many links to other articles on the same site. I started writing this post today because I found myself doing it on [Above Avalon](https://www.aboveavalon.com/).

The Hydra is born when, as you read, you open interesting-sounding links in background tabs to read later. When you finish reading one page, you close its tab and move on to the next one. Like the heads of [the mythical Hydra](https://en.wikipedia.org/wiki/Lernaean_Hydra), for each tab you close, you open several more.

The Hydra is distinct from page parking because page parking follows a hub-and-spoke pattern, with many tabs born from one page, while the Hydra is tree-shaped, with any page capable of spawning several tabs.

It's both beautiful and dangerous. Beautiful because it enables discovery, but dangerous because it can be a major time suck. I've stayed up shockingly late browsing TV Tropes, and [I have plenty of company](https://tvtropes.org/pmwiki/pmwiki.php/Main/TVTropesWillRuinYourLife).

# Taming the Hydra: for users

[I've microblogged before](http://fionavoss.blog/2018/06/28/60647) about how I use the read-it-later service [Pocket](https://getpocket.com/a/queue/list/) to approximate page parking without actually opening things in tabs.

This works great for taming the Hydra, too. It's much easier to walk away from a site when the articles are tucked away in my Pocket, rather than waiting in browser tabs. My computer likes it, too: my MacBook Air can get seriously laggy when I have too many tabs open, and using Pocket prevents this.

# Taming the Hydra: for web developers

The Nielsen Norman article ends with some recommendations for making sure your website accommodates page parking well. All of them are good guidelines for designing for the Hydra as well, especially these:

- Don't break users' ability to open pages in a new tab. (A shockingly large number of sites do this.)
- Design a good favicon and use descriptive page titles so users can identify which tab is which. (The favicon doesn't help me distinguish between TV Tropes pages, but it does help differentiate between my 20 TV Tropes tabs and my one Twitter tab.)
- Don't make links open in new tabs automatically; let users choose.

For the Hydra specifically, I will add:

- Keep your pages lightweight. If you have the kind of site that encourages Hydra behavior, then keeping 30+ tabs open indefinitely shouldn't tax the user's computer.
- Test your site in services like Pocket to ensure that they parse your markup correctly.
