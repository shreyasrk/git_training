Chapter 1
---------

We'll be delving with the details from here.

Initialize the repo:
-------------------

> Start with `git init`. This would create a git managed source control management system within the folder that you work in.
> Once git system is created, your task is to now manage the source code within the directory.

Working with remote links:
--------------------------

The powerful feature of git provides is that of remote committing. You can now transfer all your local commits to a remote location for safety and portability. Although this feature is most prominently used, it isn't necessary to work with a remote link at all. You can save the commits locally too. Git can then combine all the commits into one single package and versions them accordingly to the commit done.

Remote repositories can be either be cloned or created. Cloning repos is the most simplest way. Just go to any git-remote repository hosting solutions such as GitHub, BitBucket and create a repo there and simply clone it off to your local machine!

`git clone <URL_for_the_repo>`

git then copies the contents of the remote repo into your machine and attaches a git-scm system to it automatically. You can now continue to work on the repo without any primitive changes! Because of this feature, git is extremely portable across machines.

The other way is to create your repo locally, make a remote repo with the same name as that of the repo and then simply pushing it there.

	     ~$ mkdir myrepo
	     ~$ cd myrepo/
	~/repo$ git init
	~/repo$ touch sample.txt
	~/repo$ git add sample.txt
	~/repo$ git commit -m "First Commit"
	~/repo$ git remote add origin https://github.com/username/myrepo.git
	~/repo$ git push -u origin master

Some additional info:
--------------------

  -u in git push fixes an upstream path for the folder. Here, it is our remote repo created in GitHub.


You can also avail `git commit -a` for a simple pop up in your favourite editor of choice where you can edit commit messages and file tracking in the commit. Note that all lines beginning with a `#` are omitted during committing messages.


