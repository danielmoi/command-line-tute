# Path

We're going to look at the paths and the `$PATH` variable.

We made our shell script `magic.sh` in the previous lesson.

Note that to execute it, we had to do thi:
```
$ ./magic.sh
```

We had to specify the `path` to our shell script.

If we had done this:
```
$ magic.sh
```

We would have gotten this error:

```
$ magic.sh
zsh: command not found: magic.sh
```


This is because our shell is trying to execute the command `magic.sh` but it doesn't know WHERE to look.

By default, the shell will look in a group of directories for where the `magic.sh` program lives.

This group of directories is stored in a variable called `$PATH`.

----
## $PATH

Let's see what's inside this variable:

```
$ echo $PATH
```
