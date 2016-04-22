# How to see the command attached to a bash alias?

The `type` builtin is useful for this. It will not only tell you about aliases, but also functions, builtins, keywords and external commands.

```
$ type ls
ls is aliased to `ls --color=auto'
$ type rm
rm is /bin/rm
$ type cd
cd is a shell builtin
$ type psgrep
psgrep is a function
psgrep () 
{ 
    ps -ef | { 
        read -r;
        echo "$REPLY";
        grep --color=auto "$@"
    }
}
```

[Source](http://askubuntu.com/questions/102093/how-to-see-the-command-attached-to-a-bash-alias)
