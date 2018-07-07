# Environment Variables

`$HOME` is a environment variable - a variable that is accessible anywhere on
your machine.

```
HOME      home directory
PATH
```

## Inspect value
We can inspect the value of it inside Vim:

```
:echo $HOME
```
We can check it from the terminal:
```
$ echo $HOME
```

For my machine (a Mac), it shows:
```
/Users/danielmoi
```

If you are using the `alpine-neovim` image, we will see
```
/root
```


## HOME
The home directory of the current user. This is different for each user.

The value of this variable is used when performing tilde expansion.



## PATH
The search path for commands.

A colon-separated list of directories in which the shell looks for commands.

A common value:
```
/usr/local/bin:/usr/local/sbin:/usr/bin:/usr/sbin:/bin:/sbin
```

## $SHELL
The full pathname to the shell.



