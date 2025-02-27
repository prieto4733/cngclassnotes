# Lab 4
---


1a. /dev/null is a file that you can use to dispose of output you redirect to it.

1b. That command that list /etc is and saves the output:

``` bash
    ls /etc > ~/etc-contents.txt
```

1c. Same command but discarding error messeges:

```bash
    ls /etc > ~/etc-contents.txt 2> /dev/nullw
```

1d. The difference between > and >> is that > will save the output but if 
    runned again will overwrite the content thus errasing the first output.
    But >> in the other hand will append outputs and will not errase anything.
    I imagine that appending is needed when you need to save the outputs if the 
    command needs to run more than one time.

2c. The three modes in vi are edit mode, command mode, visual mode. In my opinion 
    I count normal mode because this mode is where the full power of vi reside.

2d. The difference between :w and :x is that running :w only will write or save 
    the file but will not exit vim, and :x will save and exit vim.

2e. The command that deletes the current line is dd and you need to be in normal
    mode.

2f. The way I would replace is with was is by running the command:

```bash
    :s/is/was/g
```

2h. The keys that allow you to move around are hjkl. h to move left, j down, k up 
    and l right.


