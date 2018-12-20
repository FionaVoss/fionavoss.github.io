---
layout: post
title: Four stages of understanding Git
tags:
  - 'Teaching and learning'
redirect_from: /articles/2018/02/25/stages-of-understanding-git.html
---

I use Git every day, and I would never want to work on a significant coding project without it. However, it took time for me to get comfortable with it. When I was a beginner, I picked up JavaScript and Ruby with relative ease, but Git was something that I couldn't wrap my head around for months.

So how did I go from a confused novice to a confident Git user? I can identify four distinct stages that I went through while learning Git. In this post I will describe each stage and what helped me move on from one to the next.

I wanted to write this post because I am interested in how people learn technological skills and I want to record my experience while it's fresh in my mind. I also think my story will be useful to beginners who may be struggling to understand Git, as well as anyone who teaches Git to beginners.

## As a remote backup and public portfolio

I started using Git when I was a student at [LEARN Academy](https://www.learnacademy.org). Our instructors introduced it on the first day of class. They explained the benefits of committing frequently and using branches, but for me, most of this information went in one ear and out the other.

I think I just wasn't ready to learn it yet because I didn't have enough experience coding to understand why Git would help me. What did make sense to me at the time was the concept of a remote backup and a public portfolio. I understood that committing and pushing to GitHub meant that my code was safely backed up somewhere that wasn't my computer, and that it was publicly shared online where potential employers could see it.

These are both real benefits of using Git, but they are not really what Git was designed for. They require the use of a remote repository host like GitHub. But like a lot of beginners, I was pretty fuzzy on the difference between Git and GitHub, and failed to comprehend the benefits of committing locally.

As a result, I would mostly just commit at the end of the day. (Well actually, since we were pair programming, I would mostly let my partner commit and push, and then I would just fork their repo in GitHub without messing with the command line myself.)

This is funny to me now, because during this time I worked on projects that were complicated enough that I would never attempt them today without using Git. For example, we spent 3 days building Battleship in jQuery. Now, I can hardly believe that I did that without committing frequently.

## As a tool for collaboration

Git finally started to make sense to me when we started working on our group projects at LEARN. Before that, we had always worked in pairs, and we only committed to master. Now we were working in a group of six, meaning that three pairs would be working simultaneously on one project, on three computers. To prevent absolute chaos, we needed branches. So, every time we started working on a new story, we would create a new branch for it. When we were finished, we would push the branch and merge it in GitHub using a pull request. This was a revelation because I was starting to see how Git could help me code rather than just store my code when I was finished working on it.

Most of our stories were small enough that they took no more than a day. Some days we would finish several stories. I still wasn't in the habit of committing as often as I do now. A lot of the time we might only commit when we finished a story. But at least I finally started to learn the command line syntax.

## As a way to reduce complexity

After LEARN, I went on to an internship. One of my first projects, adding a new feature to a Rails app, took several days. Since I was still in the habit of committing mainly when I wanted to merge, I ended up working for several days without committing.

At this internship I was using RubyMine, an IDE for Ruby programs. I still use it at my current job too. RubyMine has nice Git integration, including a diff viewer that lets you see your changes side by side with the previous version. You can view diffs in the terminal by running `git diff`, but in RubyMine they're a little more user-friendly.

As I was nearing the end of the project I was viewing my changes. Needless to say, there were a lot of them. I suddenly realized: this is why you commit locally! Committing frequently&mdash;any time you've made a change that you're pretty sure you're going to keep&mdash;is a way of letting yourself focus on one thing at a time.

From then on, I started to develop the habit of making [atomic commits](https://www.freshconsulting.com/atomic-commits/). I finish a small task, view the diff, and assuming I like what I see, commit. Then, when I finish the next task, I can see a clean, small diff that reflects only what I've been working on for the past hour or so. It's fresh in my mind, so it's easier to read and understand what I've changed before I finalize my changes by committing again.

## As a tool for reflection

A few months later, I moved on to my current job at Ceatus. This was where I experienced my first code reviews, for which we used the pull request feature in GitHub.

When you make a PR in GitHub, it shows you the diff between your branch and the branch you want to merge into. I knew this from our group project at LEARN, but back then we approved our own PRs and didn't spend much time reviewing the code. But as an eager new software engineer, anxious to have my PR approved, I spent a good while reviewing my code. How was this different from the stage I described in the previous section? Before, I would compare a small set of changes within a branch before committing. Now, I was comparing a large set of changes to master before committing.

Now that I've been at Ceatus for a while, not everything I work on gets reviewed by another developer anymore. However, I always review my own code in GitHub before merging. (Again, you can do this in the command line, but I prefer GitHub's interface.) It gives me a second chance to look at all the changes I have made in order to implement a feature, reflect on what I've done, and make sure I'm happy with the code before it becomes part of the master branch.

## Where I'm at now

I still use Git for all of the objectives I've described above. To me, these are the core uses of Git and GitHub: to back up and share code, to facilitate collaboration, to manage complexity, and to encourage reflection. I haven't covered everything Git can do, but these are the things I use it for on a daily basis.

## Advice for Git beginners

I think a lot of advice for Git beginners is confusing because it tries to cover too much too soon. If you feel overwhelmed, focus on one skill at a time.

If you're a complete beginner, start by learning how to [initialize a repository and commit and push to GitHub](https://help.github.com/articles/adding-an-existing-project-to-github-using-the-command-line/).

Once you're comfortable with that, get in the habit of committing frequently. As a guideline, commit titles should be no more than 50 characters. If you can't describe, specifically, the changes you made in that much space, you should probably commit more often. See [How to Write a Git Commit Message](https://chris.beams.io/posts/git-commit/) for some style advice. Run `git diff` to see what you've changed, or use an IDE with a built-in diff viewer. Take a moment to review your changes before you commit.

If you're interested in blogging, [starting a Jekyll blog](https://jekyllrb.com/docs/quickstart/) and [hosting it on GitHub Pages](https://jekyllrb.com/docs/github-pages/) is a good way to get some practice with Git, since you update your site by pushing to master.

Once you start working on bigger projects, or anything with multiple developers, it's time to start using branches. Learn how to use the [Pull Request](https://help.github.com/articles/about-pull-requests/) feature in GitHub. Before you merge, spend some time viewing the diff and reflecting on your changes.

If you're a university student, your school probably has rules against sharing assignments in public repos, but you can sign up for a [student account](https://education.github.com) on GitHub and get unlimited private repos for free. There are other platforms that host private repos for free, but I recommend getting familiar with GitHub because so many companies and open source projects use it.

There is a learning curve, but once you're comfortable with Git, I bet you'll soon feel like you can't live without it.
