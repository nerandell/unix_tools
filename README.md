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

➜  ~ who mom likes
ankitchandawala ttys000  Apr  3 13:15
```

## Terminal Information

### $TERM

`$TERM` is an environment variable that tell you the terminal (or terminal emulator) that you are using.

```zsh
➜  ~ echo $TERM
xterm-256color
```

### tty

Returns user's terminal name

```zsh
➜  ~ tty
/dev/ttys000
```

### stty

Used to get and set the options for a terminal device interface.

```zsh
➜  ~ stty -a
speed 38400 baud; 39 rows; 128 columns;
lflags: icanon isig iexten echo echoe echok echoke -echonl echoctl
	-echoprt -altwerase -noflsh -tostop -flusho pendin -nokerninfo
	-extproc
iflags: -istrip icrnl -inlcr -igncr ixon -ixoff ixany imaxbel iutf8
	-ignbrk brkint -inpck -ignpar -parmrk
oflags: opost onlcr -oxtabs -onocr -onlret
cflags: cread cs8 -parenb -parodd hupcl -clocal -cstopb -crtscts -dsrflow
	-dtrflow -mdmbuf
cchars: discard = ^O; dsusp = ^Y; eof = ^D; eol = <undef>;
	eol2 = <undef>; erase = ^?; intr = ^C; kill = ^U; lnext = ^V;
	min = 1; quit = ^\; reprint = ^R; start = ^Q; status = ^T;
	stop = ^S; susp = ^Z; time = 0; werase = ^W;

➜  ~ stty size
39 128
```


