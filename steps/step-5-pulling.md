Step 5 - Pulling
========

## Overview

As the name suggests, "pulling" does the opposite of "pushing".  Instead of taking your local changes and sending them to the server, pulling will take any changes that are made on the server version of the source code and bring it local.

If you have commits locally, Git will automatically rewind any commits that have been made and replay the commit events that occurred in the correct order.

Whenever you decide to do a pull and you have local commits, git will automatically do what is called a "Merge Commit".  A merge commit is essentially a verbose way of saying that there were two branches that had diverged at one point in time and this commit is bringing them back together.

## Exercise

On the GitHub website, let's make a change to your code.  To do this, navigate to your repository and click the "README.md" link.  This will bring you to a page where you are able to click the pencil icon to edit the file directly.

When in this editing view, add in a new colour pen at the very bottom of the list.  Once complete, scroll down to the "Commit changes" part of the page and add in a comment stating that you are adding in the newly stocked pen and click "Commit changes" to commit it directly to the master branch.

Now, on your local version of the repository, your boss tells you that the price of pens has gone up!  So, we need to update the price of blue pens to $1.00.  Commit this change and try to push it.

Command Line:

```
$ git push
To git@github.com:{username}/sample-store.git
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'git@github.com:{username}/sample-store.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```

Uh oh, it seems that someone else has made a change to the repository and git isn't letting us push our changes until we have that change locally.

So, now what we need to do is actually pull any changes that were made remotely down onto our local version of the repository and then we will be able to push our changes out!

Command Line:

```
$ git pull
$ git push
```

After running these commands, go back to the GitHub page for your repository and take a look at the latest commit through the "commits" link.  You will see all of your changes, plus an extra one.  It says:

```
Merge branch 'master' of github.com:{username}/sample-store
```

This is the merge commit that we were talking about earlier.  There are ways to avoid this however, we will get to that in a future step.

## Next Steps

So, that pull went through smoothly, but what happens if two people are modifying the same file at the same time, and actually touch the same line of code?  This is where conflicts come in.  Click [here](step-6-conflict-resolution.md) to start finding out about how to work through them.