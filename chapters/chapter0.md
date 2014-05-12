Commonly used commands
======================

Lets begin with some frequently known commands and their descriptions:

1. `git init` - Initializes a git repo in the folder created (in your computer).
2. `git add file(s)` - Adds the files to the git directory to be tracked. Note that you can add directories also.
3. `git remote add <remote_name_on_local> <.git URL to be added>` - Adds a remote link for pushing all file changes to a remote repository. This creates a default branch `master` in the remote repository. Note that you can create zillion branches on remote repositories.
4. `git commit -m "your commit message"` - Freezes changes to the files/folders in the repo. Note that this becomes a git commit which can be tracked.
5. `git push <remote_name_on_local> <branch_to_be_pushed_in_remote>` - This would commit changes on the branch in the remote repository for the repository defined in `remote_name_on_local` name.
6. `git pull <remote_name_on_local> <branch_to_be_pulled_from_remote>` - Sync changes from the remote repository''s mentioned branch to the local folder on your comuter. Note that the files from the requested branch would be synced to your system.


Other useful ones, but are not mandatory to know:

1. `git log` - Shows the log of commits for the entire repo.
2. `git diff entity1 entity2` - compares git changes for the respective entities. They could be files/folders.
3. `git commit -a` - Edits the git-commit file to sync changes along with user messages and files/folders changed. Git auto-tracks changes across the repo including new additions/fresh commits.


In the other chapters, you''ll comme to know which commands pertain to certain functionalities of git viz.,

1. Branching
2. Merging
3. Semantic Versioning
4. Working with a multi-user environment in git.

These are the basic features of git that is covered in a simple software development project. I''d appreciate further reading from the links on the internet to know more about the basics.
