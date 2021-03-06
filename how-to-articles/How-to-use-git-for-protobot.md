### Use GIT for Protobot  ###

## Overview ##
This document discusses how to use "FORKS" to manage source control for the protobot projects.  
We're going to 'fork' the Protobot repo and make changes.  After you're done, you'll push your changes
back into your 'fork', then generate a 'pull request' to merge the changes into the main line protobot.

Github has TONS of examples of code to learn from.  Other teams also have their sources loaded here
and you can see how they did things.

For those of you (ahem Mr. Platt) - here are some GUI clients you can download and use in lieu of 
the command line.

* https://git-scm.com/download/gui/windows

## Read these documents! ## 

* Github 'bootcamp' pages  - https://help.github.com/categories/bootcamp/
* This doc shows how to fork a repository and work on fixes.  This is 
 _EXACTLY_ how we did it last year.  
  -  https://help.github.com/articles/fork-a-repo/


Logically - 
* Upstream - the original protobot repo
* Local - the git repo checked out onto your laptop - where you will make changes
* Origin - the 'Fork' of protobot for your repo

![Triangle workflow ](https://i.stack.imgur.com/Lx7do.png "Triangular Workflow")


## Mechanics of working on a project.

Run these commands after your fork your repo.

'''
# create my "Local" copy of the clone to work on
git clone https://github.com/aadevoe/Protobot2019.git

# Set the upstream, so you can 'pull' changes made to the official protobot
git remote add upstream https://github.com/IHS-FRC-5459/Protobot2019.git

# Push a change to your 'fork'.
git add src/main/java/org/usfirst/frc5459/Proto2019ver1/Main.java
git commit -m "Added a new component"
git push origin master 

#
# ... at some later date ... 
# ... Subsequent Pull Request created at Github.com ... 
# 
# Time to pull the changes made to the master copy 
git pull upstream master

'''