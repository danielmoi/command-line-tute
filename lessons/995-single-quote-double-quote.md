# Single Quotes vs Double Quotes


## Single Quotes
Everything inside single quotes is interpreted literally.

Single quotes completely protect a string from the shell.

Here, `$SHELL` is not interpreted as an ENVIRONMENT VARIABLE:
```
$ echo 'My shell is $SHELL'
My shell is $SHELL
```

Here, `!` is not interpreted as HISTORY MATCH:
```
$ echo 'Hello!'
Hello!
```




---
## Double Quotes
Double quotes allow VARIABLE EXPANSION - they allow the use of variables.

Variables and special characters will be expanded / interpreted.

Here, `$SHELL` IS interpreted as an ENVIRONMENT VARIABLE:
```
$ echo "My shell is $SHELL"
My shell is /usr/local/bin/zsh
```

In this example:
```
$ echo "Hello!"
dquote>
```

The shell has interpreted that line as if there was only one double-quote character (`"`).

This is because `!` expands to the last command starting with `"` (which is nothing - we haven't started a command with `"`)

It was as if this was typed:
```
$ echo "Hello
```


This is why we have to use 2 double quotes (but the `!` is not output, because it is interpreted):
```
$ echo "Hello!""
Hello
```

---
## History Substitution / History Match / History Expansion
`!` starts a history substitution (for an "event" - a line in the command history).

For example, `!ls` expands to the last command beginning with `ls`

```
$ ls -la
$ !ls
$ ls -la
```

`!ls` is expanded to `ls -la` and that is returned to standard output (the command line), but without being executed (the cursor is placed after `-la`, allowing edits)


