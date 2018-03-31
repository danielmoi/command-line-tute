## Curl

----
Curl some files

-L, --location      Follow redirects (H)
-O, --remote-name   Write output to a local file named like the remote file

-k, --insecure      Allow connections to SSL sites without certs (H)
-s, --silent        Silent mode (don't output anything)
-S, --show-error    Show error. With -s, make curl show errors when they occur

curl -Lks http://bit.do/cfg-init | /bin/bash
```


# This will output the file to terminal
curl https://raw.githubusercontent.com/danielmoi/dotfiles/master/.aliases.public.sh

Instead of specifying the file name like this:
curl https://raw.githubusercontent.com/danielmoi/dotfiles/master/.aliases.public.sh > .aliases.public.sh

We can use the same file name as the incoming file:
curl -LO https://raw.githubusercontent.com/danielmoi/dotfiles/master/.aliases.public.sh
