---
layout: page
title: An introduction to rebasing
description: How to avoid merge commits using rebasing in Git
date: 2016-02-08 19:08:45 +01:00
tags: "git"
permalink: RebasingInGit
---

In [Working with local branches](WorkingWithBranchesInGit) we saw that you at one point or another would get  a merge commit when you have to pull down changes from the remote server, and mix them in with your own.

In many cases these changes are not really related to you, but when you see them, you think that "Oh no, if I just had waited a bit, then I could have these changes in before I did mine".  

This is where rebasing comes in handy.

Rebasing is a technique where you can change the starting point of a branch.  That might sound weird, but a little example will help:

