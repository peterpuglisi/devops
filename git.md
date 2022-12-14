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
`git reset`
`git restore --staged .`

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


















