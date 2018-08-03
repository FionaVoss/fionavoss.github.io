---
layout: post
date: '2018-08-02 19:50:00 -0700'
title: 'Your technical blog belongs on your own domain'
tags: Blogging
excerpt_separator: <!--more-->
---
This post is inspired by Ryan Farney's post, ["Why Your Technical Blogs Belong On Dev.to"](https://dev.to/ryanfarney3/why-your-technical-blogs-belong-on-devto-1hlf). In his post, Ryan contrasts [Dev.to](https://dev.to/), a social network for developers, with Medium, arguing that Dev.to is a better choice.

I have no particular problem with Dev.to, and no opinion on whether it's better or worse than Medium, but I was frustrated by the way his post was framed as if it and Medium are the only options.

<!--more-->

In my opinion, the best place by far for a technical blog is on a domain that you own. That could mean using Jekyll, Hugo, or another static site generator; a dynamic CMS such as Wordpress; rolling your own blog software in Rails or another framework; or a no-coding-required solution that lets you use your own domain, like [Micro.blog](https://micro.blog/) does.

When I started blogging, I initially thought about using Medium, thinking my blog would get more traffic there. I ended up picking Jekyll mainly because I wanted to learn the technology, not because I cared about having my own domain at the time. But I am glad I did, because I have since learned that there are many benefits to blogging on your own domain.

So, because I want to share what I've learned with other bloggers (and future bloggers), here are my responses to a few of Ryan's points:

# Code snippets

Ryan says Dev.to is good for displaying code snippets, but Jekyll makes this really easy, too. You get syntax highlighting in many programming languages out of the box. [Here's a post with some Ruby code snippets]({% post_url /articles/2018-05-16-ruby-methods-are-objects %}), and [here's one with Liquid, HTML, and Markdown]({% post_url /articles/2018-04-01-microblogging-in-jekyll %}).

I haven't used other static site generators much, but they're made for developers, so I'm going to confidently assume they have good support for code snippets. If you use Wordpress, there are plugins you can install for syntax highlighting, and if you build your blog in Rails, there are gems for it.

So, if you blog on your own site, you have plenty of options for displaying code nicely.

# Learning

Blogging on your own domain means you can code your own site, which is an opportunity for learning that you won't get on Medium or Dev.to. For example, using Jekyll for my blog has allowed me to learn [Liquid](https://shopify.github.io/liquid/), the templating language developed by Shopify. Rolling your own dynamic CMS would be a great way to learn a new framework.

Plus, if have your own domain, you can switch things up when you want to learn a new technology. This is because owning your domain gives you portability. You can start out with Jekyll or even a no-coding-required system, and switch to Wordpress or anything else without changing your URL.

If you start out on Dev.to and want to switch to something else, your old posts won't move to your new URL with you. If Dev.to ever shuts down, any links to your posts on other websites will be broken.

(By the way, this is why you should have your own domain if you're hosting a Jekyll site on GitHub Pages. Are you sure you want to use Jekyll forever? If your site is at *you.github.io* but you want to switch to a technology GitHub Pages doesn't support, you can't do it without changing your URL.)

# Career advancement

If you want to blog in order to advance your career, using your own domain has several advantages. For one, if your domain is your full name, then your blog will help get your name noticed.

If you code your own blog, then you have code you can show to potential employers. If you're a front-end developer, you can show off your design skills. If you're a back-end developer, you can implement advanced functionality like [Webmentions](https://indieweb.org/Webmention).

Also, you have more control over your own reputation than you do over Medium's or Dev.to's. Those sites might have a lot of high-quality content by respected developers right now, but what if they get overrun by low-effort, spammy blogs? Their reputation will decline, and people will be less likely to click through to your writing because of it.

# User experience

Dev.to might have a great user experience, but blogging on your own domain gives you much greater flexibility. You can add any features you want, or go minimalist. You control how your archives are organized, and which "related posts" get displayed.

And again, even if you think Dev.to's user experience is perfect right now, they can always change on you, and you won't be able to do anything to stop it. If you own your domain, nobody can add advertisements, intrusive tracking, or obnoxious social media integrations, except you.

# The best of both worlds

If you are using Medium or Dev.to and you like it, I'm happy for you. I just want to see you blogging, on whatever platform works for you. Still, I encourage you to consider blogging on your own domain.

One thing that I like about Medium is that they have a tool for importing posts from another site. I publish on my blog first, and then import them into Medium because it helps a few more people find my writing. There's a little note at the bottom of the post which says where and when it was originally published, so readers can find their way back to my blog. [Here's an example](https://medium.com/@fionavoss/why-i-went-back-to-school-for-a-computer-science-degree-after-a-code-bootcamp-e6b8840adb07).

[Dev.to's FAQ](https://dev.to/faq) encourages you to cross-post articles published elsewhere on their site, too. So, if you like Dev.to and want to keep using it, why not blog on your own site, and publish there as well?
