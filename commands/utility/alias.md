# `alias`

## Name
Alias

---
## Usage
```
$ <alias-name>
```

---
## Description
The alias command makes it possible to use custom shortcuts/abbreviations to launch any command(s).

These command(s) are inclusive of any options, arguments and redirection.


----
## Examples

List all aliases.
```
$ alias
```

---
Inspect an alias.
```
$ alias mv
mv -i
```
This tells us that `mv` has been aliased to `mv -i`, which is the interactive flag (`-i`), so that the user is prompted if overwriting during moving a file.


---
Set an alias.
```
$ alias hello="echo HELLO"
```

We can confirm this works:
```
$ hello
HELLO
```


Note that this alias only persists for the life of a shell session.
To make an alias persist across shell sessions and reboots, the alias must be added
to the configuration file for the shell.

For `bash` shell, this is the `.bashrc` file.

For `zsh` shell, this is the `.zshrc` file.
