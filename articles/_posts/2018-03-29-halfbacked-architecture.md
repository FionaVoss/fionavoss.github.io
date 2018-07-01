---
layout: post
date: '2018-03-29T01:16:46.956Z'
title: 'Halfbaked architecture'
permalink: /notes/2018/03/29/4606.html
tags:
  - 'Static site generators'
---
*<strong>Update:</strong> This post was originally published without a title. The name "halfbaked" [was suggested](https://micro.blog/kwlblt/436679) by Micro.blog user [@kwlblt](https://micro.blog/kwlblt).*

I&#39;m pretty happy with Jekyll for my personal site right now but I&#39;m itching to try this static-dynamic hybrid approach: Blog is a Rails app. It only has interfaces for displaying posts, not writing or editing. We have a Micropub endpoint for publishing.

All views are public, so we cache *every* view. We don&#39;t worry about cache invalidation; anytime we change *anything* in the database, we just blow away the entire cache. But we don&#39;t build the entire site at once; Rails controllers build and cache pages as they are requested. Once cached, a page is served as a static HTML file.

We have all the benefits of a static site generator in a [Majestic Monolith](https://m.signalvnoise.com/the-majestic-monolith-29166d022228) that could handle commenting and even accept Webmentions. The most magical part? The more traffic the site gets, the faster the average page load will be (to a point) because users are more likely to hit a cached page.

Please help me name this or I&#39;ll have no choice but to call it &quot;stanamic” architecture.
