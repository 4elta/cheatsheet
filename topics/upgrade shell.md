# upgrade shell

1. spawn a PTY: `python3 -c 'import pty; pty.spawn("/bin/bash")'` (same for `python`)
2. background the shell: press `ctrl+Z`
3. get the current terminal: 
```
$ echo $TERM
xterm-256color
```

4. get STTY size (i.e. `rows columns`): 
```
$ stty size
41 141
```

5. set the current STTY to type `raw` and instruct it to echo the input characters: `stty raw -echo`
6. foreground the shell: `fg`
7. reset the terminal: `reset`
8. set the shell: `export SHELL=bash`
9. set terminal type: `export TERM=<see step 3>`
10. set STTY size: `stty rows <see step 4> columns <see step 4>`
