# Shell Scripts

Let's create a shell script!

A shell script is simply a program / command that our shell can carry out ("execute").

---
## Setup
Let's use a scratch / sandbox directory:

```
$mkdir ~/blah
```

Let's navigate to that directory:
```
$ cd ~/blah
```

Now let's create a file called `magic`
```
$ touch magic
```

Note: this is a shell script, so we could name it `magic.sh`, but file extensions are not necessary for shell scripts / executable files.


And using a code editor of your choosing, add this to the file:


```
#! /bin/bash
# Prints ABRA!

echo "ABRA!"
```
Don't forget to save the file.

---
## Shebang
```
#! interpreter [optional-args]
```
- `#!` this character sequence is known as the SHEBANG
  - white space after `#!` is optional
- `interpreter` indicates the interpreter
  - the absolute path to an executable program


```
#!/bin/sh       Execute the file using the Bourne shell (or compatible shell)
#!/bin/bash     Execute the file using the Bash shell

```

----
## Execution (Part 1)
Now let's execute our shell script

```
$ magic
```

We get this error:
```
$ magic
zsh: command not found: magic
```

We need, instead, to specify the PATH to our file.


---
## Execution (Part 2)
Let's use tab completion to access our file:
```
$ ./m<TAB>
```

We should see this:
```
$ ./magic
```

Press `<ENTER>`

You should see this error:
```
$ ./magic
zsh: permission denied: ./magic
```

This means that the file is not able to executed.

This is an issue with the PERMISSIONS on that file.

We do not have permission to `execute` that file.

---
## Inspect permissions
Let's inspect the permissions on our file:
```
$  lsa magic
-rw-r--r--  1 danielmoi  staff  42 22 Apr 11:55 magic
```

This tells us that we are unable to execute the file.

We will look deeper into permission in a later [lesson](/permissions.md)

----
## Change Permissions

To change our file permissions we will use the `chmod` command.

```
$ chmod 755 magic
```

Now let's try again
```
$ ./magic

ABRA!
```

Voila!

You should see `ABRA!` displayed in the terminal.

That's your first shell script!



