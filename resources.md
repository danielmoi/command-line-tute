# Resources

## Useful sites
- linuxcommand.org
- Unix Stackexchange https://unix.stackexchange.com/
## Tips

- Don't feel intimidated! There's a LOT to learn about the command line, but learning just the basics is incredibly useful
- For commands that have "from" and "to" locations (eg. `cp`, `ln`, etc), remember that the order of these arguments is ALPHABETICAL
  - source > target (S ... T)
  - from > to (F ... T)

- Tab completion is your friend!


- Use the `man` command to find out more about a command
  ```
  $ man curl
  ```

- Use the `--help` flag to find out more about a command
  ```
  $ docker --help
  ```
  - sometimes sub-commands will have `help` available too!
  ```
  $ docker system --help

  $ docker system prune --help
  ```

- Make a "sandbox" / "scratch" directory to experiment in:
  ```
  $ mkdir ~/blah

  $ touch one.md two.md

  $ echo "ONE" >> one.md

  $ curl -O google.com > google.html

  # set an alias to this directory in your .zshrc
  # alias blah="cd ~/blah"
  # and have fun!
  ```
