# `ps`

## Name
Process Status

----
## Usage

```
ps
```

## Options
```
a     show processes for all users

u     display the process's user/owner

x     also show processes not attached to a terminal
```


----
## Description
A utility that displays a header line, followed by lines containing information about
all of your processes that have controlling terminals.

---
## Examples

List all processes
```
ps
```
---
List all processes, for all users, with the process user/owner, and processes not attached to a terminal
```
ps aux
```

---
List all processes, and grep for 'node'. This will print only the lines that include 'node'
```
ps | grep node

23865 ttys009    0:32.25 node /Users/danielmoi/.npm-packages/...
23866 ttys009   40:47.66 node /Users/danielmoi/Documents/...
87043 ttys016    0:00.00 grep --color=auto --exclude-dir=.bzr ...
```
