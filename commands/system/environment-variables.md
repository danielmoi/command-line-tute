# Environment Variables


## List of all environment variables
```sh
$ ENV
COLORTERM=truecolor
TERM=xterm-256color
...
...
```

NB. We can also do
```sh
$ env
```

We can also search for specific environment variables:
```sh
$ env | grep term
```


## $TERM
The type of terminal
```bash
$ echo $TERM
xterm
```
