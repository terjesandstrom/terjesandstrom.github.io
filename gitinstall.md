---
layout: page
title: Installing Git with Visual Studio
category: wiki
permalink: gitinstall
---

When you start up Visual Studio the first time, and go to any git part, you will see a warning stating you need to install 3rd-party Git command line tools.   

![gitinstall](img/wiki/gitinstall.png)   

Following the link to Install there will make you install the 1.9.6 (at this date) of the Git tools.  The latest version (at this date) is 2.6.4.   What you do is instead installing the 2.6.4 version directly.   
Visual Studio is smart enough to detect that this is installed and the warning disappears.    
You install from the [Git download site](https://git-scm.com/download/win).  

__NOTE:__  
The default download will use the download for your op-sys.   Visual Studio requires the 32 bit version of Git to be installed to get rid the warning, even if the x64 will work.    

