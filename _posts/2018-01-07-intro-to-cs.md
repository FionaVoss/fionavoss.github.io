---
layout: post
title: Accelerated Introduction to Computer Science (CS 165)
tags: OSU
redirect_from: /articles/2018/01/07/intro-to-cs.html
---
This past fall, I took CS 165: Accelerated Introduction to Computer Science, online from Oregon State University. It was my first course as a student in [OSU's post-baccalaureate computer science program](http://ecampus.oregonstate.edu/online-degrees/undergraduate/computer-science/), through which I'll be earning my second bachelor's degree over the next 2-3 years.

When the course started, I had been working as a Rails developer for just over a year after finishing [LEARN Academy's web development bootcamp](https://www.learnacademy.org/). I was experienced at programming in Ruby and JavaScript, but I had no experience with C++, the language used in this course, and no other formal CS education.

In this blog post, I'll describe my experience taking the class as a professional web developer and bootcamp grad. It will help new and prospective OSU students know what to expect from CS 165, but since introductory CS classes will cover a lot of the same material no matter where you study, I think it will also help other bootcamp grads decide whether they want to take a similar class from any other university or college.

## Course structure

The course was an introduction to programming in C++, covering the following topics:

* Data types
* Conditionals, loops and functions
* Classes and object-oriented programming
* Arrays and vectors
* Pointers and dynamic memory allocation
* Searching and sorting algorithms and Big O notation
* Recursion
* Class templates and the Standard Template Library
* Linked lists, stacks, and queues
* Makefiles

We had a textbook and video lectures. I always did the reading, but only watched a few of the videos, in order to review trickier subjects before the exams. Personally, I didn't find the videos very helpful, but I just don't like learning from videos.

The majority of our grade, and time commitment, came from weekly coding assignments. These assignments ranged from single functions to multi-file programs: my last project included 14 files and 6 classes. We submitted them to Mimir, an auto-grading platform. Mimir would run several tests on each assignment, but all but one were hidden until after the deadline, so we were responsible for testing our own code. Since different compilers have different settings, we were advised to upload our code to the school's server and compile and run it there to ensure that we tested in an environment identical to Mimir's. This was convenient for me, since I didn't need to install anything on my Mac except FileZilla for uploading my files.

There were two multiple-choice exams, which mostly consisted of reading code snippets and predicting their output. Exams had to be proctored. We had the option of using a local in-person proctor, or the online service ProctorU, which is what I used.

We also had a few written assignments, including two group projects. Both required us to compare our work on a previous assignment with other students, decide whose was best, and explain why.

## What it was like for me

The first few weeks were easy for me, since we were covering concepts that were already familiar to me from Ruby and JavaScript. There was a lot of assigned reading, but fortunately I was able to skim the text, just looking for ways that C++ differs from those languages. Aside from minor syntax differences, the main difference was the fact that C++ is statically typed, but I found that easy to get used to, as was the extra step of compiling. At this stage, I found most of the code assignments pretty easy, and I could finish all of the assignments for the week in one or two evenings.

As we moved on to topics that were new to me--pointers, dynamic memory allocation, and operator overloading--the course became challenging, but still manageable for me while working full time. The amount of assigned reading decreased, which was fortunate because I had to read carefully now instead of skimming. For the code assignments I needed at at least 3-4 evenings, and there were times when I got pretty frustrated by errors that took a long time to figure out, but as long as I left myself enough time, I was fine. I managed to score 100% on all of the assignments except for one, which I attribute entirely to insufficient testing due to running short on time.

The exams were challenging in a different way. Most of the questions involved reading a bit of code and predicting its output, and they weren't simple. I was not as confident about my answers as I was about the code I wrote, since I could run my code and verify the output, but on the exam, I was only allowed to use a white board as scratch paper (since ProctorU doesn't allow actual paper). I got an A on the first exam and a B on the second one, and since I had a solid average from the code assignments, my final grade was an A.

The group assignments were okay. I had good groupmates and I liked being able to see their code, but the writing assignments were a bit tedious. Better than the enforced collaboration of the group assignments was the volunatary interaction on the unofficial student Slack group, which is an amazing resourse. Being on Slack made the course feel a lot more social and fun, and is a big part of why I enjoyed the class so much.

## What I got out of it

I am really glad I took this course, and I got more out of it than I expected. When the course started, I was looking forward to learning a new language, but I didn't realize how relevant the concepts would be to my work in Ruby. For example, pointers are something that Ruby uses behind the scenes. While you don't directly interact with pointers, they do [have implications for Ruby developers](https://stackoverflow.com/a/7210058/8238305). I was always surprised when a value I didn't expect to change would change, until I learned about pointers in this class.

I am also glad that I got experience working with a compiled and statically typed language. Recently I learned about [Crystal](https://crystal-lang.org/), a new language with a syntax similar to Ruby, but which is compiled and includes optional static typing. Since I had already been working with C++, this idea was very exciting to me, which it wouldn't have been a few months ago. I now understand more about the advantages and disadvantages of different programming languages.

Taking this course has made be appreciate Ruby a lot more, and I definitely prefer programming in Ruby over C++. I wouldn't start a new project in C++ without a good reason for choosing that language, but I could contribute to an existing C++ project now.

## My advice to other bootcamp grads

A lot of intro to computer science courses teach C++, and if they don't, they should still cover a lot of the same topics as OSU's 165 does, so this advice applies whether you're studying at OSU or somewhere else.

I would strongly recommend taking an intro to CS course to other bootcamp grads. If you're a Ruby or JavaScript developer, it's a great way to get a taste of how computers work on a lower level than what you're used to. If you have no plans of pursuing a degree and don't need academic credits, [Harvard's CS50x](https://www.edx.org/course/introduction-computer-science-harvardx-cs50x) is a free option that I've heard great things about. If you are interested in pursuing a degree, I am very happy with my experience at OSU so far.

If you do decide to take an intro to CS class, be prepared to be challenged. The first few weeks of the course will be easy for you, but after that, the course will move on to topics that will probably be new to you. I found the level of difficulty manageable, and I never felt very stressed while taking this course, but I wouldn't call it easy.

One specific thing I would do differently if I could take the class again is learn an automated testing framework for C++ early on. I tested everything by printing values and checking them manually, which worked fine, but got unwieldy during the later weeks. However, by the time I started wishing I knew a test framework, my workload was heavy enough that I didn't want to invest the time to learn one.

## Some advice specific to OSU students

If you are an experienced programmer, you should almost certainly take 165 rather than 161 & 162, unless you specifically want to get really good at C++. Both options cover the same concepts, but according to other students, 162 is actually more work because you need to write a lot more code. That extra practice is necessary for beginners, but if you're already a confident programmer, you can save a lot of time by taking 165.

If you're an experienced programmer working full time, CS 165 on its own is a good workload. I had to put in a few hours most days, but still had time for a personal life. I could have fit in another 4 credits and lived, but I'm glad I chose not to.

On the other hand, if you are a beginner, I would strongly recommend taking 161 and 162 instead, because you do need that extra practice. If you do take 165, be prepared to devote a lot of time to it, up to 40 hours a week.

Either way, do get the textbook, and use the review questions to study actively. The questions where you have to predict the output or spot the errors are especially good preparation for the exams.

Finally, follow the instructors' advice to compile and test your code on Flip. There were students in my section who tested locally, and got burned when they passed the visible Mimir tests but failed hidden ones due to differences between the two environments.

## What's next for me

When this course started, I was undecided about whether I wanted to complete the entire degree program. However, I learned a lot in this class, and I am looking forward learning more. So, I plan to continue working towards a second Bachelor's degree in computer science with OSU.

The winter quarter starts tomorrow and I'll be taking Discrete Structures (because it's a prerequisite for further classes) and Web Development (because it's a required course and this is a good time to get it our of the way, but it will also me an opportunity to learn about Node.js). Later on, I'm looking forward to taking more advanced CS courses in assembly language, operating systems, and more.
