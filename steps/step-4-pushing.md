Step 4 - Pushing
========

## Overview

Everything that you do in your local version of your repository, stays in the local version of your repository.  If you commit, nothing will arrive on a remote server until you explicitly tell it to.

That is where pushing comes into play.  It's job is to push any changes that you may have made locally into the remote repository for everyone else to see.

For more information click [here](https://help.github.com/articles/pushing-to-a-remote/).

### Pre-Requisites

 * Your repository is pointing to a remote setup.  If you have been following this tutorial, then this will already be done because you cloned it from GitHub.
 * You have the latest version of the code on your local machine.

## Exercise

We finished the previous step by committing to our git repository.  What would you expect to see on GitHub?  Has the file been changed, or is it how it was originally?

Take a look on your repository to see what it has listed.

You will see that none of your changes (the changing of the price) has been updated on GitHub.  That is because we forgot to push!

So, run a push now.

Command Line:

```
git push
```

Now what do you see?  The changes should now show up on the GitHub page!  Navigate to it to verify.

## Next Steps

This approach assumed that we were the only ones working on the code.  If there were other code changes made in this repository, then this step would not work.  So, our next step will be talking about how we bring other people's changes into our repository.  Click [here](step-5-pulling.md) to continue.