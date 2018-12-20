---
layout: post
date: '2018-09-25 18:40:00 -0700'
title: "How I'm microblogging these days"
tags: 'Blogging'
---
About two months ago, I stopped microblogging on this site. At first it was just an experiment, but I like what I'm doing now and I think I am going to stick with it. Since I previously blogged about [microblogging in Jekyll]({% post_url /2018-04-01-microblogging-in-jekyll %}), I wanted to post an update describing what I'm doing now.

I'm still microblogging, but I've switched to a [Micro.blog](https://micro.blog/)-hosted weblog, which is at [fiona.micro.blog](http://fiona.micro.blog/). I post [links](http://fiona.micro.blog/2018/09/21/in-which-a.html), [quotes](https://fiona.micro.blog/2018/08/27/as-they-say.html), [photos](http://fiona.micro.blog/2018/09/02/when-the-strange.html), [summaries](https://fiona.micro.blog/2018/08/19/how-should-managers.html) and [other short posts](http://fiona.micro.blog/2018/09/20/my-data-structures.html) there, while I use [fionavoss.blog](http://fionavoss.blog) for longer, titled blog posts.

# Why I did it

The main reason I did it is because, with over 200 posts, this site was getting really slow to build, and it was obviously going to get worse over time. I like to tinker with the layout and organization of this site a lot, and waiting 30+ seconds for the site to build every time I changed one line of code was really annoying. Micro.blog-hosted blogs are actually powered by Jekyll, too, but since they are not fully customizable, having a large number of posts isn't a problem.

Another reason is photos. While I did set up this site for microblogging from my phone, I never took the time to set up photo uploads. With the Micro.blog-hosted microblog I can post photos without having to take any extra steps.

Finally, another annoyance was that I had some formatting issues when trying to post from [Quill](https://quill.p3k.io/) or the Micro.blog app to my site via [the micropub endpoint I was using](https://github.com/voxpelli/webpage-micropub-to-github). The `>` character would get converted to its HTML character code, breaking my Markdown formatting. Since I post a lot of quotes, this was pretty annoying.

# How I did it

I've hidden my old microposts on this site, but I haven't removed them. This was easy because I was previously using categories to separate my long and short posts. I just removed the short posts from navigation, so that my [home page]({% link index.html %}) and [topics page]({% link topics.html %}) only list long posts from my `articles` category.

The individual pages for my microposts are [still up](/2018/05/16/2380), so any links to them on other websites still work. Unfortunately that means my site is still slower to build than it would be if I got rid of the short posts, but it is faster than it was when I was including them in the index and topics pages.

# How it's (not) affected my writing

One of the things I liked a lot about microblogging on my own site was that I found writing untitled posts [took a lot of friction away from my writing process]({% post_url /2018-06-24-untitled-blog-posts %}). I am still benefitting from that effect, even though I have a separate microblog now. Sometimes, I will start writing a post for my microblog, and when it gets longer than planned, I will give it a title and publish it on this site instead. [Here's an example of a post that grew that way.]({% post_url /2018-09-13-yesterdays-tech-news %})

# On posting to Twitter

I also experimented with turning off cross-posting to Twitter, although I have it turned back on at the moment. The reason I turned it off was because I was annoyed with how certain posts appeared in Twitter, as I described [previously]({% post_url /2018-06-24-untitled-blog-posts %}#im-giving-more-of-my-posts-titles-now).

However, one of the reasons I am on Twitter is to keep in touch with friends and acquaintances in my industry, such as people I've met at conferences who live in other cities. Cross-posting helps me achieve that goal, because it means friends on Twitter can see what I'm up to. I think it's likely that I will experiment with turning cross-posting off and on some more, but I'm happy having it on for now.
