---
layout: post
date: '2018-06-20 20:08:00 -0700'
title: How not to change a one-to-many association to many-to-many in Rails
tags:
  - 'Ruby on Rails'
---
I am working on a feature that involves changing an existing one-to-many relationship to many-to-many, and I've realized I made it unnecessarily troublesome for myself.

Let’s pretend the models are Artists and Albums. (An experienced Rails developer will realize after a moment’s thought that artists and albums have a many-to-many relationship. So, for the sake of my reputation, let me be clear that these were not the actual models.)

This first thing I did was create and run all my migrations. I removed `artist_id` from albums and created an `albums_artists` join table. Then I updated my models to use a `has_and_belongs_to_many` association instead of `has_many` and `belongs_to`, and continued on with the rest of the feature.

# The problem

Now my feature branch and our master branch expect different database schemas. Specifically, the master branch expects Albums to have an `artist_id`. Since that column has been removed from my local database, then anytime I switch to master, the relation is broken.

Also, I haven’t been able to deploy to our sandbox environment because it would cause all sorts of headaches for the other developers.

# What I should have done

1. Run the migration to create the join table, and update the models to use `has_and_belongs_to_many`.
2. Build the rest of the feature.
3. Run the migration to delete `artist_id` from albums at the last minute, right before I’m ready to deploy to production.

That way, no matter what branch I was in, the database would have worked for the relation defined in that branch.

I am pretty confident that this will work, but since I haven’t actually done it before, there may be some problem I’m not anticipating. So, I would definitely appreciate your feedback if you have done this before.
