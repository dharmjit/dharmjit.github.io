---
published: true
layout: post
Title: 'Starting with Git Version Control:Part1'
---
Developers understand the value of version control management for the application we are developing. Small project can survive version control but if we are creating enterprise level applicaiton and not using any version control we are in big trouble. I am not going to write about the various version control systems available and which one is better in this post but start directly with the GIT version control which currently is the most popular version control.
In this post I will cover the basic setup and start the coding. I will take example of a small team of 2 persons(foo and bar) going to start coding of a project and they are thinking of using git as version control software.

##  Basic Setup
Being distributed version control, It seems that it is difficult to set up. But believe me its not. We need to install git softwares on all the machines where we need to use version control. First of all we need to maintain one central repository, which could be on different server or one of the developer machines by using below command

_ssh user@host git init --bare /path/to/repo.git_

In above command we need to provide the user,host,path and repo as per our needs. The bare options doesnt allow this to be working directory which we want for our central directory.

### Cloning
Now foo and bar will clone this central repo to their machine which will create local repositories in their respective machines using below command. Cloning will also add a shortcut called origin which points to the remote central repositories 

_git clone ssh://user@host/path/to/repo.git_

### Edit/Stage/Commit Process

Now both foo and bar have their respective repository which is local copy of the central repository. They can work on their respective task with whatever IDEs they are using by opening local repo copy on their machine. They can use edit/stage/commit model of Git, which means add it and commit it.
The above steps will ensure that your changes are being tracked in your local repositories regardless what other developer is working on. Below commands are used to see the status of our local repo which will tell us about the modified file which we can then add to staging area and commit to our local copy.

_git status # View the state of the repo_

_git add <some-file> # Stage a file_

_git commit # Commit a file</some-file>_