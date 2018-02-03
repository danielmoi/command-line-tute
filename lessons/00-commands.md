# Introduction

What is the command line?

Put simply, it is a line in the terminal where a user types commands.

These commands are executed by the shell, in interaction with the kernel.

----
Everything you type into the command line is a command (or arguments for a command).

For example, `ls`.

It produces a list produces a list of the files in the current directory.



```
$ ls
```

And `ls` is a command!

It stands for "list", or "list directory contents".

We can find out more about the `ls` command by opening the manual pages.

```
$ man ls
```

And, yep, `man` is also a command. It opens the manual pages, and `ls` is an argument passed in, specifying the section of the manual we wish to open.


We can actually open the manual for the `man` command in the same fashion:
```
$ man man
```


And, something else - what happens when we type some nonsense into the command line?
```
$ some nonsense
```

We get this:
```
$ some nonsense
zsh: command not found: some
```

Which means that the computer is trying to process the command `some` (with the argument "nonsense"), but it is not a program that is available, so it reports back that it can't execute that command.

Everything is a command in the command line.
