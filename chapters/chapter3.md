Branching
=========

One of the important requirements in a scm system is of creating independent work systems within a same repo. These are termed as branches. Branches comprise of all the source code [usually from a parent branch - `master`] along with other specific changes pertaining to it's own features. Branches are created to maintain separate links to all changes done to the code so that tracking becomes easier during bugfix/error time.

Branches are usually designed according to Semantic Versioning. Please refer to `http://semver.org` to see how software releases are done pertaining to versions that you see in the source code.
> Branches are, for example of these types: Development, Production/Release. Users work on Development and then push the changes to the Production for them to be the final code.
> `master` branch always is considered the latest production version available to work on. If it isn't the case, you're in trouble already.

> There must be separate branches for `dev-`, `feature-specific-`, `release-`, `bugfix-`, `main-`. The `-` sufix denotes the complete version number that you would be working on. Ensure all your numbers are tagged properly. Versioning depends on how the code is being planned/phased, so be careful about that. It is always easier to see if the errenous code was in a feature- branch or in a bugfix- branch later. (Semantic Versioning principles, meh!)

> You can also deviate on branching, there can be unlimited number of branches, but take care that a boring maintenance also attaches to them, periodically resulting in combining/trashing unused branches.

Process of working
------------------

Suppose you have a new feature to be employed into the code. You cannot directly work in the master branch [i.e., you shouldn't push changes to main- branch as multiple users will work on the same branch always]. So, you need to vreate a new branch for this, `features-5.3.0`

	git checkout -b features-5.3.0

This will create a new branch named `features-5.3.0` that you are planning for migrating from 5.2.8 to 5.3.0. As these features are considered to upgrade some basic features of the existing product, you are moving to a higher minor version.

> Work on this branch ONLY! If possible, create a `dev-features-5.3.0` and `rel-features-5.3.0` to separate release and development versions internally.

It will pick up source from the `master` branch by default. Commit all your changes to this branch. And then push the changes like,

	git push origin `features-5.3.0`

Now, the other users come to know that a new development has been done and will be tested. [the `git checkout` will be used again]. Once done, they are then okayed to be merged with `master` which is done by,

	git merge


Working with other users
------------------------

Going a step ahead, here is a protocol strictly followed to sync changes across in an organization.

1. Organizations have repos. Fork them. Refer Chapter-2 to how to work with remotes.
2. Clone the forked repo to your system `origin`
3. Create the branch that you'd be working with. `git checkout -b new-branch`
4. The repo now is in your branch. Do all your changes [`git add`, `git commit`]
5. Push this to `origin`: `git push origin new-branch`
6. Initiate pull request to the `main` repo after you're convinced that 

	* New branch exists in GitHub for forked repo.
	* Changes done in the new-branch are visible in GitHub.

That's it! Track Comments in submitted pull requests and then re-work if needed.



