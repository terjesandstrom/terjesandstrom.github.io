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

### Small team working without branches
John and Terje cooperates on working with the code.  John pushes up his commit, and Terje tries to commit his, but is rewarded with a message saying he can't push, because there already are changes on the remote. 

![WorkingWithBranchesInGit](WorkingWithBranchesInGit_images\WorkingWithBranchesInGit.png)

This is the same as with TFS VC, you need to do a get latest first, which in Git, is done doing a Pull. 

And, when you do a Get Latest, you may get merge conflicts, and it is here the Git branches can help. 

But first, let us see what we can do to get this to work nicely.
We can do a Pull immidiately, and that may or may not trigger a merge.  But we can also start with a Fetch.  A  Fetch is the first part of a Pull.  From the [Git Survival Guide](ASurvivalGuideToGit) you see that the Pull brings the commits from the remote all the way down to the workspace.  A Fetch does the first part, it moves the commits from the remote in to the local repository, but does NOT move it into the workspace.  
This is smart to do, since it makes it easier to see what these remote commits are, and if they possible could trigger some action on your side.

![WorkingWithBranchesInGit1](WorkingWithBranchesInGit_images\WorkingWithBranchesInGit1.png)

And we see that the commit from the remote updated an existing class, whereas we locally added a new class.  This should not create any conflicts.  But we do have a branching here that needs to come together:
![WorkingWithBranchesInGit2](WorkingWithBranchesInGit_images\WorkingWithBranchesInGit2.png)

And that must happen before we can push, so we have now no choice but to merge these two commits.

### Merging in git is easy

Thankfully, Git merging is just as forgiving and easy as the branches, and we can merge any branches, we don't even need to worry about how they are related.  In this case we merge the two parts of the same branch, the local and the remote. 

Normally we would do that using the Merge button in the Branches hub, but in this case we just trigger it by using the Pull button in the Synchronization hub.  (We could have used the Merge here too, it is fully legal to merge a remote branch into a local, they both exist in our local repository). 

![WorkingWithBranchesInGit3](WorkingWithBranchesInGit_images\WorkingWithBranchesInGit3.png)

The merge worked with no conflicts, but we got another merge commit with the combined changes, and now we have two commits to push up.

![WorkingWithBranchesInGit4](WorkingWithBranchesInGit_images\WorkingWithBranchesInGit4.png)

The two commits marked (1) and (2) are the two we need to push up, if we do so, the remote master will be in sync with us.   It is smart to do this as soon as possible, so that we don't get more remote commits to merge in.  

![WorkingWithBranchesInGit5](WorkingWithBranchesInGit_images\WorkingWithBranchesInGit5.png)

Note how the remote master branch pointer now have moved up along with the local master branch pointer.  If you **think** "branches are pointers" it makes it easier to get a good grasp of this.  

### Small team working with local branches

Let us now assume that you didn't really want to merge these changes in now, you wanted to (1) Just delay the merge, you didn't feel ready  (2) You wanted to share your code with another developer, but not the merged stuff  (3) You wanted to just see if your changes still builds on the server build. 

If you make it a habit of **always** working in a local branch,  these things can be done, and also, it opens up more possibilities.  











