# Where am I?

At the moment, your terminal is showing this:
```
~ $
```

Some important things displayed in this line:
1. Location = we are in the `~` directory
2. Command prompt = the `$`
  - this indicates that the shell is ready to receive commands
3. Command line = the space after the command prompt
  - we type our commands here


---
## Directories
Directories are folders.

They hold a collection of files and/or other directories.

Some important directories:
1. Root directory
2. Home directory
3. Current working directory


---
## Root directory
The root directory is the top-most parent directory on a machine.

This is the "Macintosh HD" folder in the Finder.

We can navigate to this directory with the `/` symbol.

```
$ cd /
```

If we try to change directories to one directory above:
```
$ cd ..
```

Nothing happens, because we are already at the top-most directory.

