# Change Author of All commits (For Single User)

> One liner, but be careful if you have a multi-user repository - this will change all commits to have the same (new) author and committer.

`git filter-branch -f --env-filter "GIT_AUTHOR_NAME='Newname'; GIT_AUTHOR_EMAIL='new@email'; GIT_COMMITTER_NAME='Newname'; GIT_COMMITTER_EMAIL='new@email';" HEAD`

> Remember to Swap `Newname` and `new@email`

[Source](http://stackoverflow.com/questions/750172/change-the-author-of-a-commit-in-git)
