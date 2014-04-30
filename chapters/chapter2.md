Chapter 2: Synchronization
--------------------------

`git` has the option to sync changes from/to remote repositories. You might be encountering multiple users accessing the same repo for a lot of internal work based on development and thus, it gets difficult to sync changes made by all of them. It is thus necessary to capture all of these changes done into your system before you push your code to the remote repo.

> Note that the remote repo is the prima-facie standard of a final codebase. You might be developing changes locally but unless they are synced to a remote repo, they are (usually) not considered as final. This is because of usability of your repo by yourself/others. Unless your latest changes are not committed, you'll get an incomplete repo to work with.

Standard of working with git remotes:
-------------------------------------

Before we move into how repos are synced, it is important to understand how do you actually work with remote repos. 
> You get two types of repos - under your username (which are considered your own repos) or of others with access (public repos are accessible by all, private ones need permissions). 

Once you know you've to work on a certain repo created by others, it is your duty to make a copy of the repo into your repositories. This method is called `forking`. Forking a repo means that you create a clone of the user's repo into your list of repos so that while developing, you aren't disturbing his system at all. Once you've done with all changes, it is safe to then submit a `pull request` (explained later).

1. Fork the user's repo. It gets cloned automatically under your username. [This is in GitHub].
2. Clone this forked repo into your system using `git clone <forked_repo_URL>`.
3. Now that you've cloned this, this would be considered as `origin`.
4. Save one more remote link `main` by giving the URL of that user's repo too. - `git remote add main <other_user_repo_URL>`
5. Now, whenever you're developing, sync changes from `main` remote and initiate a `git push origin <branch>` (YOUR forked repo only).
6. Once all changes are commited to your repo, initiate a `pull request` in GitHub. The user will now see all the changes made by you in the pull request and then *merges* with his repo thereby freezing your changes. 

Remember the golden rule: 

	pull from main; push to origin; send pull request

> If your own changes aren't reflecting it is a good practice to pull your `origin` changes also.

> Working with your own repos is easier. Just clone it, work on it and then push the changes on the same remote itself. No hassles of maintaining different remotes. No hassles of pull requests.

Synchronizing
-------------

`git pull <remote_name> <branch_name>`

This command synces the changes from the remote URL and the particular branch into your local system.

> Merge conflicts. Due to duplicate/clashing code. Fix them file-by-file. Commit them and then push them off.


