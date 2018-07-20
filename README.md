# git-setup

## set name
```
git config user.name "John Doe" 
```

## set email
```
git config user.email email@email.com
```

## set gpg key
```
git config user.signingkey kye_id
```

## always sign commits
```
git config commit.gpgsign true
```

# git commands

## checkout file form different branch to current branch
```
git checkout other_branch_name -- file_path
```

## squash n top commits
```
git rebase --interactive HEAD~n
```

## clean deleted branches
```
git remote prune origin
```

## delete local merged branches
```
git branch --merged >/tmp/merged-branches && vi /tmp/merged-branches && xargs git branch -d </tmp/merged-branches
```

## delete all local merged branches from list
```
git branch >/tmp/merged-branches && vi /tmp/merged-branches && xargs git branch -D </tmp/merged-branches
```

## pull submodules in git first time
```
 git submodule update --init --recursive
```

## crate and push tag on current branch
```
git tag tagname
git push origin --tags
```

## add +x to commited file
```
git update-index --chmod=+x file.name
```

## delete commit from local branch
```
git reset --hard HEAD~1
```

## tags management
```
git tag -am "annotation goes here" tagname_goes_here # cut a tag
git tag -d tagname_goes_here                         # burn it
git tag -am "annotation goes here" tagname_goes_here # cut another tag
git push --tags                                      # push tags to remote
git push origin :refs/tags/tagname_goes_here         # delete tag from remote
```
