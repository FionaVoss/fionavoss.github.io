---
layout: post
date: '2018-06-03 14:50:00 -0700'
title: 'Stripping HTML from truncated content in Jekyll'
tags: Jekyll
---
When I started writing this post it was going to be a request for debugging help, but in the process of writing it I solved my own problem. (Don't you love it when that happens?) Since I had already written half a blog post, I decided to share the solution here for posterity.

# Background

Previously, I was only tagging my [articles]({% link articles.html %}), but I wanted to organize my [notes]({% link notes.html %}) by tag as well. I created a new page to list [articles and notes by topic]({% link all-posts-by-topic.html %}), and if you scroll down to the bottom of this page, you'll see a list of articles and notes tagged 'Jekyll'.

Since notes don't have titles, I am displaying the first 80 characters of the post body. Since the body sometimes contains HTML, I am stripping the HTML to prevent unclosed HTML tags from wreaking havoc on my layout.

# The problem

I was using using the same code to display truncated post content in two different places:

```liquid
{% raw %}{% if post.title == "" %}
  {{ post.content | strip_html | truncate: 80 }}
{% else %}
  {{ post.title }}
{% endif %}{% endraw %}
```

But the Markdown formatting was not getting stripped consistently.

On [the topics page]({% link all-posts-by-topic.html %}) ([source code here](https://github.com/FionaVoss/fionavoss.github.io/blob/master/all-posts-by-topic.html)) one post showed up as:

> Current goal: Finish On Fire With Phoenix before Code School goes bye-bye on ...

While on [an individual post's page]({% post_url /notes/2018-03-04-01 %}) ([source code here](https://github.com/FionaVoss/fionavoss.github.io/blob/master/_layouts/post.html)) it looked like:

> Current goal: Finish [On Fire With Phoenix](https://www.codeschool.com/course...

# The fix

Googling led me to a distantly relevant [GitHub issue about the Minimal Mistakes theme](https://github.com/mmistakes/minimal-mistakes/issues/719) where I saw that they were calling `markdownify` before `strip_html` to display truncated content.

I added `markdownify` to my code to see what would happen, and it worked! So now I have:

```liquid
{% raw %}{% if post.title == "" %}
  {{ post.content | markdownify | strip_html | truncate: 80 }}
{% else %}
  {{ post.title }}
{% endif %}{% endraw %}
```

And the Markdown formatting gets stripped in both places.

# The takeaway

I don't know why, but it seems that `post.content` was automatically being converted from Markdown to HTML on the first page but not on the second. Perhaps it's because the first file is a page while the second one is a layout?

 Anyway, `strip_html` only strips HTML, so the unconverted Markdown was not getting stripped. Calling `markdownify` converts from Markdown to HTML so that `strip_html` can do its job.
