---
layout: page
title: Working with branches in Git:  Scenario 2
description: How to work with branches in git in small teams
date: 2016-02-08 19:08:45 +01:00
tags: "git"
permalink: WorkingWithBranchesInGit
---

The [Branches in Git](BranchesInGit) explained the basics of how branches works in Git, and how they are very lightweight.
If you are working by yourself, branches can be a convenience to keep yourself organised.  However, if you work in a small team, meaning from 2 or more developers working at the same time, then you **should** use local branches to keep a smooth work flow. 

###Small team working without branches
John and Terje cooperates on working with the code.  John pushes up his commit, and Terje tries to commit his, but is rewarded with a message saying he can't push, because there already are changes on the remote. 

This is the same as with TFS VC, you need to do a get latest first, which in Git, is done doing a Pull. 

And, when you do a Get Latest, you may get merge conflicts, and it is here the branches can help. 




