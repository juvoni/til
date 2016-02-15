#Update Local Project Commit Author

When first settings up Git on my machine I ran (like everyone does):
```
$ git config --global user.name "Orr Sella"
$ git config --global user.email myemail@address.com
```

The global user configuration wasn’t going to help me with my situation – I need to use different emails for the different environments.

Fortunately, Git allows you to add configuration for individual repositories. This would solve the problem – I’ll manually add the correct email to each repository locally:

```
$ git config user.email myemail@address.com
```

[Source](https://orrsella.com/2013/08/10/git-using-different-user-emails-for-different-repositories/)
