# 1. the path variable

### using PATH="" to remove commands.

**Flag:** `pwn.college{QSRkTOqaUpllFFQmX-3EO8YPs6b.QX2cDM1wyM3gjNzEzW}`

as per the challenge, if we do `/challenge/run` it would remove `/flag`, and thus we will lose the flag, so we need to remove first the rm command, so we `PATH="rm"` and thus then `/challenge/run` and thus got the flag.



```
hacker@path~the-path-variable:~$ ls
COLLEGE  a             not-the-flag      pwn         script.sh  x.sh
Desktop  instructions  not-the-flag.bak  pwn_output  solve.sh
PWN      myflag        output.sh         run.sh      the-flag
hacker@path~the-path-variable:~$ /challenge/run
Trying to remove /flag...
Uh oh, looks like I successfully removed the flag! That means you did not
properly set PATH to keep me from finding 'rm'. Since the flag is gone, you
will need to re-launch the challenge from the module page! Better luck next
time.
hacker@path~the-path-variable:~$
                                                                                                                                                                                                                                                                                                        Connected!
hacker@path~the-path-variable:~$ PATH="rm"
hacker@path~the-path-variable:~$ /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: command not found
The flag is still there! I might as well give it to you!
pwn.college{QSRkTOqaUpllFFQmX-3EO8YPs6b.QX2cDM1wyM3gjNzEzW}
hacker@path~the-path-variable:~$

```

## What I learned

I learned how to remove commands from path using PATH="" command


## References

NIL

..................................................................

# 2. setting Path

### setting path using PATH=

**Flag:** `pwn.college{sSxe0kVCekVn4OQdVjinmPY1rT2.QX1cjM1wyM3gjNzEzW}`

as per the challenge, we need to run `/challenge/run` which only runs using `win` but is stored inside `/challenge/more_commands/` so we will blank that using `PATH=/challenge/more_commands/` and then ran the code `/challenge/run` and thus got the flag.



```
hacker@path~setting-path:~$ PATH=/challenge/more_commands/
hacker@path~setting-path:~$ /challenge/run
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{sSxe0kVCekVn4OQdVjinmPY1rT2.QX1cjM1wyM3gjNzEzW}
hacker@path~setting-path:~$

```

## What I learned

I learned we can add actual paths in PATH=


## References

NIL

..................................................................



# 3. Finding commands.

### finding commands using which command

**Flag:** `pwn.college{Eyt5Q9esb7Y-H-rQYRiTfFy2Wnz.01NzEzNxwyM3gjNzEzW}`

as per the challenge, we are suppose to find the command win, in that same directory the flag is stored, so we did `which win` which gave the directory after cd there, i did `cat ./flag` and thus got the flag



```
hacker@path~finding-commands:~$ which win
/challenge/paths/31299/win
hacker@path~finding-commands:~$ cd /challenge/paths/31299/
hacker@path~finding-commands:/challenge/paths/31299$ cat ./flag
pwn.college{Eyt5Q9esb7Y-H-rQYRiTfFy2Wnz.01NzEzNxwyM3gjNzEzW}
hacker@path~finding-commands:/challenge/paths/31299$

```

## What I learned

I learned how to use which command to find other commands.


## References

NIL

..................................................................



# 4. adding commands

### adding commands

**Flag:** `pwn.college{0xw-_expZcK7UZABaA_BNOxTNx2.QX2cjM1wyM3gjNzEzW}`

as per the challenge, i first did `nano win` and wrote the script, and exited,.
then did `chmod 777 win` to make it read,write ex for all.
then i put `PATH=/home/hacker`.
then did `/challenge/run` and thus got the flag.


Inside nano win:

```
!#/bin/bash
read flag < /flag
echo "$flag"

```

```

hacker@path~adding-commands:~$ pwd
/home/hacker
hacker@path~adding-commands:~$ nano win
hacker@path~adding-commands:~$ nano win
hacker@path~adding-commands:~$ cat win
!#/bin/bash
read flag < /flag
echo "$flag"
hacker@path~adding-commands:~$ chmod 777 win
hacker@path~adding-commands:~$ PATH=/home/hacker
hacker@path~adding-commands:~$ /challenge/run
Invoking 'win'....
/home/hacker/win: line 1: !#/bin/bash: No such file or directory
pwn.college{0xw-_expZcK7UZABaA_BNOxTNx2.QX2cjM1wyM3gjNzEzW}
hacker@path~adding-commands:~$
```

## What I learned

I got practice of using shell scripts.


## References

NIL

..................................................................



# 5. Hjacking commands

### 

**Flag:** ``



```


```

## What I learned


## References

NIL

..................................................................
