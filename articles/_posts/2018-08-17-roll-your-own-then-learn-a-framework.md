---
layout: post
date: '2018-08-17 19:36:00 -0700'
title: 'Roll your own, then learn a framework'
tags: Teaching
---
Today a coworker and I were researching two popular authorization frameworks ([Pundit](https://github.com/varvet/pundit) and [CanCanCan](https://github.com/CanCanCommunity/cancancan)) in order to decide which was the better choice for one of our applications.

Both of us attended the same bootcamp, [LEARN Academy](https://www.learnacademy.org/), before we worked together, so we got to talking about our experience learning CanCanCan there.

My coworker said that he had been a little confused at the time, and I think I was too. Part of it was just being new to Ruby on Rails in general, but I think another reason I was confused was that it was my first time implementing any form of authorization, and I was doing it with a pretty expansive library that abstracted away a lot of the logic.

In retrospect, I think it would have been slightly better if we had first learned about authorization by writing our own from scratch, and only then learned to use a gem like CanCanCan.

This is a pattern I’ve seen a lot in the context of learning to code, and I think it’s really effective: learn to do something from scratch first, then learn a popular library for doing the same thing. You will understand a problem much better if you try to solve it on your own first than you will if you are just handed a solution.

A really simple example is that when we were first learning JavaScript at LEARN, we wrote our own own functions to map and filter arrays before we learned the built-in functions for doing so.

I learned of another example from [Ariel Caplan on Twitter](https://twitter.com/amcaplan/status/991404232946388993):

> At @FlatironSchool we built a crummy version of every abstraction layer before using it, e.g. built a simple ORM before starting to use ActiveRecord.

If you took this idea to its logical extreme, you’d write an entire application framework before learning a popular one like Rails. This is too ambitious to be practical, but a friend who attended Dev Bootcamp told me that they learned Sinatra&mdash;a simpler Ruby framework which does a bit less for you&mdash;before Rails. If you took this approach, you could then guide your students through writing some functionality that Rails has but Sinatra lacks, then show them how to do the same thing in Rails.

I also have an inkling that the same technique could be really effective for teaching a front-end framework like React, although being a beginner to React I'm not entirely sure how you would do this.

# Bridging the gap between code bootcamps and CS degrees

As somebody who attended a bootcamp and is now [studying computer science at a university]({% post_url /articles/2018-07-08-why-back-to-school-for-cs %}), I think that both types of institutions could improve their teaching by applying this principle more often&mdash;but for opposite reasons.

Universities are criticized for teaching too much theory and not enough practical skills. If they spend the majority of their time on the low-level concepts, but take a little time to expose students to popular libraries for accomplishing the same goals at the end, graduates will have the skills to work on real-world projects while getting the same strong theoretical foundation.

This technique can also make it easier for universities to keep their courses up-to-date in the rapidly-changing world of software engineering, since the lessons about building things from scratch&mdash;which is what they should spend the majority of their time on&mdash;will have more longevity. But when React is usurped by some other framework, that part of the course can be swapped out relatively easily.

Bootcamps, on the other hand, are criticized for producing technicians as opposed to engineers, who can put code together like Lego blocks but don’t understand what's going on behind the scenes. If they teach their students how to do more things from scratch&mdash;even in a very basic way&mdash;then bootcamp grads will have a deeper understanding of software development, and be prepared for when the popular libraries aren't flexible enough to do what they need.

# Does this technique work for self-teaching?

I wrote this post with people who teach others to code in mind. I think it's trickier to apply this technique when you are teaching yourself, but still doable. If you're feeling adventurous, go ahead and try to build your own authorization system from scratch. If it gets too frustrating, it's fine to just dive in with CanCanCan.

For a little more guidance, you could seek out tutorials that teach you how to do the thing you want to do from scratch. Or, switch up the order: learn the library first, and when you feel comfortable, try rolling your own.
