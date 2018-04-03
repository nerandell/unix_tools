# Unix Power Tools 
This is an attempt to make a list of all the unix tools and commands that will help you make a power user. 
This is based on my reading of the book [Unix Power Tools](https://www.goodreads.com/book/show/172314.UNIX_Power_Tools).

## man

Used to format and display the on-line manual pages

Ex. 
```zsh
➜  ~ man man
```

`man` by default pipes output to whatever environment variable is set in `$PAGER` environment variable.
For my system, it is `less`.

```zsh
➜  ~ echo $PAGER
less
```



