#Pull Range of Commits Into Current Branch

The flow is to first create a new branch from feature at the last commit you want, in this case 62ecb3.

```
git checkout -b newbranch 62ecb3
```

Next up, you rebase the newbranch commit --onto master. The 76cada^ indicates that you want to start from that specific commit.

```
git rebase --onto master 76cada^
```

The result is that commits 76cada through 62ecb3 are applied to master.


[Source](https://ariejan.net/2010/06/10/cherry-picking-specific-commits-from-another-branch/)
