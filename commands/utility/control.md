# Control Operators

## Name
Control operators

## Description
The control operators are tokens that perform control functions.

Control operators allow you to control the flow and execution of commands.

---
## A. List Terminators

## A1. `;` (semicolon)
The `;` token just separates commands.

The next command will run, after the previous command completes (regardless of the exit code).
```
$ command1; command2
```
- `command1` is launched in the foreground
- `command1` completes
- `command2` is launched in the foreground
- `command2` will run regardless of whether `command1` succeeds.

## A2. `&` (ampersand)
The `&` token will run a command in the background, and start running the next command in the foreground (without waiting for the previous command to exit)

```
$ command1 & command2
```
- `command1` is launched in the background
- `command2` is launched in the foreground

----
## B. Logical Operators
## B1. `&&` (AND)
`&&` is used to build AND lists - allowing you to run a command only if another command exits successfully
```
$ command1 && command2
```
- `command1` is launched in the foreground
- `command1` completes successfully (exit code 0)
- `command2` is launched in the foreground

This command is equivalent to:
```
$ if command1
then command2
else false
fi
```

Also:
```
$ if command1; then command2; fi
```

----
## B2. `||` (OR)
`||` is used to build OR lists - allowing you to run a command only if another command exits unsuccessfully (fails).

```
$ command1 || command2
```
- `command1` is launched in the foreground
- `command1` fails (exit code other than 0)
- `command2` is launched in the foreground

This command is equivalent to:
```
$ if command1
then true
else command2
fi
```

Also:
```
$ if ! command1; then command2; fi
```


----
## B3. `!` (NOT)
This is used to negate the return status of a command (return `0` if the command returns a nonzero status, return `1` if it returns the status `0`)

```
! command1
```
NB. there must be a `SPACE` after the `!` (`!` is used for history autocompletion, when immediately followed by characters)


----
## C. Pipe Operator
See [pipe operator](/commands/pipe.md)

----
## D. Test
The `test` command.

If `~/.zshrc` exists, print 'REAL FILE' to stdout.
```
$ test -f ~/.zshrc & echo 'REAL FILE'
```

Shorthand, we can use the square brackets: `[ ]`:
```
$ [ -f ~/.zshrc ] && echo 'REAL FILE'
```
