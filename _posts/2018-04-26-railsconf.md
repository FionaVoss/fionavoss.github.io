---
layout: post
title: RailsConf 2018
tags: 
  - 'Tech Conferences'
date: 2018-04-26
---
Last week I attended RailsConf in Pittsburgh. It was my first tech conference and an all-around amazing experience. I left feeling grateful to work with Rails, and excited for its future.

I'm going to share some of the highlights below. The talks were recorded and you'll be able to watch videos eventually. To save you from having to read "You should watch the video!" every time, consider it implied. 😊

(Update: Videos are now available, so I've added links to the videos to all of the headings below!)

# The Scholar Program

RailsConf has scholarships for attendees who otherwise wouldn't be able to attend. In addition to free admission, scholars are paired with a guide, who helps them navigate the conference.

I applied to the scholar program because when I initially asked about attending Railsconf at work, the answer was maybe. When I found out that my company was going to fund my trip, I let the organizers know that I didn't need the scholarship, but I was still interested in having a guide. They included me in the program and treated me just like the rest of the scholars.

The scholar program *made* my RailsConf experience. My guide was amazing. She introduced me to lots of people, gave me advice on which talks to attend, made sure I had someone to eat dinner with, told me about her experiences in software development, and listened to mine. The other guides I met were all very welcoming and helpful, too.

On Monday night there was a reception for the scholars and guides. This allowed me to meet a lot of people and get some advice on how to make the most of the conference. We also received our badges and t-shirts, saving me from having to wake up extra early on Tuesday for registration. Some other nice perks included front-row seats for the keynotes, designated tables for lunch, and reserved slots for lightning talks (more on that later).

I thought the whole program was hugely successful at ensuring first-timers have a great conference. Many thanks to my guide and all of the organizers and guides for doing this.

# [David Heinemeier Hansson, Opening Keynote](http://confreaks.tv/videos/railsconf2018-opening-keynote-fixme)

In his keynote, DHH talked about "conceptual compression": the idea that high-level programming tools like Rails empower developers by allowing them to do more while knowing less. One of his main examples was how Rails's ActiveRecord mostly allows developers to avoid writing SQL. He made the argument that conceptual compression "arms the rebels", since solo developers and small teams are able to build entire applications. Conceptual compression is what made it possible for "full-stack developer" to be a thing, and for bootcamps to train developers in three months.

This resonated with me since I am a web developer and bootcamp grad who learned Rails first, and am studying computer science now. I am glad to be learning the fundamental, low-level concepts *now*, but I am equally glad that I learned Rails first. Knowing a high-level framework allowed me to become a productive developer really quickly, and gave me a big-picture view of software which means that gnarly things like assembly language make a lot more sense now that I'm learning them.

In fact, DHH's talk is what convinced me to do a lightning talk, which I was interested in doing but a little on the fence about. It also set the tone for the conference, since conceptual compression was a topic that came up again and again.

# [Gretchen Ziegler, "All Onboard: Cruising on the Mentorship"](http://confreaks.tv/videos/railsconf2018-all-onboard-cruising-on-the-mentorship)

Gretchen talked about how her company hired two high school students as interns. A former teacher, Gretchen applied what she knew about learning and designed a thoughtful program for them. One of her techniques was "backwards planning": she started with an end goal for the interns, which was to build a chat bot that would display some business information. She worked from there by considering what skills the interns would need to know and designing simpler projects to help them get there. It seems to have been a great success, since the company wants to hire more high school interns, and the two interns she talked about are both planning to study computer science in college.

I used to be a teacher too, so this talk was inspiring to me. Especially when working with junior developers, good managers must be good teachers, and I was glad to see this idea being shared and recognized. I was lucky to find a job as a new developer where I got the support I needed, but I think a lot of companies hire junior developers to save money and then fail to help them grow. Employers would help themselves and their junior developers by taking inspiration from Gretchen's talk.

# [Eileen Uchitelle, "The Future of Rails 6: Scalable by Default"](http://confreaks.tv/videos/railsconf2018-keynote-the-future-of-rails-6-scalable-by-default)

Eileen's keynote was a response to the common assertion that "Rails doesn't scale." She argued that Rails does scale, but it "doesn't scale easily... yet." Large companies like GitHub, where she works, have built solutions to make Rails scale better, but it took a lot of time and thought. Eileen went on to discuss how she wants to make these solutions part of Rails, so that developers at different teams don't have to come up with the same solutions independently.

Specifically, she talked about two things she's working on to make Rails 6 scale more easily. The first was better support for multiple databases, and the second was parallel testing so that tests can run more quickly and not slow down the development of large applications.

This dovetailed nicely with DHH's keynote by giving specific examples of how Rails can compress more concepts and make more things easy.

# [Pete Holiday, "The Code-Free Developer Interview"](http://confreaks.tv/videos/railsconf2018-the-code-free-developer-interview)

Pete started by explaining why he thinks having developers write code in interviews is not an effective assessment. Whiteboarding is stressful and not a realistic representation of the skills developers really need, while take-home assignments don't respect candidates' time and discourage a lot of qualified people.

Instead, Pete suggested two things. The first was a simulated code review: showing the candidate a pull request and asking them to review it as if you, the interviewer, had written the code. (He acknowledged that this exercise is not technically code-free; the point is that it doesn't involve *writing* code.) Compared to whiteboarding and take-home assignments, a code review shows more about what a developer will be like to work with, while still demonstrating their technical skills.

His second suggestion was a planning exercise: asking the candidate to describe how they would implement a feature or an MVP application. This is easily adaptable to different skill levels, since you can provide help if a candidate is struggling, or ask for more detail if they are doing great. Plus, it mimics what tends to be the hardest part of developing software, in my opinion.

I don't make hiring decisions, but I have been involved in screening interns. I think we could have benefited from these techniques. We didn't make the interns write any code, since we didn't think it would be a useful assessment, but I had a hard time thinking of what to ask them instead. I wouldn't do the mock code review with interns, but I would do the planning exercise.

# [Justin Collins, "The Evolution of Rails Security"](http://confreaks.tv/videos/railsconf2018-the-evolution-of-rails-security)

This talk was an overview of the major vulnerabilities that have been discovered in Rails, and how they were fixed. I started out with Rails 4, when a lot of these flaws had already been addressed, so this was eye-opening to me.

# [Cecy Correa, "Taking the Pain Out of Support Engineering"](http://confreaks.tv/videos/railsconf2018-taking-the-pain-out-of-support-engineering)

I found Cecy's talk surprisingly inspiring, and walked away feeling like I wanted to be a support engineer or manage a support team. At worst, support engineering is degrading, but at best, it's a job where every day is unique and you get the satisfaction of solving people's problems.

She suggested having dedicated support staff if possible, rather than having developers rotate support duties. If that's not possible, she recommended that whoever starts out with an issue see it through to resolution, even if the support rotation moves on to the next person, to maintain continuity. If an issue must be passed on to another team or developer, they should also be the one to communicate its resolution to the customer, for the same reason. And finally, Cecy recommended a zero-tolerance approach to abusive customers. She even showed an example of a customer who, after one warning, switched from angry and abusive language to polite communication.

# [Justin Weiss, "Building a Collaborative Text Editor"](http://confreaks.tv/videos/railsconf2018-building-a-collaborative-text-editor)

This talk was a demonstration of how to build a text editor similar to Google Docs, where multiple users can view and edit the same document at the same time on different devices. The problem was how to maintain a consistent result if User A edits the document after User B's changes hit the server, but before A receives B's edits. If we just send the entire document to the server, then B's changes will be erased by A's update.

So instead of sending the updated document to the server, we should send a representation of the change. If the document contains "cat" and I change it to "cart", then my client should submit something like:

```ruby
{ insert: "a", position: 2 }
```

In case we receive two updates to the same version of the document, we would need to implement some logic to decide which update takes precedence. Then, we would apply an algorithm to transform the second update in accordance with the first one.

This was one of those hard problems where I had never realized how complicated it was because I had never taken the time to think about it. I am glad I saw the talk, because now I know where to start if I ever need to build this kind of editor.

# [My lightning talk](http://confreaks.tv/videos/railsconf2018-lightning-talks)

RailsConf dedicates an evening to lightning talks, when anybody can talk for up to five minutes. There were more people who wanted to talk than there was time for, but I was able to talk because some slots are reserved for scholars.

I talked about my experience going back to school for a computer science degree as a professional developer. I wanted to share my experiences with other bootcamp grads and self-taught developers who are interested in formal CS education, especially because I'm sure a lot of people who might be interested don't know that programs like OSU's online CS degree exist. I explained that it is personally rewarding to learn things like assembly language, but I don't think everybody needs to learn it. New developers have to keep learning, but it doesn't have to be nitty-gritty computer science unless that's what you want to know.

My hope was that anyone who wanted to know more would come and talk to me afterwards. I didn't get as many bites as I had hoped for, but a few people told me it was useful to them.

One thing I wish I had done differently was to use slides. I didn't need bullet points, and I thought I was being smart by eliminating any potential AV problems, but I wish I had shown a few photos and a slide with my contact info at the end.

Still, I am really glad I did the talk! It was by far the biggest audience I have ever spoken in front of, which will make speaking at my local Ruby meetup feel like no big deal. I also did a practice run on stage with the other two scholars who did lightning talks, which was a really intense bonding experience. 😅

If you want to know more about my experience at OSU, you can find some posts I've written about it [on my Topics page]({% link topics.html %}).

# [Sarah Mei, "Livable Code"](http://confreaks.tv/videos/railsconf2018-keynote-livable-code)

The scheduled speaker couldn't make it due to the weather, and Sarah Mei filled in at the last minute. Nevertheless, her talk was incredible.

She talked about how construction is not a good metaphor for software development, even though it's often used as such. Buildings are a lot harder to change after they're built, and there is a clear distinction between the construction and maintenance phases. Software, on the other hand, is never really finished, and it's often maintained by the same people who built it.

So, Sarah explained, a better metaphor is furnishing and living in a house. When codebases get messy, it's not because developers enjoy living in filth. The real cause is a pattern of small bad decisions. If you neglect to do the dishes one night, it's harder to put the groceries away the next day because there's no room on the counter.

The huge refactor or rewrite that lots of developers dream of, Sarah explained, is like doing a massive declutter and reorganizing. The house might get clean, but it won't stay that way unless you actually change your habits. Making cleaning into a huge project feels productive, but simply doing the dishes every night is more important.

I think we do a pretty good job of this at my company. We rarely fall into the trap of making quick and dirty changes with the intention of cleaning up later. However, Sarah's talk was a good reminder to try to always leave the code better than I found it, rather than simply not make it worse.

# Betsy Haibel and Jennifer Tu, "Uncomfortable Refactoring"

Betsy and Jennifer walked us through adding some new features to some legacy code and refactoring using TDD techniques.

I was already familiar with the "red, green, refactor" pattern in TDD, where you write a failing test, make it pass by writing the smallest code change possible, and then refactor and repeat. However, they demonstrated some techniques that were new to me. During the "green" phase, they only *added* lines of code instead of removing or changing any. Then, during the "refactor" stage, they only changed one line at a time (maybe not exactly one line, but always one "idea"), running the tests after each change. Any time a test failed, they would undo the change and figure out a different approach. This is a good way to avoid falling down a rabbit hole of not knowing which change caused a test to break.

Another new-to-me technique was "defactor to refactor". This is when you un-DRY some code to get a clearer picture of what's going on before making changes, then DRY it up again in a hopefully more appropriate way. You might do this when you have two classes sharing similar logic, but find it awkward to add a third class because they're so tightly coupled.

# [Sasha Grodzins, "Build a Blog in 15 (More Like 30) Minutes: Webpacker Edition"](http://confreaks.tv/videos/railsconf2018-build-a-blog-in-15-more-like-30-minutes-webpacker-edition)

Sasha demonstrated building a blog using a React front end and GraphQL API. Previously, I had been of the impression that integrating React into a Rails app is tricky and that it's simplest to use two separate apps for your React front end and Rails back end. Sasha's talk demonstrated that with Webpacker, setting up React in a Rails app is relatively seamless. I haven't felt like I needed React for any of my projects yet, but if I need to build an app with a *lot* of front-end interaction, I might reach for it now.

# [Sumeet Jain, "Actionable Tactics for Leveling Up Junior Devs"](http://confreaks.tv/videos/railsconf2018-actionable-tactics-for-leveling-up-junior-devs)

I knew I was going to like this one when Sumeet said, "Mentorship skills are actively learned. They are not intuitive." My two favorite ideas from his talk:
* Focus on depth rather than breadth. It's better to spend a day deep-diving into a subject once a month than to spend a couple hours getting a shallow overview of a technology every week.
* Have junior developers write for an engineering blog. This will help cement what they've learned and identify gaps in their understanding. Senior developers should serve as technical editors.

# [Aaron Patterson, Closing Keynote](http://confreaks.tv/videos/railsconf2018-closing-keynote)

After an indescribably hilarious intro, Aaron gave a detailed explanation of some performance work he did at GitHub, including different types of profilers and when to use them.

At the end of three days of sleep deprivation and information overload, this was a lot to take in, so I'll have to watch the video when it comes out. Fortunately, he then said that performance tuning is something he wants to make easier, continuing the theme from DHH's and Eileen Uchitelle's keynotes. Perhaps a future version of Rails will include some powerful profiling tools so we can benefit from these ideas without knowing all the details.

# \# TODO

The hardest thing about attending RailsConf is deciding which talks to attend, since there are so many going on at once. Here are some that I missed, but look forward to watching when the videos are available:

* [Nick Quaranto, "The GraphQL Way: A new path for JSON APIs"](http://confreaks.tv/videos/railsconf2018-the-graphql-way-a-new-path-for-json-apis)
* [Mike Calhoun, "Continuous Deployments and Data Sovereignty: A Case Study"](http://confreaks.tv/videos/railsconf2018-continuous-deployments-and-data-sovereignty-a-case-study)
* [Ryan Laughlin, "The Doctor Is In: Using checkups to find bugs in production"](http://confreaks.tv/videos/railsconf2018-the-doctor-is-in-using-checkups-to-find-bugs-in-production)
* [Coraline Ada Ehmke, "Scaling the Software Artisan"](http://confreaks.tv/videos/railsconf2018-scaling-the-software-artisan)
* [Craig Buchek, "Booleans are Easy - True or False?"](http://confreaks.tv/videos/railsconf2018-booleans-are-easy-true-or-false)
* [Tess Griffin, "Keeping Moms Around for the Long Term"](http://confreaks.tv/videos/railsconf2018-keeping-moms-around-for-the-long-term)
* [Ryan Davis, "Minitest 6: test feistier!"](http://confreaks.tv/videos/railsconf2018-minitest-6-test-feistier)
* [Liz Certa, "Why We Never Get to Web Accessibility 102"](http://confreaks.tv/videos/railsconf2018-why-we-never-get-to-web-accessibility-102)
* [André Arko, "Pairing: a guide to fruitful collaboration 🍓🍑🍐"](http://confreaks.tv/videos/railsconf2018-pairing-a-guide-to-fruitful-collaboration)
* [David McDonald, "Dropping Into B-Trees"](http://confreaks.tv/videos/railsconf2018-dropping-into-b-trees)
* [Megan Tiu, "The Practical Guide to Building an Apprenticeship"](http://confreaks.tv/videos/railsconf2018-the-practical-guide-to-building-an-apprenticeship)
* [Todd Kaufman and Justin Searls, "Running a Business, Demystified"](http://confreaks.tv/videos/railsconf2018-running-a-business-demystified)
* [Michael Hartl, "Ten Years of Rails Tutorials"](http://confreaks.tv/videos/railsconf2018-ten-years-of-rails-tutorials)
* James Adam, "Here’s to the crazy ones"
* [Leonardo Tegon, "Warden: the building block behind Devise"](http://confreaks.tv/videos/railsconf2018-warden-the-building-block-behind-devise)
* [Geoffrey Litt, "Ruby: A Family History"](http://confreaks.tv/videos/railsconf2018-ruby-a-family-history)
* [Harisankar P S, "Using Databases to pull your applications weight"](http://confreaks.tv/videos/railsconf2018-using-databases-to-pull-your-applications-weight)
* [Vaidehi Joshi, "Re-graphing The Mental Model of The Rails Router"](http://confreaks.tv/videos/railsconf2018-re-graphing-the-mental-model-of-the-rails-router)
* [Graham Conzett, "Old-school Javascript in Rails"](http://confreaks.tv/videos/railsconf2018-old-school-javascript-in-rails)
* [Jordan Raine, "Ten years of Rails upgrades"](http://confreaks.tv/videos/railsconf2018-ten-years-of-rails-upgrades)
* [Claudio Baccigalupo, "Inside Active Storage: a code review of Rails' new framework"](http://confreaks.tv/videos/railsconf2018-inside-active-storage-a-code-review-of-rails-new-framework)
* [Ariel Caplan, "Automating Empathy: Test Your Docs with Swagger and Apivore"](http://confreaks.tv/videos/railsconf2018-automating-empathy-test-your-docs-with-swagger-and-apivore)
* [Derek Prior, "Up And Down Again: A Migration's Tale"](http://confreaks.tv/videos/railsconf2018-up-and-down-again-a-migration-s-tale)
* [Aja Hammerly, "Testing in Production"](http://confreaks.tv/videos/railsconf2018-testing-in-production)
* [Ross Kaffenberger, "Look Before You Import: A Webpack Survival Guide"](http://confreaks.tv/videos/railsconf2018-look-before-you-import-a-webpack-survival-guide)

# Final thought

I have caught the conference bug. I hope to attend many more in the future, both RailsConf and others.

People use the word "community" to describe the group of people who simply use the same technology, but Rails is a community in every sense of the word. I'm not saying that other technologies aren't, but Rails is something special.

It's not without divisions (see the RubyTogether controversy that cropped up the very day after the conference), but Rails is designed with clear values in mind, and it attracts people who share those values: putting people first, treating developers as humans, and making it easy to solve new problems instead of the same ones over and over again. I am grateful to be a part of it.
