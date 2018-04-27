# Permissions


When we initially created our `magic` shell script, the shell was unable to execute it:

This was because a permissions issue.

The user did not have permission to execute that file, based on the permissions settings on that file.


---
## Setup

Let's create a file with a command (ie. a shell script):

And let's use a file extension this time.

And don't forget to use TAB COMPLETION!

```
$ touch pokemon.sh
$ echo 'echo PIKACHU!' >> pokemon.sh
$ cat pokemon.sh
echo PIKACHU!
```

---
## File Actions
There are 3 things you may do with a file: read, write and execute.

There are referred to, in Linux, by a single letter each.
- r read - you may view the contents of the file.
- w write - you may change the contents of the file.
- x execute - you may execute or run the file if it is a program or script.

---
## User Groups
There are 3 user groups:
- owner - the user who owns the file (typically the creator of the file)
- group - the user group to which a file belongs
- others - all other users (the "world")


---
## Default permissions
Let's check the set of permissions created for that file, using the long list command:
```
$ ls -l pokemon.sh
-rw-r--r--   1 danielmoi  staff     42 22 Apr 11:55 pokemon.sh
```

Let's look at the string of 10 characters: `-rw-r-xr--`

The first character describes the file type
- a dash `-` means that it is a normal file
- a `d` means that it is a directory

The next 9 characters is the permission set. This describes what actions may be performed on the file, by various user groups.
- first 3 characters - the user
  - can read, write, but not execute
- next 3 characters - the user group
  - can read only
- next 3 characters - everyone else
  - can read only

You can read more about permissions [here](/chmod.md).



---
## Changing permissions
Let's allow all users to execute our shell script:
```
$ chmod 755 pokemon.sh
```

Now let's inspect the file permissions:
```
# ls -l pokemon.sh
-rwxr-xr-x   1 danielmoi  staff     42 22 Apr 11:55 pokemon.sh
```

This means that:
- the file type is a file (not a directory)
- user can read, write, execute
- user group can read and execute
- others can read and execute


Let's run our shell script!
```
$ ./pokemon.sh
PIKACHU!
```

