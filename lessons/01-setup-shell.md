## Shell
The default Shell in MacOS is Bash.

---
## Zsh
We're going to install Zsh to use as our Shell.

Both Bash and Zsh are very powerful shells with powerful scripting support.

The Zsh script is very similar to Bash, with only small differences, but the differences
are large enough that they are not interchangeable.

Some advantages of Bash:
- more POSIX compliant, and hence avoids features that should exist in the modern shell
- more portable (because of its POSIX-compliance)


Some advantages of Zsh:
- better auto-completion
- more versatile command prompts (customizable, left- and right-prompts)
- shared command line history


---
## Oh My Zsh
We're going to use Oh My Zsh to help configure our Zsh shell.

> Oh My Zsh is an open source, community-driven framework for managing your zsh configuration.

Source code: https://github.com/robbyrussell/oh-my-zsh

Open your terminal (iTerm2!) and paste this into the command line:
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

This command will install `zsh`, install `oh-my-zsh`, and set up some basic configuration

In depth:
- we are using the command `sh`
- from the manual page for (enter `man sh` into the command line),
  ```
  -c string If  the  -c  option  is  present, then commands are read from
          string.  If there are arguments after the  string,  they  are
          assigned to the positional parameters, starting with $0.
  ```
- we can see what the command `sh` does:
  ```
  $ which sh
  /bin/bash
  ```
- this means that `bash` (the default shell) is launched, and then the commands after the option `-c` are executed
- `curl -fsSL <URL>` means we are using `curl` with these flags
  - `-f` = fail silently on remote server errors
  - `-s` = silent mode (don't show progress meter or error messages)
  - `-S` = show error messages (overrides `-s` = only hide progress meter)
  - `-L` = if the resource has changed location, then redo the request on the new location
- the bash script `install.sh` will be run locally (on your machine)
- it will install `zsh` and setup the configuration


## Plugins

## Themes

Your terminal should look like this now:
FIXME: screenshot


