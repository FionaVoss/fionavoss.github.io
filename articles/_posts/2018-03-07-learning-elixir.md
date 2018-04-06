---
layout: post
title: One Month of Learning Elixir
redirect_from: /2018/03/07/learning-elixir/
---

I recently became interested in learning Elixir. I had been hearing a lot about functional programming, and I wanted to see what all the fuss was about.

After doing a bit of research, I learned that Elixir is especially popular among Ruby developers who want to work with a functional language. I figured that if other Ruby lovers like using Elixir, I would probably like it too.

Keep reading to learn more about what Elixir is and how I've been learning it.

## What is Elixir?

Elixir is a general-purpose programming language. It can be used for many types of programs including web applications.

It is based on the functional programming paradigm. In functional programming, the return value of a function depends entirely on its arguments, and calling the same function with the same arguments always returns the same result. Functions do not have any side effects, meaning that they do not have any observable effects besides returning a value. Elixir functions are organized into modules, and there are no objects or classes.

Elixir runs on the Erlang virtual machine. See [this talk by Elixir creator José Valim](https://vimeo.com/53221562) for an explanation of what that means and why it's important. Long story short: it means Elixir is scalable and fault-tolerant.

Why is Elixir popular in the Ruby community? It was created by Rails developers, and its syntax has some similarities to Ruby. More importantly, the language was designed with developer productivity in mind, a value shared by Ruby and Rails.

## How have I been learning?

The very first resource I used was [Try Elixir](https://www.codeschool.com/courses/try-elixir), a free course from Code School. This is a short course that covers some basic features of the language including modules, functions, the pipe operator, and pattern matching. It consists of short videos followed by code exercises.

I liked learning on Code School, so I upgraded to a paid account to take their second Elixir course, [Mixing It Up With Elixir](https://www.codeschool.com/courses/mixing-it-up-with-elixir), which has the same format but is longer and covers more topics including recursion, data structures, and the Mix tool.

Another tool I've used is [Elixir Koans](http://elixirkoans.io). This is a set of challenges you download and run in the command line. It consists of a set of test assertions that all fail initially, and you have to make them pass. It's a good way to get familiar with Elixir's data types and built-in functions.

Finally, I've also been practicing on CodeWars. This is a site where you can do code challenges in a variety of languages. The challenges, which they call katas, become more difficult as you progress. I've been making good use of Elixir's [docs](https://hexdocs.pm/elixir/) while practicing on CodeWars.

## How it's going so far

I can't remember where, but I recently heard somebody say that learning your first programming language is hard, learning your second one is harder (because you have to unlearn the ways of thinking that your first language taught you), but after that picking up new languages is not that big a deal (because now you can see the general principles that all programming languages share).

If you take those words literally, they do not hold true in my experience. JavaScript was my first language, Ruby was my second, and C++ was my third. Learning Ruby after JavaScript was a breeze. Some things about C++ are hard, but as long as you're not dealing with pointers or dynamic memory allocation, doing OOP in C++ isn't *that* different from writing Ruby, albeit with a much less friendly syntax.

Elixir, on the other hand, feels like the second programming language that that person was talking about. It's just so different from Ruby. The best example is probably loops. There are no `for` loops in Elixir. Instead, loops are accomplished by writing recursive functions.

Another example is control flow. Elixir does have `if` and `else`, but they are used less frequently than in most languages. Instead, it's common to define multiple functions with the same name, and use pattern matching to determine with version will execute depending on the arguments it is called with.

Here's an example illustrating both of these concepts, taken from [Wikipedia](https://en.wikipedia.org/wiki/Elixir_(programming_language)):

```elixir
defmodule Fun do
  def fib(0), do: 0
  def fib(1), do: 1
  def fib(n) do
    fib(n-2) + fib(n-1)  
  end
end
```

This example defines three functions named `fib`. If we pass it some positive integer n it will return the nth term in the Fibonacci sequence. The first two functions define the base cases that will execute when we call `Fun.fib(0)` and `Fun.fib(1)`. The third function, which is recursive, will execute when we pass it some other argument.

These differences can make writing Elixir feel like an academic exercise to me. The idea of a programming language without `for` loops reminds me of [writing a novel without the letter e](https://en.wikipedia.org/wiki/Gadsby_(novel)). I know Elixir can be a very practical choice for writing real-world applications, but as a beginner, I feel like I have no idea how anyone *does* anything in Elixir.

That said, it's a challenge that I am enjoying. Learning Elixir as a Ruby developer is harder than learning C++, but the hard parts are more enjoyable. I think that if I stick with it, I will get exactly what I want out of it&mdash;exposure to an entirely new way of thinking in code.

## What's next?

I can tell that I have reached a point where in order to continue progressing, I need to stop doing a bunch of disjointed tutorials and challenges and sink my teeth into a significant project.

However, the idea of building some command-line application doesn't excite me. I think building a web app will be a lot more fun and relevant to my personal goals.

So, my next focus is going to be learning [Phoenix](http://phoenixframework.org/), a web framework for Elixir. I plan to start with another Code School class, [On Fire With Phoenix](https://www.codeschool.com/courses/on-fire-with-phoenix). After that, I'll probably start building my own Phoenix app.
