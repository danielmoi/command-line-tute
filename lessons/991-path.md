# Path

Let's look at paths and the `$PATH` environment variable.

---
## Paths
A path is the location to a resource.

Every file and directory on a computer has their own path.

A path tells the computer where to look, in order to locate that resource.


---
## Executable path

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

When the shell receives a command, it will look in a list of directories for that program.

So, when we type `magic`, our shell will attempt to locate the program `magic` in those directories.

This list of directories is stored in a variable called `$PATH`.

`$PATH` is also called the EXECUTABLE PATH.

A list of paths to directories that hold executable files (programs).

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
## Editing $PATH (Part 1)

We can add directories to our $PATH:
```
$ export PATH=$PATH:directory
```

Where `directory` is the path of the directory we want to add.

In our case:
```
$ export PATH=$PATH=~/blah
```

Or, to use the current directory, we can use the `$PWD` environment variable (Print Working Directory):
```
$ export PATH=$PATH=$PWD
```

Note:
- `pwd` is a PROGRAM, a shell builtin / binary
- `$PWD` is an environment variable, and this is printed by the `pwd` program


Let's recheck our $PATH:
```
$ echo $PATH

/Users/danielmoi/.npm-packages/bin:/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin:/Users/danielmoi/blah
```

We can see that our current directory (which holds our new program / shell script) has been appended to the list of directories.

Now let's run our `magic` shell script:
```
$ magic

ABRA!
```

This will work in any directory now!

---
## Editing $PATH (Part 2)

Editing the $PATH like we have is not permanent - if we restart our terminal session:
```
iTerm Menu > Session > Restart session
```

And we try our `magic` command again, we get our `not found` error again:
```
$ magic

zsh: command not found: magic
```

This is because our `$PATH` edits have been temporary.

We can edit our shell configuration file.

Because we are using the `zsh` shell, this is the `~/.zshrc` file.

We will look into configuring our `.zshrc` in a later lesson.

Let's add the path to our command into the `$PATH` environment variable.

Note: use an absolute path (avoid relative paths in shell configuration files, and `$PWD` will reference the directory of the `.zshrc` file, which is not what we want)
```
export PATH=$PATH:<path-to-command>
```

For my machine, it looks like this:
```
export PATH=$PATH:/Users/danielmoi/blah
```


Now, even after restarting our terminal session / machine, our command works!

```
$ magic
ABRA!
```





