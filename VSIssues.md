---
layout: page
title: Visual Studio issues and how to fix them
description: How to fix miscellaneous Visual Studio issues
date: 2016-02-08 19:08:45 +01:00
tags: "git"
permalink: VSIssues
---

Sometimes Visual Studio gives up on you, and this post is a collection of issues I have had, and the resolution to those.  In some case there is no fix yet, then that is documented. 

## Package load failure

This is a very common error, and it says something like "The  *something*  package did not load correctly", and may look like this:

![NewDocument](NewDocument.png)

You can go and verify that is indeed is a package load error by looking in the log it refers to, but it doesn't really help you any more.  
The cause for this is most often a corrupted MEF cache, and the best approach is to simply delete it. 

There are 3 ways to do that:

1. Command Line:  Download [IFix](https://visualstudiogallery.msdn.microsoft.com/b8ba97b0-bb89-4c21-a1e2-53ef335fd9cb) and run the command   IFix mefcache -f 
2. Use a VSIX in Visual Studio:  Install from [here](https://visualstudiogallery.msdn.microsoft.com/22b94661-70c7-4a93-9ca3-8b6dd45f47cd), and go to Tools/Clear MEF Component cache.    (Note this adds another vsix to your VS loading)
3. Just delete the relevant cache folder from command line or explorer, it is located at this place for VS 2015:  %localappdata%\Microsoft\VisualStudio\14.0\ComponentModelCache.   
For VS 2013, the number in the middle there is 12.0,  for VS 2012, the number is 11.0, and for the upcoming codename 15, the number is 15.0

