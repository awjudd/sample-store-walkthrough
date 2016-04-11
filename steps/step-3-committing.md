Step 3 - Committing
=======

## Overview

Every source control system has a concept of "committing".  The verb that they use may vary (i.e. check in, commit, etc.) however, they all mean the same thing.  That thing is essentially "add my changes into the repository to track the change".

During this step, metadata about the file is generated (i.e. deltas are created).  The source control engine will keep track of the changes that went into that commit.  Be it, adding and removing files, or modifying pre-existing ones.

## Exercise

In your local version of the "Sample Store" demo, open up the "README.md" file and adjust the price of the blue pens to $0.75 and then save the file.

Now try to do a `git commit`.  What happens?

Absolutely nothing right?  Do you know why that is?  It's because you haven't staged any of the changes.  Git does not assume any of the files that you want to commit, you have to explicitly tell it.  That is where the staging area comes in handy.

For now, let's just stage all of the files.

Command Line:

```
git add -A
```

This command tells git to add in all changes which are in your directory (recursively) which are not being excluded by the `.gitignore` file.

Once staged, run `git commit` again.  What happens now?  You are prompted to specify a comment.

### Standards

When committing messages into a git repository, the first line should not be more than 50 characters.  This goes into the main "commit" area of the log.  If you have more to say add in a new line and it will automatically go into a "details" section where you are supposed to provide specific details about the commit.

## Next Steps

We have now committed our first change to source control.  But what happens from there?  Click [here](step-4-pushing.md) to find out.