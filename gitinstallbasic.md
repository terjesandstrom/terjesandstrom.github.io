---
layout: page
title: Git
category: wiki
permalink: gitinstallbasic
---

### Install git

| Windows | Linux | MacOS |
|----|----|----|
| [Windows git](https://git-scm.com/download/win) | [Linux git](https://git-scm.com/download/linux) |[ Mac OS git](https://git-scm.com/download/mac) |

If you have git installed, check that you are on the latest on, which is now (March 21st, 2019) 2.21.

Use the command:
```
git --version
```



### Install Visual Studio Code

[Download](https://code.visualstudio.com/download)   Links to all targets

### Install git tools

| Windows | Linux | MacOS |
|----|----|----|
| [SourceTree for Windows](https://product-downloads.atlassian.com/software/sourcetree/windows/ga/SourceTreeSetup-3.0.17.exe?_ga=2.247612480.698735789.1553020656-1415669506.1553020656) | - | [SourceTree for MacOS](https://product-downloads.atlassian.com/software/sourcetree/ga/Sourcetree_3.1.1_213.zip?_ga=2.247612480.698735789.1553020656-1415669506.1553020656) |

or

| Windows | Other platforms |
|----|----|
| [GitKraken for Windows](https://www.gitkraken.com/download/windows64) | [GitKraken, other plateforms](https://www.gitkraken.com/download) |

#### For Powershell users:
Install as module using:
``` 
Install-Module -Name posh-git -RequiredVersion 0.7.3  
```
If you already have an earlier version installed, you must use the **-Force** parameter to update to the new version

This command has to be run from an elevated command prompt.

"Provides prompt with Git status summary information and tab completion for Git commands, parameters, remotes and branch names."

[Information](https://www.powershellgallery.com/packages/posh-git/0.7.3) 


#### For Visual Studio

[Visual Studio git extension install](gitinstall)

#### For [Visual Studio Code](https://code.visualstudio.com/download)

At the minimum, install [Git Lens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)


#### Visualizing the git tree

GitViz, Superb tool for learning how the git tree works with commits and branches. Use during learning phase, or for teaching others. 

[Download](https://github.com/Readify/GitViz/releases)

#### Git aliases

In the beginning it can be wise to not use aliases for the git commands, to learn them "as is".  However, after some time using aliases can give you a real speed-up. 

[This post](http://hermit.no/visual-studio-and-vsts-git-extend-the-git-command-line-to-speed-up-your-workflow-part-1/), ([also see part 2](http://hermit.no/visual-studio-and-azure-devops-git-extend-the-git-command-line-with-server-commands-part-2/)) descibes how they work, and [this is my set of git aliases](https://gist.githubusercontent.com/OsirisTerje/e9d06c627405f576e6ebf85e2c09f3c4/raw/f34398cbe3eccccbfd5d58df3c4541f99ea47b84/GitAliases).
