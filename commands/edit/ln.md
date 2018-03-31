# `ln`

## Name
Make links

----
## Usage
```
ln [options] <source> <target>
```

----
## Description
The `ln` utility creates a directory entry that has the same modes as the original file.

There are 2 types of links:
- hard links (default)
  - A hard link to a file is indistinguishable from the original direc-
     tory entry
- symbolic links ("symlinks")
  - A symbolic link is revealed as such when inspecting a directory with `ls`

When a user opens the `target` file, the `source` file will be opened instead.

---
## Examples
Suppose we have `f1.md` with the text `FILE 1` inside:
```
$ echo "FILE 1" >> f1.md
```

---
## Hard Links
Let's create a hard link:
```
$ ln f1.md f1-hard-link.md
```

Let's `cat` our `f1-hard-link.md`:
```
$ cat f1-hard-link.md

FILE 1
```

Let's `ls` our directory:
```
$ ls -la

-rw-r--r--   3 danielmoi  staff     7 31 Mar 14:14 f1-hard-link.md
-rw-r--r--   3 danielmoi  staff     7 31 Mar 14:14 f1.md
```
----
## Symbolic Links
Let's create a symbolic link:
```
$ ln -s f1.md f1-symbolic-link.md
```

Let's `cat` our `f1-symbolic-link.md`:
```
$ cat f1-symbolic-link.md

FILE 1
```

Let's `ls` our directory:
```
$ ls -la

lrwxr-xr-x   1 danielmoi  staff     5 31 Mar 14:18 f1-symbolic-link.md -> f1.md
-rw-r--r--   3 danielmoi  staff     7 31 Mar 14:14 f1.md
```
We can see that our symbolic link POINTS to the original file!

This is MUCH more transparent and useful...

----
Interactive mode:
```
ln -si my-source.md my-target.md
```

- `-s` makes a symlink
- `-i` if the target file exists, warn

Now, when a user opens `my-target.md`, they will actually be opening `my-source.md`.

----

These are example commands to create symbolic links to configuration files that exist in a `~/dotfiles` directory.

This allows all the configuration files to be kept in a directory, but any programs that request the original location `~/.zshrc` will actually open the `~/dotfiles/zshrc` file!

```
ln -si ~/dotfiles/bashrc ~/.bashrc
ln -si ~/dotfiles/bash_profile ~/.bash_profile
ln -si ~/dotfiles/zshrc ~/.zshrc

ln -si ~/dotfiles/vimrc ~/.vimrc

ln -si ~/dotfiles/.env.sh ~/.env.sh
ln -si ~/dotfiles/.aliases.public.sh ~/.aliases.public.sh
ln -si ~/dotfiles/.aliases.private.work.sh ~/.aliases.private.work.sh
ln -si ~/dotfiles/.aliases.private.home.sh ~/.aliases.private.home.sh

```
## Remove Symlink
rm .vimrc
