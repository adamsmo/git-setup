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
