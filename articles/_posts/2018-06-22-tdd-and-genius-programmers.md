---
layout: post
date: '2018-06-22 20:07:00 -0700'
title: "TDD and \"genius\" programmers"
tags:
  - 'Software Engineering'
---
The way I usually explain automated software tests to people who aren’t familiar with them is that if you write a test for the thing you're working on *now*, it will let you know when you accidentally break it *later*, before the bug gets into production.

This describes how tests can be a part of QA, but not how they can be a part of the development process.

I’ve been working on a complicated feature for several weeks and I don’t think I could have done it without using TDD. The requirements are just too complex for me to hold them all in my head at once.

Last month, Sarah Mei [tweeted about how "genius" programmers can be at a disadvantage](https://twitter.com/sarahmei/status/999901279559139328) because they aren't forced to learn the techniques that non-geniuses rely on:

>Sometimes I think that people who can hold complex systems entirely in their heads - classic ‘genius’ programmers, clearly the type this author is - are actually at a disadvantage these days.
>
>At some scale, even _they_ run out of brainspace, and then they don’t have the habits people like me developed early on - by necessity - to carve out spaces where we didn’t _have_ to hold it all in our heads.

TDD is a tool that lets non-geniuses build complicated software when the requirements are too sprawling to hold everything in your head at once. When things get really hairy, the non-genius who is skilled at practicing TDD may be more effective than the genius who can get by without it.
