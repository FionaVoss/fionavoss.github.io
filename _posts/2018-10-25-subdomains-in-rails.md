---
layout: post
date: '2018-10-25 17:11:00 -0700'
title: "Testing subdomains in Ruby on Rails, with and without lvh.me"
tags: 'Ruby'
---
Recently I was working on using subdomains in a Rails app. Basically, I needed to be able to look up a database record based on the subdomain, so I needed to be able to access the subdomain in my controller.

Domains and subdomains are one of those things where it's not immediately obvious how to test in development, since you can't just visit `http://sub.localhost:3000` and have it work without doing a little setup.

It took some searching to find all the info I needed, scattered across a few Stack Overflow questions and blog posts, so I'm posting it here to have everything in one place.

# Plan A: lvh.me

In the past, I've used [lvh.me](http://lvh.me), a domain that's pointed at localhost. If you have a local server running on port 3000, `http://lvh.me:3000` will get your server. It has a [wildcard DNS record](https://en.wikipedia.org/wiki/Wildcard_DNS_record), so `[anything].lvh.me` will point to localhost. [Here's some more info about lvh.me.](http://www.matthewhutchinson.net/2011/1/10/configuring-subdomains-in-development-with-lvhme)

This worked beautifully before, but unfortunately, for some reason I couldn't get it to work in the office this time. At home, it loads fine, so either I was making a stupid mistake, it was down temporarily, or some firewall was blocking it. Anyway, here's what I ended up doing instead:

# Plan B: editing the hosts file

First, I added `sub.localhost` to my hosts file following the instructions in [this blog post](https://codedecoder.wordpress.com/2018/03/01/subdomain-on-localhost-rails/).

In my Rails controller, I attempted to call `request.subdomain` to get the subdomain, but it was returning an empty string, while `request.domain` was returning `'sub.localhost'`.

From [this Stack Overflow answer](https://stackoverflow.com/a/31062044) I learned that I needed to add `config.action_dispatch.tld_length = 0` to `config/environments/development.rb`. Now, `request.subdomain` returns `'sub'` and `request.domain` returns `'localhost'`.

That answer linked to [this comment on a GitHub issue](https://github.com/rails/rails/issues/12438#issuecomment-25875656) which explains that `tld_length` refers to the number of dot-separated pieces of the TLD. The default is 1, for TLDs like `.com`. It would need to be 2 for TLDs like `.co.uk`.

# Subdomains in tests

Finally, in my Capybara tests, I used `Capybara.app_host = "http://sub.mydomain.com"` to fake the subdomain, as explained in [another Stack Overflow post](https://stackoverflow.com/questions/6536503/capybara-with-subdomains-default-host).
