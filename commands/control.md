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


----
## B. Logical Operators
## B1. `&&`
## B2. `||`
## B3. `!`

----
## C. Pipe Operator
See [pipe operator](/commands/pipe.md)
