---
layout: post
title: "Ruby methods are objects: a debugging tip"
date: 2018-05-16 19:10:00 -0700
tags: Ruby
---
Today I was debugging some RSpec tests that were failing intermittently. Eventually I narrowed the issue down to Devise's `active_for_authentication?` method, which was sometimes returning true and sometimes false.

I tried looking up the source code and had a WTF moment when I saw how `active_for_authentication?` is defined in the `Devise::Models::Authenticable` module:

```ruby
def active_for_authentication?
  true
end
```
<small>[Source](https://www.rubydoc.info/github/plataformatec/devise/Devise%2FModels%2FAuthenticatable:active_for_authentication%3F)</small>

After a bit of research I learned [via StackOverflow](https://stackoverflow.com/a/660129/8238305) that you can use the `method` method to find out where an object gets a method from. This showed me that my user model was actually using the `active_for_authentication?` method defined in `Devise::Models::Confirmable`, not `Devise::Models::Authenticable`.

```ruby
user.method(:active_for_authentication?)
#=> #<Method: User(Devise::Models::Confirmable)#active_for_authentication?>
```

This version of the function was a bit more complicated than merely returning `true`. Sanity restored.

```ruby
def active_for_authentication?
  super && (!confirmation_required? || confirmed? || confirmation_period_valid?)
end
```
<small>[Source](https://www.rubydoc.info/github/plataformatec/devise/Devise%2FModels%2FConfirmable:active_for_authentication%3F)</small>

Eventually, I realized that the failing tests were caused by calling `Timecop.freeze` in an unrelated test without calling `Timecop.return`, which was messing with one of the time-based checks Devise does.

# More about the `method` method:

It returns an object of class `Method`, which has a lot of other useful methods you can call:

``` ruby
user.method(:active_for_authentication?).source_location
#=> ["/path/to/file.rb", 144]

user.method(:active_for_authentication?).owner                 
#=> Devise::Models::Confirmable

user.method(:active_for_authentication?).parameters         
#=> []
```

You can also perform sorcery like assigning methods to variables and calling them, which I'm sure is useful sometimes although I can't imagine such a scenario:

```ruby
m = 12.method("+")
m.call(3)    #=> 15
m.call(20)   #=> 32
```
<small>[Source](https://ruby-doc.org/core-2.2.0/Method.html#call-method)</small>

The first thing they tell you when you start learning Ruby is "everything is an object". I feel like I understand this better every day, even after two years of writing Ruby. Yes, everything is an object, including methods.
