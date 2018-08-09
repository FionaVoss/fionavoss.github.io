---
layout: post
date: '2018-07-01 16:21:00 -0700'
title: 'Pair programming, inclusion, and teaching people how to pair well'
tags: Programming
---
I'm going to PearConf! [PearConf](https://pearconf.splashthat.com/) is a conference dedicated to pair programming and inclusiveness. It's going to be held in San Francisco later this month.

Why go to a conference about pair programming? First of all, I love pair programming. We don't pair at my job, but we did every day at my bootcamp, [LEARN Academy](https://www.learnacademy.org/), and I loved it. I really enjoy how a good partner can help me when I get stuck, slow me down and ask questions that deepen my understanding of a concept, and make programming fun and social.

But I’m also interested in learning about the intersection between pair programming and inclusion.

# Wait, what?

I first became aware of this intersection when Sarah Mei [tweeted this in April](https://twitter.com/sarahmei/status/990594488052559874):

> Wondering why all the agile/XP stuff (like pairing, TDD, etc) doesn’t seem to work for a heterogenous team?
>
> It’s because they were developed by a bunch of white dudes. The practices assume the practitioners all have A LOT of built-in privilege.

I'll admit that I was surprised and confused at first. My own experience with pair programming at LEARN involved a diverse group of students, and it was overwhelmingly positive for me, and I believe pretty positive overall for the rest of my cohort.

Fortunately, she elaborated the next day in a [lengthy Twitter thread](https://twitter.com/sarahmei/status/990968833547497472), in which she explained how power dynamics--whether based on race, gender, experience, or other factors--can make pairing go badly for the person with relatively less power:

> For many years, I was a pair programming evangelist. Between that & my consulting work, I've met lots of people who tried pair programming and hated it. Some of them had paired for months, with different people, on different schedules, & still couldn't find a modality they liked.
>
> These people came from many different genders & races. Some were introverted; some weren't. What they all had in common wasn't obvious to me for a long time...until recently, it was.
>
> They're all usually on the downward side of one or more _power dynamics_ in their pairs.
>
> [...]
>
> Pairing has nothing to say about how to structure an interaction to avoid taking unfair advantage of power dynamics. One of its basic assumptions is that everyone feels empowered to contribute.
>
> When this is true, pairing is amazing. When it's not, it's a nightmare.

With those ideas in mind, I think it's worth exploring why pairing worked so well when I was at LEARN.

# Things that made pairing work (for me)

My cohort was diverse because it included people of different ages, genders, ethnicities, nationalities, and educational backgrounds (although it leaned white, Asian, male, and young). However, it was homogeneous in a very big way: experience.

LEARN is a code bootcamp, so by definition, we were all beginners at full-stack web development. Sure, some of us had more coding experience than others, but none of us were experts. So that minimized one potentially large power dynamic. If my first experience with pairing had been in the workplace, with me as a junior developer pairing with an experienced partner, I would have felt a lot less empowered to contribute, as Sarah Mei put it.

Also, I was at the privileged end of some big power dynamics relating to class, wealth, education, and access to technology. I grew up in the Silicon Valley, am the child of two former Apple engineers, attended private schools, have used Macs since I was a toddler and have had my own computers since I was ten. My parents bought me books on HTML and sent me to computer camp. I excelled in AP math and science classes in high school.

All of these factors made me feel confident in what I did know about coding and in my ability to learn what I didn't know yet. If I didn't have all of these privileges, I might have found pairing to be a less positive experience because I might have been afraid to look dumb or make mistakes. As a woman, I would have been more vulnerable to [stereotype threat](https://en.wikipedia.org/wiki/Stereotype_threat) if I didn't have all those other power dynamics working in my favor.

However, I think one very important reason that pairing worked at LEARN was that the instructors *taught* us how to pair program. On day one, before we students did any pairing, two instructors stood at the front of the room and demonstrated pair programming by writing a short program together. They taught us to choose a driver and a navigator, set a timer for 25 minutes, stick to our roles until the timer went off, and take a short break before switching roles. They generally encouraged us to take care of ourselves and take plenty of breaks, not specifically for the sake of pair programming, but it's certainly easier to be a considerate partner when you're well-rested.

# Pairing fails without instruction

The worst pair programming experience I've had was at a local meetup. I was in a group of three, and one of my partners didn't seem to understand that good pairing requires being fully present. He kept going off to work on his own laptop, and then coming back and interrupting us every few minutes. Fortunately it was only for an evening, so it wasn’t that bad, but I would have been miserable if I had to pair with somebody who did that at work.

Annoying, but I can't blame him entirely. We weren't given any instructions on how to pair at this meetup, and maybe it was new to him. Pair programming is a very different way of working compared to what most people know from work and school, and it's not reasonable to expect people to be good at pairing without any instruction.

# One attempt to teach good pairing

Back in May, I hosted an introductory workshop about Elixir. I gave a short [presentation](http://fionavoss.blog/slides/intro-to-elixir/) about the language, and then the participants broke into pairs to practice with [Elixir Koans](https://github.com/elixirkoans/elixir-koans).

Inspired by the recent discussions about how pairing can go wrong, I wanted to do what I could to ensure that everyone would have a good experience. So, I prepared a slide with the following pointers:

> Do:
>
> - Communicate
> - Take turns "driving" and "navigating"
> - Be patient
>
> Don’t:
>
> - Interrupt
> - Type without communicating
> - Grab the mouse or keyboard from your partner

When I got to this slide, I asked my audience to raise their hands if they had experience with pairing, and everybody did. (It wasn’t a huge crowd.) So, I didn’t spend much time talking about these guidelines, but I still went over them, as a reminder.

While the participants were pairing, it looked like everyone was contributing and enjoying themselves. I didn’t see anybody being bossy or patronizing, or any pairs where one person was doing everything.

Now, if I hadn’t presented any guidelines, maybe the workshop still would have gone just as well. I'm sure that the participants' prior experience pairing had a larger impact than the two minutes I spent talking about it. Still, I will definitely be doing this again the next time I lead any event that involves pairing. Next time, there may be people who have never paired before. Or maybe they’ve only had bad experiences pairing, and this is a chance for them to experience pair programming done well for the first time.

# What I'll do differently next time

While the Elixir workshop was a success, I did see one pair that wasn’t functioning great. One of the participants was not fully engaged with his partner. He was switching between their shared computer and his own laptop, so he basically kept abandoning his partner to work on his own every few minutes. It looked a lot like my own experience that I described above.

In the context of a one-evening workshop, I don’t care if individuals pair or not, but I do want everybody who pairs to have an excellent partnership. So, I think next time, I will emphasize that participants are free to pair or not pair as they see fit, but if they do, they *must* follow the guidelines, unless they and their partner agree to do things differently. I might call them "rules" instead of "guidelines". I'll also make it clearer that pairs should only be using one computer.

It's probably a good idea to discourage participants from using their own laptops too, if possible. In another tweet, [Sarah Mei said](https://twitter.com/sarahmei/status/877732773267611648):

> If your pair programming is on a computer where one of you is the "owner" and one of you is the "guest," it's not actually pairing.

At LEARN, there are computers available, so if I lead another workshop there, I may add a rule that if participants pair they must use the LEARN computers, and if they want to use their own laptops then they must work solo. If we're in a situation where people have to use their own laptops, perhaps the rule will be that the person who *doesn't* own the computer must drive first.

# Goals for PearConf

PairConf is going to follow the “unconference” format, so I don’t know exactly which topics will be discussed, but I am interested in discussing how we can teach people to pair better, and ways to make pair programming successful not just in the workplace, but also in other scenarios, like my Elixir workshop.

In [Sarah Mei's thread starting here](https://twitter.com/sarahmei/status/991023062802837504), she provided some excellent guidelines for how to neutralize power imbalances when pairing.

I think these guidelines are great for a workplace or a medium-to-long-term educational setting like a bootcamp. But since they involve some subtle concepts, and take time to study, I would like to distill them a bit for short-term situations like a one-evening workshop, where we only have a minute or two to talk about how to pair.

# Further reading

If you want to hear more about these ideas, definitely read the full Twitter threads I linked to, because I only quoted a few parts.

I also recommend listening to the Tech Done Right podcast's episode on [diverse agile teams](http://www.techdoneright.io/38). It features Marlena Compton, the organizer of PearConf, and Betsy Haibel and Jennifer Tu, who are leading a workshop there.
