## Git Rebase

# What is Git Rebase? - Conceptual Overview

The first time I tried the git rebase command, I was confused -I find most git commands unwieldy & git has a bad user experience-
Rebase has a simple job integrate the changes from one branch into another. Just like merge.

But git rebase has a very different flow to achieve this.

## What does git merge exactly do?

To highlight the difference between the two approaches. Let's examine git merge first as it's the more common approach.

git merge starts by creating a commit in the feature branch that ties together the histories of both branches, maintaining both branches without any alteration.
Although git merge is a simple safe command, it can clutter the history of your feature branches.

## Git Rebase

As an alternative to merging, you can rebase the feature branch onto the main branch.
rebase puts your feature branch in front of the main branch.

**DANGER!**

git rebase rewrites the project history by creating brand new commits for each commit in the feature branch.
This can cause lots of problems we will discuss but, first the nice things.
Eliminate the unnecessary merge commits required by git merge
Linear project timeline. Instead of the miss of "metro lines" merge creates you get a single line simple easy to follow. 

## Avoiding a disaster

Tinkering with time is a dangerous act.
Now that you know about rebasing, the most important thing to learn is when to avoid it.

*Never rebase a branch used by other people.*

Think about what would happen if you rebased the dev branch on the main branch?

The rebase moves all of the commits in dev in front of main. 
Only you have this update in your local repository. 
All of the other developers are still working with the original dev. Since rebasing results in brand new commits, git will think that your dev branch history has diverged from everybody else’s

*For such branches only use merge
*
