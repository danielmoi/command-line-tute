## Curl

----
Curl some files

-L, --location      Follow redirects (H)
-J, --remote-header-name  Use the header-provided filename (H)
-O, --remote-name   Write output to a file named as the remote file

-k, --insecure      Allow connections to SSL sites without certs (H)
-s, --silent        Silent mode (don't output anything)
-S, --show-error    Show error. With -s, make curl show errors when they occur

curl -Lks http://bit.do/cfg-init | /bin/bash
```


# This will output the file to terminal
curl https://raw.githubusercontent.com/danielmoi/dotfiles/master/.aliases.public.sh

Instead of this:
curl https://raw.githubusercontent.com/danielmoi/dotfiles/master/.aliases.public.sh > .aliases.public.sh

Do this:
- writes output to a file
curl -JLO https://raw.githubusercontent.com/danielmoi/dotfiles/master/.aliases.public.sh
