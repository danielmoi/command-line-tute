# Bash

```
man bash
```

## Description
GNU Bourne-Again SHell
(as opposed to zsh - the Z shell)

Bash is a sh-compatible command language interpreter.
It executes commands read from the standard input or from a file.

## Options
--  Signals the end of OPTIONS
    Diables further option processing
    Any arguments after the -- are treated as FILENAMES and ARGUMENTS

## Arguments

## Invocation

## Definitions

## Reserved words

## Shell Grammar

## Commends

## Quoting

---
## Parameters

### Special parameters
0     The name of the shell or shell script
      $ echo $0
      # -zsh

$     The process ID of the shell

### Shell variables - set by the sehll
HISTCMD   Number in the history list of the current command

PWD       The current working directory as set by the cd command

RANDOM    Each time this parameter is referenced, a random integer
          between 0 and 32767 is generated

### Shell variables - used by the shell
HOME      The home directory of the current user
          The value of this variable is also used when performing tilde
          expansion

PATH      The search path for commands
          A colon-separated list of directories in which the shell looks
          for commands
          The default value is system-generated
          A command value is:
          /usr/local/bin:/usr/local/sbin:/usr/bin:/usr/sbin:/bin:/sbin

PS0       The value of this parameter is expanded
          And displayed by interactive shells
          AFTER reading a command, and
          BEFORE the command is executed

PS1       The value of this parameter is expanded
          and used as the primary prompt string
          The default value is:
          \s-\v\$

PS2       The value of this parameter is expanded
          and used as the secondary prompty string
          Default value:
          >

SHELL     The full pathname to the shell

---
## Expansion


## Redirection

## Aliases

## Functions

## Arithmetic Evaluation

## Conditional Expressions

## Simple Command Expansion

## Command Execution

## Command Execution Environment

## Environment

## Exit Status

## Signals

## Job Control

## Prompting

---
## Readline
### Commands for Moving
C-f   CTRL-f  forward-char      Forward a character

C-b   CTRL-b  backward-char     Back a character

M-f   OPT-f   forward-word      Forward a word

M-b   OPT-b   back-word         Back a word

C-e   CTRL-e  end-of-line       End of line

C-a   CTRL-a  beginning-of-line Start of line

### Commands for Manipulating the History
Return        accept-line       Accept the line, regardless of cursor position

C-p   CTRL-p  previous-history  Previous command

C-n   CTRL-n  bext-history      Next command

C-r   CTRL-r  reverse-search-history

### Commands for Killing and Yanking
C-k   CTRL-k  kill-line         Kill text from cursor to end of line

C-u   CTRL-u  backward-kill-line  Kill text from cursor to start of line.
                                  Killed text is saved on the kill-ring
C-y   CTRL-y  yank                Yank the top of the kill-ring into buffer
                                  (paste last copied into command line)

---
## History

## History Expansion

---
## Shell Built-in Commands
These are commands / programs that come with Bash
Other programs, such as "ls", are their own binaries

alias               List all aliases

alias <command>     Expand alias
                    $ alias gcm
                    # gcm='git commit -m'

echo          Output the arguments, separated by spaces, followed by a newline

help          Display helpful information about builtin commands

history 10    Display the last 10 commands

pwd           Print working directoy
              Prints the absolute path of the current working directory



---
## Restricted Shell

---
## Files
/   Root directory

~   Home directory
    The absolute path is stored in the variable $HOME
    This is /Users/<username>
    Which means that these are "personal" files
    ie. for the particular user logged in


/bin/bash         The bash executable
                  The binary that create the Bash shell
                  $ which bash
                  # /usr/local/bin/bash

/etc/profile      The system-wide initialization file, executed for login shells

~/.bash_profile   The personal initialization file
                  Executed for login shells
                  Stored in the $HOME directory (for each user)
                  Used ONCE, at login

~/.bashrc         The individual per-interactive shell startup file
                  Read every time a shell is started
                  Should be kept as lightweight as possible, to reduce the
                  overhead when starting a new shell

~/.bash_logout    The individual login shell cleanup file
                  Executed when a login shell exists

~/.inputrc        Individual readline initialization file

---
## Other
bash            Change to Bash

bash --login    Change to bash
                Make bash act as if it had been invoked as a LOGIN SHELL

zsh             Change to ZSH

