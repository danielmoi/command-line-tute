# Shell Scripts

Let's create a shell script!

Create a file called `hello.sh`

```
# !/bin/bash
# Prints Hello!

echo "Hello!"
```


Save it.

Now let's execute it.

```
$ ./h<TAB>
```

With autocompletion, we should see:
```
$ ./hello.sh
```

Press `<ENTER>`

You should see this error:
```
$ ./hello.sh
zsh: permission denied: ./hello.sh
```

This means that the file is not able to executed.

----
## Permissions

