# What is the difference between git push, pull, and fetch?

- `git fetch` - gets the changes from a remote repo into your tracking branch. 
  git fetch  takes the current branch, and checks to see if there is a tracking branch. If so, it looks for changes in the remote branch, and pulls them into the tracking branch. It does not change your local branch. 
- `git pull` -  gets the changes from a remote branch into your tracking branch and merges them into a local branch.  git pull does a `git fetch` followed immediately by `git merge`. 
- `git push` - sends the changes from a local branch to a remote repo. 
  `git push` takes the current branch, and checks to see whether or not there is a tracking branch for a remote repository connected to it. If so, the changes are taken from the local branch and pushed to the remote branch. 

- `git merge` - merges the changes into your master branch (usually called "master").

------

Note: Note that `git push` and `git pull` are not equivalent. git pull does both git fetch and git merge. 

------

### How to  make the remote branch resemble my local branch

Before you commit your local branch changes to a remote branch,  you have to ensure that the remote branch has not diverged from your local branch. That is, the commits in the remote branch must already be in your local branch, otherwise your commits will not succeed.

 To synchronize your local branch with the remote branch, use:

​		`git pull` 

OR

​		`git fetch` followed by `git merge origin/master` 

​		If you want to make sure you understand the changes you are merging into the branch before the merge happens. 

------

------

