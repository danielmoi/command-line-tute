--------------------------------------------------------------------------------
## Environment Variables
`$HOME` is a environment variable - a variable that is accessible anywhere on
your machine.

We can inspect the value of it inside Vim:

```
:echo $HOME
```
We can check it from the terminal:
```
$ echo $HOME
```

For my machine (a Mac), it shows:
```
/Users/danielmoi
```

If you are using the `alpine-neovim` image, we will see
```
/root
```
