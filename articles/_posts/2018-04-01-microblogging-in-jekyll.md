---
layout: post
title: Microblogging in Jekyll
redirect_from: /articles/2018/04/01/microblogging-in-jekyll.html
tags: Jekyll
---

A microblog is a blog that features short, usually untitled posts. Until recently, I thought that Twitter and Tumblr were the only ways anybody microblogged nowadays. Turns out, there is a vibrant community of [IndieWeb](https://indieweb.org/) enthusiasts microblogging on their own websites. So lately, I've been setting up my own site for microblogging.  

I've added a [Notes]({% link notes.html %}) page for microposts and an [Articles]({% link articles.html %}) page for my longer posts, while my [home page]({% link index.html %}) shows both types of posts. I can easily post to my Jekyll blog from anywhere using my phone, and my posts automatically get cross-posted to Twitter.

(Note: I have made some changes to my site since I published this post, so the paragraph above is a little out of date.)

Why do this? Microblogging on my own site gives me more flexibility than using Twitter. I don't have to obey Twitter's character limits and I can mark up my posts however I want. I control the design of my own site, and I choose whether it has ads or not.

Since I cross-post to Twitter, I can stay connected to people who are there, but if I ever decide I want to leave Twitter, I can delete my account without losing my posts or worrying about how to export them in a format I can do something with. And right now, people can follow me without having a Twitter account, using RSS or Micro.blog.

Here's how I set my blog up to accomplish this:

## Jekyll Setup

I was using a Jekyll theme called [Lanyon](https://github.com/poole/lanyon), but decided to switch back to the default theme, Minima, because I like the navigation better. Minima is a gem-based theme, so where I wanted to customize the appearance of my site, I had to copy layout files from the gem into my source code [as shown here](https://jekyllrb.com/docs/themes/#overriding-theme-defaults).

Here's the markdown file for one of my notes. It's a standard Jekyll post, except for the fact that it has an empty string for a title. If I removed that line, Jekyll would title the post based on the slug, which in this case is "343". Not pretty.

```md
---
layout: post
date: '2018-03-25T00:05:43.780Z'
title: ''
slug: '343'
---
Posting to my Jekyll site from my phone using the Micro.blog iOS app. Now I’m ready to rep the indie web at RailsConf!
```

I am using Jekyll's category feature to differentiate between articles and notes. Jekyll automatically assigns the category based on the file path, which in my case is either `articles/_posts` or `notes/_posts`. I created my Notes and Articles pages based on [this example from the Jekyll docs](https://jekyllrb.com/docs/posts/#displaying-post-categories-or-tags).

My homepage, which shows both types of posts, doesn't know anything about categories; it just shows all posts. To prevent empty `<h3>` tags from creating excess whitespace for posts without titles, the template checks if the title is an empty string. Not elegant, but it get the job done.

```md
{% raw %}{%- if post.title != "" -%}
  <h3>
    <a class="post-link" href="{{ post.url | relative_url }}">
      {{ post.title | escape }}
    </a>
  </h3>
{%- endif -%}{% endraw %}
```
If the post is an article, we show an excerpt (the first paragraph, by default) with a link to read more. If it's a note, we show the entire content.

```md
{% raw %}{%- if post.categories contains 'articles' -%}
  {{ post.excerpt }}
  {% if post.content contains site.excerpt_separator %}
    <a href="{{ post.url | prepend: site.baseurl }}">Read more</a>
  {% endif %}
{% else %}
  {{ post.content }}
{%- endif -%}{% endraw %}
```

On line 3, `if post.content contains site.excerpt_separator` ensures that we only show the "Read more" link if there is actually more content than what's displayed. In practice, it's not really necessary since all my articles have more than one paragraph. But in theory I could write a long post without a title, or a short post with one, and it will be displayed reasonably whether it's in "Articles" or "Posts", since the display logic has nothing to do with which category a post belongs to.

## POSSE with Micro.blog

[POSSE](https://indieweb.org/POSSE) stands for Publish (on your) Own Site, Syndicate Elsewhere, and its goal is to give you the best of both worlds: owning your content by publishing on your own website first, while still connecting with others on social media. This was the easiest part for me to set up because it's powered by the service [Micro.blog](https://micro.blog/), which is kind of like a smaller, friendlier, better Twitter.

With Micro.blog, you can make an account and syndicate posts from your own blog's RSS feed to your personal Micro.blog feed. Short, untitled posts will appear in their entirety, like tweets. Longer posts will be displayed as excerpts or titles, with a link to the full post on your blog. Other micro.blog users can follow you and reply to your posts in the Micro.blog app. [Here's how my feed looks.](https://micro.blog/fiona)

I am really enjoying the Micro.blog community. It feels a lot more human and less commercial than Twitter. The platform is totally ad-free, and the feed is strictly chronological. Since the community is small, it's easier to keep up with, and I think more people see my posts than on Twitter. Even though there are fewer people, I have more conversations in Micro.blog.

Micro.blog also allows me to stay connected with people who are on Twitter, because it automatically cross-posts my feed there. This part costs $2 a month.

Micro.blog will also host a blog for you for $5 a month. This is a good choice if you don't want to set up and maintain your own site, or if you already have a blog but want to keep your microblog separate.

## Publishing

Micro.blog has their own macOS and iOS apps, which can post to your blog if your site supports Micropub. Micropub is a specification for a standard way of posting to a site that works with a variety of client apps. If you're blogging on a dynamic site, you would set up an API endpoint to receive POST requests in a specific format. If you're using WordPress, which seems to be the most popular choice with IndieWeb people, there are plugins for it.

Since I'm using Jekyll, a static site generator, I thought Micropub would be hard to set up, but fortunately there's a great tool for doing exactly this: [webpage-micropub-to-github](https://github.com/voxpelli/webpage-micropub-to-github). This is an app that creates a Micropub endpoint for Jekyll sites hosted on GitHub pages.

First I had to add some code to the `<head>` of my site for authentication purposes:

```html
<link rel="authorization_endpoint" href="https://indieauth.com/auth">
<link rel="token_endpoint" href="https://tokens.indieauth.com/token">
<link href="https://twitter.com/fionajvoss" rel="me">
<link href="https://github.com/FionaVoss" rel="me">
```

The first two lines tell Micropub what authentication service to use, and the last two lines are to connect my social media accounts to my website so I can sign in with [IndieAuth.com](https://indieauth.com/). Either Twitter or GitHub would have been sufficient; I don't actually need both links. I also had to add my site's URL to my GitHub and Twitter bios.

webpage-micropub-to-github is self-hosted, so the next step was to deploy my own instance of the app. All I had to do was click the "Deploy to Heroku" button in the [README](https://github.com/voxpelli/webpage-micropub-to-github/blob/master/README.md) and configure a few variables, including my GitHub username, API key, and repository name. I forked the repo but is wasn't necessary since I didn't need to make any code changes.

Once small gotcha: to configure the optional `MICROPUB_LAYOUT_NAME` variable, I had to enter the value, `"posts"`, in quotes; without quotes it broke the app. Same thing with `MICROPUB_FILENAME_STYLE`, which I set to `"notes/_posts/:year-:month-:day-:slug"` to make my posts go into the "Notes" category.

Once that was deployed, I had to link to the app in my `<head>` to tell Micropub where to submit posts:

```html
<link rel="micropub" href="https://jekyll-micropub-to-github.herokuapp.com/micropub/main">
```

Finally I had to add my website URL in my Micro.blog preferences and go through the IndieAuth authentication process, which basically entailed signing in to my Twitter account.  

When I post, Micro.blog sends a request to webpage-micropub-to-github. Then webpage-micropub-to-github formats the post as a markdown file appropriate for Jekyll, and adds the file to my site repository through the GitHub API. Since GitHub pages rebuilds my site every time there is a commit to master, the post shows up right away.

Having Micropub set up means that I can not only use the Micro.blog apps to post, but a variety of others as well. Another one that I've tried is [Quill](https://quill.p3k.io/). Since it's browser-based, it's convenient for posting from a shared computer without having to install anything. To post from my phone, I use Micro.blog.

Although the setup was fairly involved, posting to my blog is now as fast and easy as tweeting, which is the missing puzzle piece that makes Microblogging with Jekyll totally feasible.
