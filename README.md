# Unix Power Tools 
This is an attempt to make a list of all the unix tools and commands that will help you make a power user. 
This is based on my reading of the book [Unix Power Tools](https://www.goodreads.com/book/show/172314.UNIX_Power_Tools).
The commands are for Darwin but most of them should work on other UNIX based operating systems too, subject to few changes.

## man

Used to format and display the on-line manual pages. Example: 
```zsh
➜  ~ man man
```

`man` by default pipes output to whatever is set in `$PAGER` environment variable.
For my system, it is `less`.

```zsh
➜  ~ echo $PAGER
less
```

## uname

Used to print operating system name. Example:

```zsh
➜  ~ uname -a
Darwin Ankits-MacBook-Pro.local 17.4.0 Darwin Kernel Version 17.4.0: Sun Dec 17 09:19:54 PST 2017; root:xnu-4570.41.2~1/RELEASE_X86_64 x86_64
Darwin
```

## who

Display who is logged in.

```zsh
➜  ~ who
ankitchandawala console  Apr  2 15:23
ankitchandawala ttys000  Apr  3 13:15

➜  ~ who am I
ankitchandawala ttys000  Apr  3 13:15
```

## Terminal Information

`$TERM` is an environment variable that tell you the terminal (or terminal emulator) that you are using.

```zsh
➜  ~ echo $TERM
xterm-256color
```
