# Where am I?

At the moment, your terminal is showing this:
```
~ $
```

Some important things displayed in this line:
1. Location
    - we are in the `~` directory
2. Command prompt
    - this is the "`$`"
    - this indicates that the shell is ready to receive commands
3. Command line
    - the empty spaces after the command prompt
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

Here is a sample tree to illustrate this:
```
/ (Root directory (/))
├── Applications
├── Library
├── Network
├── Users
└── var
```


---
## Home directory
The home directory is the base directory for the user currently logged in to a machine.

On a Mac, my home directory is at `/Users/danielmoi`.

That is, starting from the root directory (`MacintoshHD`, referenced as `/`),
there is a `Users` directory where each user has their own home directory.

Let's expand the previous tree to illustrate this:

```
/ (Root directory)
├── Applications
├── Library
├── Network
├── Users
│   ├── Guest
│   ├── Shared
│   ├── danielmoi (Home directory (~) when logged in as danielmoi)
│   ├── pikachu
│   └── snorlax
└── var
```

There are 5 home directories in this tree.

There are home directories for the default Guest and Shared users.

There are also home directories for each of the 3 users (`danielmoi`, `pikachu`, and `snorlax`).

Logged in as `danielmoi`, navigating to `~` would take me to `/Users/danielmoi`.

Similarly, logged in as `pikachu`, `~` would take me to `/Users/pikachu`.
Again, logged in as `snorlax`, `~` would take me to `/Users/snorlax`.

This is called TILDE EXPANSION.

The Home Directory is where "personal" files are kept for each user.
These include directories such as `Documents` and `Downloads`.

Each user has their own `Documents` and `Downloads` directories (inside their own Home Directory)

Let's expand the previous tree to illustrate this:
```
/ (Root directory)
├── Applications
├── Library
├── Network
├── Users
│   ├── Guest
│   │   ├── Documents
│   │   └── Downloads
│   ├── Shared
│   │   ├── Documents
│   │   └── Downloads
│   ├── danielmoi (Home directory (~) when logged in as danielmoi)
│   │   ├── Documents
│   │   └── Downloads
│   ├── pikachu
│   │   ├── Documents
│   │   └── Downloads
│   └── snorlax
│       ├── Documents
│       └── Downloads
└── var
```

Note: The Root Directory is really the Home Directory for the `root` user.
