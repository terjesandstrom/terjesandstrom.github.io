---
layout: page
title: Using Git With Visual Studio
description: How to use Visual Studio Git functionality
date: 2016-02-08 19:08:45 +01:00
tags: "git"
permalink: UsingGitWithVisualStudio
---

This guide tells you how to use Visual Studio to work with Git in the simple Scenario 1 case (ref [A survival guide to Git](ASurvivalGuideToGit)).

### Cloning an existing remote git repository

You can find existing git repositories in any team project, or on external sites like Github.  
To find them, open up the Team Explorer and choose the Green socket icon.

 ![UsingGitWithVisualStudio](UsingGitWithVisualStudio_images\UsingGitWithVisualStudio.png)
 
Collapse the top nodes in the tree that appears



The Github (1) node will appear, but if you have anything there, just collapse it, and go to our tfs server (2).  The Products team project (3) contains the git repositories (4) of interest.  
One team project can have multiple git repositories.  This is a change from TFSVC where the source control is shared, not only within a team project but also between team projects.  Not so with Git. 
What you see here is the Remote repositories , the A's in the survival guide. 
To the right there is either a kind of folder icon (5) or a blank space (6).  If it is blank there (6), then you already have a local repository too (The B's in the survival guide).  If you see the folder (5), then you are ready for the start operation, the Clone.
As explained in the Git survival guide, the clone creates a "copy" of the remote on your local machine.  
Right click the (5) icon and choose Clone

You will now be moved down to a dialog under (7), local repositories, 

Normally you can just accept the default values.  I prefer to keep all the Kimsim repos in its own subfolder under here, so I just add a Kmsim folder (1) to the target path, and then you just press Clone (2)
After the clone operation has finished, which should only take some seconds, you go back up to your repos, and choose Connect on the repo you just cloned.

The choose the Home button (1 in screenshot below) 

If nothing appears under Solutions, press the refresh button (2), then you see the solutions within your repository, and can open whichever suits you.
 
The workflow for scenario 1
Referring back to the survival guide, there are 3 operations we need to do.  Within Team Explorer these are condensed into 2 functions:

The two functions are Changes and Sync.  
The Sync handles step 1 and 3 (from the A survival guide to Git), and the Changes handles step 2.
Press Sync to get to that hub to do step 1:

Step 1  Pull
Here you see step 1, which is the Pull, the green #1.  Prefer to use that.  It is very safe, no side effects, and is one of the basic git commands.
Microsoft has added the Sync button (2).  It combines a Pull and a Push, but since these are on each side of the workflow, it may or may not have side effects.  A possible side effect here is a merge, then followed with an automatic push you didn't intend.  It is thus better to use Push and Pull individually.
When you press Pull, you will either get new commits down, or a message saying you're up-to-date. 

 
Step 2   Coding
Now you can do your changes.  Compared to TFS VC there is no equivalent of checking out a file.  You can just drop files in, edit the file, git will pick up it is changed compared to its latest, and mark it so.  
When you fixed some small thing, just commit.  
Step 3  Commit
You can start the commit from the solution explorer, by right-clicking 

It will then take you to the Changes hub - you can of course go directly there too, if you happen to have the team explorer open - whatever is fastest.

You add the relevant workitem either as a part of the comment (1) , or using the Related workitem Add  (2).   
You see the included changes in that section (3).  
Keep an eye on Untracked files (4).  If there is anything here, you probably would like to include those to.  There is a context sensitive include option on any item here. 
Also note, that git requires a comment (1), without a comment , the Commit button (5)  doesn't appear.
When finished, just press Commit (5).

Now you can go to step 4, which is the Pull,  you can then press the Sync link here, or go to the Sync hub through the team explorer.
Step 4  Push
On this page, you will see your commits listed under Outgoing Commits, and there is really only one thing to do, press Push

You may be asked about your credentials, then use the standard KM logins.  
All your commits will then be pushed up to the server.