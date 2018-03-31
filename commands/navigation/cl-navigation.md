# Command Line Navigation

## Find command
```
<Up>                Show the previous command
CTRL-P              Pressing <Up> again will cycle backwards through the list

[chars]<CTRL-R>     Show the first command in the Search History that match chars
                    Pressing <CTRL-R> again will cycle backwards through the matches
                    Also known as:
                    - bck-i-search
                    - Reverse Incremental Search
                    eg. cd<CTRL-R> - will show most recent command starting with "cd"

[chars]<CTRL-D>   Show all commands in the Search History that match that partial string
```

## Edit command
```
CTRL-K    Clear command line
```

## Move cursor
```
CTRL-E    End of line
CTRL-A    Beginning of line

OPT-F     Forward 1 word
CTRL-F    Forward 1 character

OPT-B     Back 1 word
CTRL-B    Back 1 character
```
