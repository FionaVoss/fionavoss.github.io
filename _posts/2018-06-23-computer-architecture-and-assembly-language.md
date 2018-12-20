---
layout: post
date: '2018-06-23 21:32:00 -0700'
title: 'Computer Architecture and Assembly Language (CS 271)'
tags: OSU
excerpt_separator: <!--more-->
---
I recently finished my third course at OSU, Computer Architecture and Assembly Language (CS 271).

If you're wondering what assembly language is, I'll say more on that later, but essentially it's about as low-level as you can reasonably get with programming&mdash;one step up from writing machine language. It's not terribly practical for the vast majority of software developers today, but writing assembly teaches you a lot about how computers work.

<!--more-->

# Course structure

The course covered assembly programming for the [Microsoft Macro Assembler (MASM)](https://en.wikipedia.org/wiki/Microsoft_Macro_Assembler) and some theoretical concepts. The programming techniques and MASM features that we used included:

- Data representation
- Conditions & control structures
- Repetition structures
- Procedures
- Passing parameters on the system stack
- Arrays
- Converting strings to integers and vice versa
- Macros

While concepts that we were tested on, but didn't write programs with included:

- Binary arithmetic and converting between binary, decimal, and hexadecimal
- Byte ordering
- Floating-point representation & operations
- Hamming codes
- Multi-dimensional arrays
- Recursion
- Digital logic circuits
- Parallelism

There were six programming assignments total, with one due every two weeks.

Every week, there was some assigned reading, about an hour's worth of video lectures, and a "summary exercise"&mdash;basically an open book quiz, except you would get a 6-hour window to finish it when you definitely didn't need 6 hours.

Every two weeks there would also be a "quiz"&mdash;also open-book, but with a much shorter time frame.

There were two proctored exams, a midterm and a final. Like the summary exercises and quizzes, the exams were a mix of multiple choice and free-answer sections, including a lot of code tracing. Also, each exam had a section where you had to write actual code (without the benefit of being able to run and test it 😭).

# What I liked

The requirements are very clear. A detailed rubric is provided for each of the programming assignments before it is due, so it's easy to predict exactly how many points you'll earn. The exams are similar: the questions are not easy, but all the topics are covered in the lectures and the questions are similar to the ones on the practice exams. The grading is very fair.

Also, I think the breadth and depth of the topics covered is just about perfect. Most OSU post-baccalaureate graduates are going to end up working as software engineers, and very, very few of us will need to write assembly, so we don't need too much depth, but the degree is called "Computer Science", not "Software Engineering", so we do need to know a bit about low-level fundamentals.

# What could have been better

For one, the textbook and lectures are *very* dry. I would like to see OSU redo the lectures to make them more engaging.

Also, I think the programming assignments could be better [scaffolded](https://en.wikipedia.org/wiki/Instructional_scaffolding). There was a major ramp-up in complexity from Program 4 to Program 5, due to a lot of new topics being introduced at once, and it doesn't have to be that way. Instead of 6 relatively large programming assignments due every two weeks, I'd rather see 10-12 smaller assignments due every week, so that fewer new topics can be introduced at once.

Finally, there was one part of the syllabus that really bugged me:

> The class grade is divided such that you can be either a really good programmer or a
really good test taker and do okay in the class. If you are a really good with the
programming, but do poorly on tests, you can still succeed in the class. If you are
great with tests, but crummy at coding, again, you can succeed in the class. If you are
good at both, you’ll excel.

First of all, this doesn't make a lot of sense because both of the exams require you to write *actual code*, and it's worth a significant number of points.

But more importantly, I really hate to see a course in a program designed to *train future software engineers*&mdash;especially one that's usually taken pretty early in the program&mdash;adopt what is essentially a [fixed mindset](https://en.wikipedia.org/wiki/Mindset#Fixed_and_growth) toward coding abilities. They should not be saying "If you're crummy at coding, that's OK." They should be saying, "If you're not great at coding, we will help you get better."

# My experience

If you read my blog post about [Discrete Structures (CS 225)]({% post_url /2018-03-30-discrete-structures %}), you might remember that I wrote this:

> I enjoyed learning C++ a lot because it helped me understand how computers work on a lower lever compared to the Ruby development I normally do, so **assembly language should be a real treat.**

😂😂😂😂😂😂😂😂😂😂

I learned some cool things, and it was satisfying when I got my programs to work, but I would not describe any part of this class as a "treat". It was hard, and near the end, I couldn't wait for it to be over. Still, I got a lot out of it.

For one, I now understand why Baby Boomers call C++ a high-level programming language. And honestly, I kind of agree with them.

The big difference between assembly and other programming languages is that each assembly instruction (mostly) corresponds to just one machine instruction, whereas in C++, each instruction corresponds to multiple machine instructions. Instructions in assembly are referred to as "mnemonics", because it's literally just something that's easier to remember than the actual machine language opcodes.

Therefore, assembly lacks basic features that most programming languages share, such as the ability to assign the value of a variable to another variable in one line, or to use the keywords `if` and `else`. So from my perspective, C++ has more in common with Ruby than it does with assembly. Ergo, C++ is a high-level language.

Obviously, there is still a pretty big difference between Ruby and C++. We need a better term than "high-level" to describe Ruby. "Celestial", perhaps.

Another big takeaway is that this class showed me the *why* behind some things that I had previously accepted as “just the way things are with computers”. For example, I now understand why floating-point arithmetic is inexact. You know how the decimal representation of 1/3 is 0.3333333...? In a computer, we have to represent those infinitely repeating sequences in a finite space, so we get rounding errors. And since in a computer we are representing those numbers in binary, even some fractions that terminate in decimal notation repeat infinitely in binary. (0.4 is 0.01100110011...)

Another example is why array indexes start at zero. If an array is a contiguous block in memory (which it is in assembly), then the address of the array is the address of the first element. So, if we call the first element `list[0]`, then we get a nice clean formula for calculating the address of element `list[k]`:

```
address of list[k] = address of list + (k * size of element)
```

So despite the fact that this class was not fun the way [CS 165]({% post_url /2018-01-07-intro-to-cs %}) was for me, I am glad I took it, and proud of myself for getting through it.

And if nothing else, I now know exactly how low-level is too low for me. 😁

# Advice to students

During the first half of the course, I would try to do all the readings and watch all the videos before I did the summary exercises. To prepare for the midterm, I went through all the lecture slides and wrote things that looked like they would be helpful on my cheat sheet.

After the midterm, I switched to mainly scanning the lecture slides while I did the summary exercises, and referring to the textbook when I needed more detail about something. To prepare for the final I watched all of the videos from the second half of that class and wrote things that looked like they would be helpful on my cheat sheet.

I got a significantly better grade on the final than I did on the midterm. Two full letter grades higher. Not saying you should do what I did, but make of that what you will. And I wasn't reading or watching the lectures *passively* during the first half of the course, either; I was doing the review exercises at the end of each section.

Also, when they say that programs 5 and 6 are significantly more work than 1-4 and that you should not procrastinate, they mean it.

# What's next

Freedom! I am taking the summer off from OSU. I am looking forward to lazy weekends, getting back into Elixir, lots of blogging, going to lots of meetups, and maybe giving some talks. And I just impulse-bought tickets to [DjangoCon](https://2018.djangocon.us/) because it's going to be in San Diego this fall, so maybe I should try to learn a little Python? I am not going to do all of that in just 3 months, but I'll try to make the most of it.

In the fall, I'm taking Data Structures (CS 261).
