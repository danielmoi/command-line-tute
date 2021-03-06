# Overview

Ok, let's start with an overview.


## Shells, Terminals, and Command Lines

You may have heard of these terms: the "shell", the "terminal", and the "command line".

What do these mean?

Let's step back and start with mainframes...


---
## Mainframes
Mainframes are physically large computers.

An example of a old mainframe:

![Mainframe](/images/mainframe-1.gif)



Mainframes still exist today, and are used for high-volume, processor-intensive computing.

They are "central" computers, in the sense that many users can connect to them.

Each user connects to the mainframe through a terminal

---
## Terminal
A terminal is a physical device with a monitor and a keyboard.

A terminal provides a text input/output environment in which a user can interact with a mainframe.

As such, a terminal is a piece of hardware, located remotely from the mainframe.

A user at a terminal:

![Terminal](/images/terminal-1.jpg)

---
## Console
A console is special sort of terminal - it is directly connected to the mainframe via a console port.

It's where the operating system of the mainframe would print error and log messages.

Users at a console:

![Console](/images/console-1.jpg)

---
## Shell
A shell is software (a computer program).

It runs in the terminal.

The shell takes commands typed by a user into the terminal and executes them.

The eventual execution of these commands is done by the kernel - the shell is a layer (an interface) between the user and the internal parts of the operating system.

Examples of these commands:
- program execution (launch a program)
- input / output (list the files inside a directory)

There are many different shells.

In the unix universe, there is:
- `bash` (the default shell for Ubuntu, and other Linux distributions),
- `zsh` (which emphasizes power and customizability),
- `fish` (which emphasizes simplicity)

---
## Kernel
The kernel is a program that constitutes the central core of a computer's operating system.

It has complete control over everything that happens in the computer.

It is very "low level" (interacting with a kernel requires using instructions very close to machine code). Because of this, the shell is provided to allow users to interact with the kernel in an easier way.


---
## Command Line Interface
A command-line interface (CLI) is a means of interacting with a computer program, allowing the user to issue commands to the program using lines of text (command lines).

Input source = keyboard.

A CLI is where the user types commands.

The "command prompt" (or, prompt) is the character(s) that appears on the screen, indicating that the program is ready to receive user input.

As such, the "shell prompt" is the command prompt for the shell, and it usually ends with a `$`.

```
$
```

The command prompt:

![Command Prompt](/images/command-prompt.png)


The "command line" is the space to the right of the command prompt, and is where the user types commands.
![Command Line](/images/command-line.png)


---
## Graphic User Interface
A graphical user interface (GUI) is another means of interacting with a computer program, allowing the user to issue commands to the program using graphical elements, such as a pointer controlled by a mouse / trackpad.

Input source = mouse / trackpad.

The Finder application on a Mac is an example of a GUI.

---
## Consoles Today
Nowadays, the console can be a _virtual_ console.

Example: the Console application on MacOS, which continuously logs out messages from the Mac operating system.

![Console Mac](/images/console-mac.png)

---
## Terminals Today
A terminal today can also be a _virtual_ device - software that emulates a physical terminal.

It is more correct to use the term "terminal emulator" for a virtual terminal, but it is common
to just use the term "terminal".

As such, a terminal now is a wrapper program that runs a shell (another program).

Example: the Terminal application on MacOS (running Bash shell)

![Terminal Mac Terminal](/images/terminal-terminal.png)

Example: iTerm (running Zsh shell)

![Terminal iTerm](/images/terminal-iterm.png)

SSH is another example of a terminal - it connects a terminal on one machine with programs on another machine.


---
## Summary
So, to bring it all together, in the context of a modern Mac laptop,
- the "mainframe" would be the laptop itself
- the "shell" would be Bash, the default shell installed on a Mac
- the "terminal" would be the Terminal application (each tab would be a new "terminal")
- the "console" would be the Console application

The USER _types_ COMMANDS into the COMMAND LINE of the TERMINAL.

These commands are _executed_ by the SHELL, in interaction with the KERNEL.

The shell then displays relevant output in the terminal, such as data or a success/failure code.


----
Hopefully, this article has helped you understand shells, terminals, and command lines - and a few other terms along the way!


---
###  References
https://askubuntu.com/questions/506510/what-is-the-difference-between-terminal-console-shell-and-command-line

http://www.linfo.org/shell.html
