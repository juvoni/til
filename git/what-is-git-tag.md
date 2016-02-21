# What is Git Tag

CharlesB's answer and helmbert's answer are both helpful, but it took me a while to understand them. Here's another way of putting it:

- A tag is a pointer to a commit, and commits exist independently of branches.
    - It is important to understand that tags have no direct relationship with branches - they only ever identify a commit.
        - That commit can be pointed to from any number of branches - i.e., it can be part of the history of any number of branches - including none.
- Therefore, running git show <tag> to see a tag's details contains no reference to any branches, only the ID of the commit that the tag points to.
    - (Commit IDs (a.k.a. object names or SHA-1 IDs) are 40-character strings composed of hex. digits that are hashes over the contents of a commit; e.g.: 6f6b5997506d48fc6267b0b60c3f0261b6afe7a2)
- Branches come into play only indirectly:
    - At the time of creating a tag, by implying the commit that the tag will point to:
        - Not specifying a target for a tag defaults to the current branch's most recent commit (a.k.a. HEAD); e.g.:
        
        ``` 
        git tag v0.1.0            # tags HEAD of *current* branch
         ```

    - Specifying a branch name as the tag target defaults to that branch's most recent commit; e.g.:
    ```
    git tag v0.1.0  develop   # tags HEAD of 'develop' branch
    ``` 

(As others have noted, you can also specify a commit ID explicitly as the tag's target.)

- When using git describe to describe the current branch:
```
git describe [--tags]``` describes the current branch in terms of the commits since the most recent [possibly lightweight] tag in this branch's history.
    - Thus, the tag referenced by git describe may NOT reflect the most recently created tag overall.

[Source](http://stackoverflow.com/questions/14613540/git-tag-in-branches)
