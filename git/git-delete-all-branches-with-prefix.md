#Git Delete All Branches With Prefix

Ever do a git branch as see a ton of log branches you no longer need. Instead of manually doing a git branch -d you can do this.

Add Function to .aliases or .zshrc
```
function gbrm { git branch | grep $1 | xargs git branch -d }
```

If you want to delete all hotfix/ branches locally for example run:
```
gbrm hotfix
```

[Source](https://github.com/josh/dotfiles/blob/master/bin/git-branch-prune)
