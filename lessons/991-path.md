# Path

We're going to look at the paths and the `$PATH` variable.

We made our shell script `magic` in the previous lesson.

Note that to execute it, we had to do thi:
```
$ ./magic
```

We had to specify the `path` to our shell script.

If we had done this:
```
$ magic
```

We would have gotten this error:

```
$ magic
zsh: command not found: magic
```


This is because our shell is trying to execute the command `magic` but it doesn't know WHERE to look for the program.

By default, the shell will look in a list of directories for where the `magic` program lives.

This list of directories is stored in a variable called `$PATH`.

----
## $PATH

Let's see what's inside this variable:

```
$ echo $PATH

/Users/danielmoi/.npm-packages/bin:/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin
```

This is a colon separated list of directories.

In this example, there are 6 directories:
```
/Users/danielmoi/.npm-packages/bin
/usr/local/bin
/usr/bin
/bin
/usr/sbin
/sbin
```

So, when we type `magic`, our shell looks in those directories for the program `magic`.

Because our program does not exist in any of those directories, the shell throws an error:
```
$ magic
zsh: command not found: magic
```

However, when we specify the LOCATION of our program (the PATH to the directory in which it is located - in this case, the current directory, specified as `./`), the shell is able to find, and execute that program:
```
$ ./magic
ABRA!
```

If `magic` was located in a child directory (`spells`), we would have needed to specify that path:
```
$ ./spells/magic
```

---





