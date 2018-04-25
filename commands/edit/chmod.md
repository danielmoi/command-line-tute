# `chmod`

## Name
Change File Modes (or Access Control Lists)


----
## Usage
```
$ chmod [permissions] [filename]
```

The `permissions` argument has 3 components:
- permission target (user, group, others, all) `[ugoa]`
- permission action (grant/revoke) `+` or `-`
- permission type (read,write,execute) = `[rwx]`

----
## Description
The `chmod` utility modifies the file mode bits of the listed files as specified by the mode operand.

It may also be used to modify the Access Control Lists (ACLs) associated with the listed files.


---
## Examples
Grant execute permission to current user
```
$ chmod u+x file.sh
```

Grand read, write, and execute permission to file user group
```
$ chmod g+rwx file.sh
```

Grant execute permission to all users
```
$ chmod +x file.sh
```

Revoke execute permission to all users
```
$ chmod -x file.sh
```

---
## Examples (using shorthand)
If we wanted to set permissions for each of the 3 user groups, we would have to do this one group at a time, one permission action at a time:
```
$ chmod u+rwx file.sh
$ chmod g+rw file.sh
$ chmod g-x file.sh
$ chmod a+r file.sh
$ chmod a-wx file.sh
```

Instead, we can use a shorthand method, by using the OCTAL number system.

The octal number system uses the digits 0 to 7.

For a given user group, with the 3 file actions, there are 8 possible combinations.
Fortuitously, we can employ a single octal digit to represent this:
```
Octal     Binary      Permission set
0         0 0 0       ---
1         0 0 1       --x
2         0 1 0       -w-
3         0 1 1       -wx
4         1 0 0       r--
5         1 0 1       r-x
6         1 1 0       rw-
7         1 1 1       rwx
```


For the 3 different user groups, there are 24 possible combinations.
We can represent the elected permission set for these 3 groups with 3 octal digits.

---
So, to implment this:
- current user: read, write, executable permission (`rwx`, or `7`)
- user group: nothing (`---`, or `0`)
- others: nothing (`---`, or `-0`)

That is, we would use `700`:
```
$ chmod 700 file.sh
```

---
For scripts there are 2 common number sequences:
- `755`
  - user: read, write, execute
  - user group: read, execute
  - others: read, execute
- `700`
  - user: read, write, execute
  - user group: none
  - others: none


Use `755` when you want everybody to be able to read and execute the file (and for you to be able to write / edit the file).

Use `700` if you want the script to be private (only you can read, write, and execute the file).


---
## References
https://ryanstutorials.net/linuxtutorial/permissions.php
