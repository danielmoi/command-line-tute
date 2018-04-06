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

We can even omit the `cd`:
```
$ /
```

If we try to change directories to one directory above:
```
$ cd ..
```

Nothing happens, because we are already at the top-most directory.

---
## Home directory
The home directory is the base directory for the user currently logged in to a machine.

On a Mac, my home directory is at `/Users/danielmoi`.

That is, starting from the root directory (`MacintoshHD`, referenced as `/`),
there is a `Users` directory where each user has their own home directory.

Here is a sample tree to illustrate this:

```
.
└── Users
    ├── Guest
    ├── Shared
    ├── danielmoi
    ├── pikachu
    └── snorlax
```

There are 2 home directories for Guest and Shared users.

There are also home directories for each of the 3 users (`danielmoi`, `elmo`, and `jessicajones`).

Logged in as `danielmoi`, navigating to `~` would take me to `/Users/danielmoi`.

Similarly, logged in as `pikachu`, `~` would take me to `/Users/pikachu`, and so on.

This is called TILDE EXPANSION.
