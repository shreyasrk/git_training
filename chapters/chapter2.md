Chapter 2: Synchronization and Merging
--------------------------------------

`git` has the option to sync changes from/to remote repositories. You might be encountering multiple users accessing the same repo for a lot of internal work based on development and thus, it gets difficult to sync changes made by all of them. It is thus necessary to capture all of these changes done into your system before you push your code to the remote repo.

> Note that the remote repo is the prima-facie standard of a final codebase. You might be developing changes locally but unless they are synced to a remote repo, they are (usually) not considered as final. This is because of usability of your repo by yourself/others. Unless your latest changes are not committed, you'll get an incomplete repo to work with.

Standard of working with git remotes:
-------------------------------------

Before we move into how repos are synced, it is important to understand how do you actually work with remote repos. 
> In GitHub, you've two types of repos - yours or others providing access (public repos are accessible by all, private ones need permissions). 

Once you know you've to work on a certain repo created by others, it is your duty to make a copy of the repo into your repositories. This method is called `forking`. Forking a repo means that you create a clone of the user's repo into your list of repos so that while developing, you aren't disturbing his system at all. Once you've done with all changes, it is safe to then submit a `pull request` (explained later).

1. Fork the user's repo. It gets cloned automatically under your username. [All of this is in GitHub].
2. Clone this forked repo into your system using `git clone`.
3. Now that you've cloned this, this would be considered as `origin`.
4. Save one more remote link `main` by giving the URL of that user's repo too.
5. Now, whenever you're developing, sync changes from `main` remote and initiate a `git push` to YOUR forked repo.
6. Once all changes are commited to your repo, initiate a `pull request`. The user will now see all the changes made by you in the pull request and then *merges* with his repo thereby freezing your changes. 

> Working with your own repos is easier. Just clone it, work on it and then push it back. No hassles of maintaining different remotes. No hassles of pull requests.

Synchronizing
-------------

`git pull <remote_name> <branch_name>`

This command synces the changes from the remote URL and the particular branch into your local system.
> There will be clashes and dependencies. Sort them over (explained later)
> Merge conflicts. Due to duplicate code.


