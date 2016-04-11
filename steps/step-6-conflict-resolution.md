Step 6 - Conflict Resolution
=====

## Overview

Throughout the development process, conflicts are bound to happen.  Be it, people working in various branches and the code is merged together, or two people working in the same piece of code at the same time.

It's how you deal with them that matters.

Click [here](https://help.github.com/articles/resolving-a-merge-conflict-from-the-command-line/) for more information about resolving conflicts.

## Exercise

One of your bosses just informed you that the cost of red pens has increased.  This has to go live immediately because we are losing money!  Navigate to the store in GitHub and adjust the price of red pens to $1.50 and commit the change!

Now we just got word from the supplier that there was a typo in the memo that was sent out.  The price of red pens has actually dropped down to $0.75.  But, since the upped price of red pens isn't necessarily hurting us, let's take our time with the change.  Make the change in your local git repository (do **not** do a pull prior to changing the cost).  Commit this change to your local repository.

Now, it's time to push this change out, so let's be a good developer, and pull from source control first.

```
$ git pull
remote: Counting objects: 3, done.
remote: Compressing objects: 100% (1/1), done.
remote: Total 3 (delta 1), reused 3 (delta 1), pack-reused 0
Unpacking objects: 100% (3/3), done.
From github.com:{username}/sample-store
   426d0a3..cd9eaf7  master     -> origin/master
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
```

Uh oh!  There is a conflict!

By default, git will show the conflicted lines one under the other as follows:

```
1. Blue Pen - $1.00
<<<<<<< HEAD
2. Red Pen - $0.75
=======
2. Red Pen - $1.50
>>>>>>> {commit hash}
3. Green Pen - $0.50
```

What this means is, locally (at HEAD), we have the following line:

```
2. Red Pen - $0.75
```

However, on the remote version of the repository, we have:

```
2. Red Pen - $1.50
```

Since this is a conflict, git doesn't know what you want to do with it, so you have to manually complete the merge.  Take our local version of the changes.  To do this, all you need to do is modify the file so it looks like you want it to afterwards.

Once done, we will need to tell git to accept the code as it stands resolving the conflict.  To do this, all you need to do is stage the file, and then commit it.

Command Line:

```
$ git add -A
$ git commit -m "Resolving conflict"
$ git push
```

This should push the changes back up to GitHub.

## Next Steps

Working in one branch is good.  However, if you need to make some drastic changes, it is far better practice to use a feature branch in order to do your work.  Click [here](step-7-branching.md) to continue on to branching.