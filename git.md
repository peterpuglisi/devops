## Output list of config settings

`git config --list`

## Update name and email

git config --global user.name "Your Name"
git config --global user.email "you@example.com"


## Get current status

`git status`

### Git log

`git log`

### Git add all files

`git add .`


### Git commit with a message

`git commit -m "updates"`

### Git diff

`git diff`

### Combine git add and commmit

`git commit -a -m "updates"`

## Last commit from log

`git log --oneline`

### With visual representation

`git log --graph`


### Reset

- Reverts what was added to the index/staging area:
`git reset` - updates the index (staging/added)
`get reset --hard` - updates both the index (staging/added) and the working tree

## Revert all local and added changes to cloned and committed state

`git reset --hard`

### Fetch the remote branch and set your branch to it

git fetch origin
git reset --hard origin/master


### Git stash pop

- Stash current changes
`git stash`

- Restore stashed work
`git stash pop` 

- Get stash list
`git stash list`

- View what is in a stash for lastest stash change
`git stash show --patch stash@{0}`

- Extract/apply a particular stash
`git stash apply stash@{1}`

- View diffs
`git diff`


### Git add interactive

`git add -i`

### Git reflog

- Reference log of history of changes made to the head
`git reflog`

- Reset back to commit id, to undo last commit for example
git reset --hard **commit id**

new line added to staging

### Cherry picking a change made in another branch into current branch
- Do a `git log --all --oneline` to find the commit id of the change you want.
- Switch to master branch and cherry-pick that commit:
`git cherry-pick <<commit-id>>`

### git rebase

- Switch to the branch where changed were made but main branch has moved on will other commits
- Resolve conflicts and follow any hints
 
`git switch <branch_name>`
`git rebase main`
`git rebase continue`  (if needed)

`git log --all --decorate --graph` - to check new graph to verify rebase

- Merge rebased branch into master
-`git switch master`
-`git merge <branch-name>`  (This will fast-forward main by default)



### Reote Repositories

- This just gives you remote back :)
`git remote`

- To view list of branches with more info
`git branch -vv`

- Push a new local branch up to origin
- `git push --set-upstream origin <branch-name>`

- Short version
- `git push -u origin <branch-name>`

- When running `git branch -vv`, the new remote branch should show in the list in addition to the local branch

- To push more changes to the remote branch after that, `git push`

### How to update you local branch with latest changes from master (using merge)

* Go to master branch with: `git switch master`

* Update your local master with: `git pull origin master`
  - Better still, do a `git fetch origin` followed by   `git merge origin/master` so that you fully understand what `git pull` actually does.

* Resolve conflicts (if applicable)
* Go back to features with: `git switch features`
* Merge master branch over features with: `git merge master`
* Push changes with: `git push -u origin features` (the -u sets the upstream remote branch and tracking in you local repository)
* To push more changes, you can then just do `git push`

### How to update you local branch with latest changes from master (using rebase)

`git fetch`
`git rebase origin/master`

- Shorter version
- `git pull --rebase`



### About pull

- `git pull <remote> <branch>`

* is equivalent to 
- `git fetch <remote>`
- `git merge <remote>/<branch>`






























