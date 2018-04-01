# Finder App

The Finder app is the graphical user interface (GUI) counterpart to browsing and navigating directories in the command line (using `cd` and `ls`).

Here are some tips for switching between the two.

----
## Hidden files
The first step in making Finder more dev-friendly is to enable displaying hidden files.

Hidden files begin with a period (`.`), such as `.zshrc` or `.gitignore` files.

The easiest way is a keyboard shortcut in the latest release of macOS:
```
SHIFT + CMD + .
```

Voila!

---
The previous way was to do this:
```
$ defaults write com.apple.finder AppleShowAllFiles YES
```

And then to relaunch Finder (OPT-click Finder icon > Relaunch)

---
## Command line > Finder
Navigate to the desired directory.
```
$ open .
```

Say we navigated to `/Users/danielmoi/Documents` in the command line.

NB. This is the same as entering `~/Documents`.

We are taken to that directory inside the Finder application!


----
## Finder > Command line
Focus the directory in Finder (single click).

Copy that directory (either `CMD-C` or right-click > Copy)

Paste directly into command line.

```
$ /Users/danielmoi/Documents
```

We are taken to that directory inside the command line!
