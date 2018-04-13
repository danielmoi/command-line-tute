# Shell Scripts

Let's create a shell script!

Create a file called `magic.sh`

```
#! /bin/bash
# Prints ABRA!

echo "ABRA!"
```

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
Save it.

Now let's execute it.

```
$ ./m<TAB>
```

With autocompletion, we should see:
```
$ ./magic.sh
```

Press `<ENTER>`

You should see this error:
```
$ ./magic.sh
zsh: permission denied: ./magic.sh
```

This means that the file is not able to executed.

----
## Permissions


Let's use the `chmod` command.

