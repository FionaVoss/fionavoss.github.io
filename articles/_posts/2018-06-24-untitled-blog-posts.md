---
layout: post
date: '2018-06-24 18:24:00 -0700'
title: 'Untitled blog posts were a game changer for my writing'
tags: Blogging
---
This is the story of how one small change&mdash;writing blog posts without titles&mdash;had a huge effect on my writing. It removed a ton of friction and helped me make writing a habit. If you are somebody who would like to blog because you have ideas you’d like to share with the world, but think the writing part sounds like too much work, I think this will be helpful to you.

# I thought writing had to be painful

If I had to describe the way I viewed the writing process when I started this blog in one word, the best would be “arduous”. I blame school. If you wanted to design a system to make young people hate writing, you couldn’t have done better than my education, from third grade through college. But that’s a story for another blog post.

The first few posts I published reflect this belief: they are long, heavily structured, and took me weeks to write. See for yourself:

* [Accelerated Introduction to Computer Science (CS 165)]({% post_url /articles/2018-01-07-intro-to-cs %})
* [Four Stages of Understanding Git]({% post_url /articles/2018-02-25-stages-of-understanding-git %})
* [One Month of Learning Elixir]({% post_url /articles/2018-03-07-learning-elixir %})

I didn’t start a blog because I thought the writing part would be fun. I did it because I was intrigued by [Jekyll](https://jekyllrb.com/) and wanted to learn the technology, and because I had just taken Intro to CS and thought that my take on the class would be helpful to other bootcamp grads and self-taught developers.

# What changed

I discovered [Micro.blog](https://micro.blog/). I decided to set up my blog for microblogging, and syndicate to Micro.blog and Twitter. When you see me [tweet](https://twitter.com/fionajvoss/status/1010753057599184896), that tweet was originally published [on my blog](http://fionavoss.blog/2018/06/23/18627).

At first, I thought that I would use microblogging just like Twitter, posting either long, titled posts, or untitled posts below 280 characters. If you read the post about [how I set up my blog for microblogging]({% post_url /articles/2018-04-01-microblogging-in-jekyll %}), you’ll see that I drew a bold line between these two types of posts, creating separate categories for “notes” and “articles”.

But one of the great things about Micro.blog is that it handles all post lengths reasonably. Untitled posts below 280 characters appear in the timeline fully. Longer untitled posts show an excerpt, with a link to the full post. Titled posts display only the title, with a link to the post. If you have cross-posting to Twitter turned on, they show up in Twitter the same way.

So I soon found that if a thought was a bit too long to be a tweet, it didn’t matter. I just kept writing. And my notes started getting longer and longer.

This changed the way I think about blogging. Before, I would save ideas for long posts. For example, I started keeping a running list of useful Ruby gems that I found, with the intention of eventually publishing a post with a title like “10 Cool Ruby Gems I Learned About This Year”. But now, I’ll just write about the gem the day that I find it.

The magical part is that since I write when inspiration strikes, and finish before inspiration dissipates, it feels like these posts write themselves. Examples: [this](http://fionavoss.blog/2018/06/07/8609), [this](http://fionavoss.blog/2018/06/05/14755), and [this](http://fionavoss.blog/2018/05/19/11647).

In response to Seth Godin’s recent call to blog daily, [CJ Chilvers wrote this](https://www.cjchilvers.com/blog/seth-godin-to-the-world-youre-still-not-blogging-daily?):

> Nothing has been healthier for my idea generation than to throw out ideas. Once they’re in the public, they feel completely gone. I’m free to come up with new and better ideas. And I do.
>
>When I don’t put those ideas out into the public, they fester. They cause uncertainty and anxiety. They kill the possibility of new and better ideas.
>
>Maybe I need to create the time, even at great cost, to blog more often if it means I can regularly free my brain of festering ideas. Maybe I shouldn’t say maybe: it seems like an invitation for this idea to fester.

Which rang very true for me. Blogging daily, or at least frequently, lets me move on to the next idea. But you can’t blog every day if you’re writing posts like [this]({% post_url /articles/2018-02-25-stages-of-understanding-git %})—not unless blogging is your full-time job. You can, however, publish posts like [this](http://fionavoss.blog/2018/06/07/8609) every day.

OK, time to address the irony of the fact that this post has a title:

# I’m giving more of my posts titles now

Now that I’ve internalized the lesson I learned from writing untitled posts, I’m starting to give more of my short posts titles.

Part of it is because of formatting. I use a lot of links, blockquotes, and other HTML formatting in my posts. Micro.blog strips the formatting from posts longer than 280 characters, because otherwise there would be problems with unclosed tags. This can [look confusing in the timeline](https://micro.blog/fiona/655667). It’s even worse on Twitter, because Twitter doesn’t respect hyperlinks. Even below 280 characters, [posts with more than one link](http://fionavoss.blog/2018/06/14/10999) [never come out the way I expect them to look](https://twitter.com/fionajvoss/status/1007459784021463040). Giving my posts titles solves the formatting problem.

But also, I’ve lowered my threshold for what kind of post “deserves” to have a title. I’m not elevating those long, arduously written posts above the rest of my writing anymore. Short posts that write themselves are allowed to have titles too. Examples:

* [TDD and "genius" programmers](http://fionavoss.blog/2018/06/22/tdd-and-genius-programmers)
* [How not to change a one-to-many association to many-to-many in Rails](http://fionavoss.blog/2018/06/20/how-not-to-change-rails-associations)
* [Stripping HTML from truncated content in Jekyll](http://fionavoss.blog/2018/06/03/stripping-html-in-jekyll)
* [Ruby methods are objects: a debugging tip](http://fionavoss.blog/2018/05/16/ruby-methods-are-objects)

The line between “articles” and “notes” isn’t as thick as it was for me before. I might change my site’s design a bit to reflect that. I might even go back and retroactively title some of my old posts.

If you’re reading this and you want to put what I’ve learned into practice, I suppose you could just write short, titled blog posts. But I don’t know if that alone would have the same magical, friction-erasing effect that writing untitled posts did for me. I encourage you to write your own untitled blog posts, at least for a while.

# But how?

Unfortunately, a lot of blogging software expects or even requires titles, so you’ll have to find one that doesn’t.

It’s pretty easy with Jekyll, but if you’re trying to reduce friction, you’ll probably want to set up a Micropub endpoint so you can publish without having access to a text editor and command line, as I’ve described [here]({% post_url /articles/2018-04-01-microblogging-in-jekyll %}).

I know people are doing this with Wordpress blogs, too.

But if you want to just start writing with a minimal amount of technical setup, I can’t recommend [Micro.blog](https://micro.blog/) highly enough. For $5/month they will host a beautifully designed blog for you. Posting is as easy as using Twitter or Medium, but you can write short and long, titled and untitled posts all in one place. They make it easy to add your own domain, or migrate to a different platform later on if you decide you want to use something else.
