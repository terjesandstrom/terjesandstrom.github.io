---
layout: page
title: An introduction to rebasing - Scenario 3
description: How to avoid merge commits using rebasing in Git
date: 2016-02-08 19:08:45 +01:00
tags: "git"
permalink: RebasingInGit
---

In [Working with local branches](WorkingWithBranchesInGit) we saw that you at one point or another would get  a merge commit when you have to pull down changes from the remote server, and mix them in with your own.

In many cases these changes are not really related to you, but when you see them, you think that "Oh no, if I just had waited a bit, then I could have these changes in before I did mine".  

This is where rebasing comes in handy.

Rebasing is a technique where you can change the starting point of a branch.  That might sound weird, but a little example will help:

We again have changes in master, and we have made our new working branch, called TerjeExperiments, we have committed some changes to that branch, and we have pulled down the remote changes to master.

It now looks like this:

![RebasingInGit](RebasingInGit_images\RebasingInGit.png)


What we want to do now is to move the "base" of the first commit (yes, there can be multiple commits) in the TestExperiments branch over to instead start at the commit to which master now points. 

We do this by choosing Rebase in the branch hub.


![RebasingInGit1](RebasingInGit_images\RebasingInGit1.png)

And in the dropdown for the "Onto branch" field, we choose Master, and press Rebase

![RebasingInGit3](RebasingInGit_images\RebasingInGit3.png)


The TerjeExperiment branch is now starting from the new master pointer, and is one ahead of that.
Now, compare with the before rebasing above.  Notice that the old commit had a hash of 5d9c767, and now that is showed dimmed, but we have instead got a new commit with the hash fa69a31.  
What has happened is that the old one is still there, but the new one - which content is the same, has been created and taken its place.  
The old one will eventually be garbage collected and disappear.  
This is what we mean by saying that "history has been rewritten".  

### Note 1:  You can only rebase local branches

Since remote branches can have been cloned/pulled down to another local repository, that means the branch relations we have now changed would be overwritten again when the other local repository was pushed up again.  This is the reason why only local branches can be rebased.  It then also makes sense to hold off a bit before you push up your local branches, you might want to rebase first. 

### Note 2: Make it a habit of rebasing when pulling down

The practice of rebasing is very convenient.  Notice in the [page on working with git branches](WorkingWithBranchesInGit) that you doing the merging requires you to switch branches, make merge commits etc.  With rebasing it is all much less to do.   You can also just rebase on top of the remote branch, given that you have fetched down first. 



