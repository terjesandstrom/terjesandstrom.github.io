---
layout: page
title: Cleaning up with Git
description: How to clean up when it gets wrong with Git
date: 2016-02-08 19:08:45 +01:00
tags: "git"
permalink: CleaningUpWithGit
---

Things tend to go wrong, they always do. And there are different ways that things can go wrong.  
So we need ways to clean up and correct the things that go wrong.
This post is about what you to fix things **when** they go wrong. 

There is a [great flowchart by Justin Hileman](http://justinhileman.info/article/git-pretty/) that sorts out the different commands, when to use them and what they do.  We're going to walk through these and see how they are implemented in Visual Studio, and for what remains - point out where you need to use the command line.


# Simple cleanups

## Uncommitted mess

You have made a series of changes, and now it is just but a mess.  There are two things you can do, depending upon what you want to do with the mess:

### "I don't care about it" - Undo 

The undo is both in the Solution explorer, where you can undo one by one or all of them,  and in the Changes hub in the Team Explorer.

In both cases, just right click and choose Undo from the context menu

### "I might fix this later" - Store it in a separate branch

With git you don't need to create branches before you do your changes.  You can just as well create them afterwards, and you can create them when you have uncommitted files.  This is very handy for cases like this.

Just create a new local branch, like "MyOwnMess/Take3", which will point to the same commit as the branch we branch off from do.  Then commit your mess into this branch, and go back to the branch you branched off from. 

![CleaningUpWithGit](img/CleaningUpWithGit.png)

(1)  A file with some mess
(2) We see the changes in the Changes hub, in the current branch  "TerjeWork"
(3) Go to the Branches Hub, and create a new local branch
(4) Call it something meaningful and Create
(5) And we got a new branch

Now, if we look at the Changes Hub again, we see the same changes as in (2) above, but now in the new branch

![CleaningUpWithGit1](img/CleaningUpWithGit1.png)

This is nice, so now we can commit this.
When we commit this we see the following changes happening:

![CleaningUpWithGit2](img/CleaningUpWithGit2.png)

And we can then go back to the TerjeWork branch and continue without the mess, or more correctly, having the mess safely tucked away

![CleaningUpWithGit3](img/CleaningUpWithGit3.png)



# Not so simple cleanups, using the Visual Studio Git cleanup tools

There are two places in Visual Studio where you see the real git tools for cleaning up.  One is the Branches hub in team explorer, and the second is the history view. 