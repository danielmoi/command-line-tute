# Commands

## The command line
A quick refresher: what is the command line?

Put simply, it is a LINE IN THE TERMINAL where a user types commands for the SHELL.

_Reference: [an overview of shells, terminals, and the command line](/lessons/00-shells-terminals-command-line.md)._

----
## Our first command
Everything you type into the command line is a command (or arguments for a command).

For example, `ls`.

```
$ ls
```
`ls` stands for "list", or "list directory contents".

It produces a list produces a list of the files in the current directory.

----
## Manual pages

We can access comprehensive help for commands by browsing its MANUAL pages:

```
$ man ls
```

Note that `man` is another COMMAND.

It opens the manual pages, and `ls` is an ARGUMENT passed in, specifying the section of the manual we wish to open.


We can actually open the manual for the `man` command in the same fashion!
```
$ man man
```
----
## Executables and location
Each command that we type into the command line is also the name of a corresonding PROGRAM - an EXECUTABLE.

We can find where the `ls` lives, by using another command/program called `where`:

```
$ where ls
```

And we will get this output:
```
ls: aliased to ls -G
/bin/ls
/bin/ls
```

This tells us that
1. the `ls` command is actually aliased to `ls -G` (more about this later)
2. the `ls` program/executable lives in the `bin` directory of our ROOT directory

We can confirm this by changing directories to our ROOT directory.
```
$ cd \
```

... and then we change directory to the `bin` directory:
```
$ cd bin
```

... and then if we list the directory contents:
```
$ ls
```

... we will see this:
```
$ ls
[          date       expr       ln         pwd        sync
bash       dd         hostname   ls         rm         tcsh
cat        df         kill       mkdir      rmdir      test
chmod      domainname ksh        mv         sh         unlink
cp         echo       launchctl  pax        sleep      wait4path
csh        ed         link       ps         stty       zsh
```

... and we can see our `bin` program there!

Note that we can `ls` the contents of a specific directory from any current working directory,
by passing the PATH of that directory:
```
$ ls /bin
```

----
## Wrap up
And, something else - what happens when we type some nonsense into the command line?
```
$ blahhh
```

We get this:
```
$ blahhh
zsh: command not found: blahhh
```

Which means that the shell is trying to execute the command `blahhh`, but `blahhh` is not an available program.

The shell reports that message back to the user.

This is a good example that highlights that:

```
The command line is all about COMMANDS.
```
