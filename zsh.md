# Zsh

```
man zsh
```

## Description
Zsh is a UNIX command interpreter (shell) usable as an interactive login shell
and as a shell script command processor.

Of the standard shells, zsh most closely resembles ksh, but includes many
enhancements.

## Files
Note that we should not source `.bash_profile` because it's a file meant to be
read only by bash, which is not compatible with zsh.
Best to move common ENV vars out and source those from both `.bash_profile` and
`.zshrc`.


## Scripts
The syntax of zsh is similar to bash.

The shell that runs the scripts is the one indicated in the first line, the
shebang line. For example, if the script starts with #!/bin/bash,
it will be executed by bash (even if your default shell is zsh).
[source](https://unix.stackexchange.com/questions/38172/switching-to-zsh-are-all-bash-scripts-compatible-with-zs://unix.stackexchange.com/questions/38172/switching-to-zsh-are-all-bash-scripts-compatible-with-zsh)
[source](http://slopjong.de/2012/07/02/compatibility-between-zsh-and-bash/)
