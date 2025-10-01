# 1. Listing Processes

### listing out processes using ps command

**Flag:** `pwn.college{Ubxqs-Tp4utU1V-6GW7RPtUsf8c.QX4MDO0wyM3gjNzEzW}`

as per the challenge, we do not know which file has a the flag in, but is running it the terminal so we will use ps aux or ps -ef to get the processes snapshots.
so we did `ps aux` in that we got `/challenge/11872-run-15104`. and thus got the flag.



```
hacker@processes~listing-processes:~$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.0  0.0   1056   640 ?        Ss   16:57   0:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-works
root           7  0.0  0.0 231708  2560 ?        S    16:57   0:00 /run/dojo/bin/sleep 6h
root         132  0.0  0.0   4132  2560 ?        S    16:57   0:00 /challenge/11872-run-15104
root         135  0.0  0.0   2744  1600 ?        S    16:57   0:00 sleep 6h
hacker       147  0.0  0.0  36972 21440 ?        Sl   16:57   0:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.
hacker       161  0.0  0.0 231576  3520 pts/1    Ss   16:57   0:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-inte
hacker       167  0.0  0.0 231940  4160 pts/1    S    16:57   0:00 /run/dojo/bin/bash --login
hacker       226  0.0  0.0 231940  4160 pts/0    Ss+  17:00   0:00 /run/dojo/bin/bash --login
hacker       245  0.0  0.0 233600  3840 pts/1    R+   17:04   0:00 ps aux
hacker@processes~listing-processes:~$ /challenge/11872-run-15104
Yahaha, you found me! Here is your flag:
pwn.college{Ubxqs-Tp4utU1V-6GW7RPtUsf8c.QX4MDO0wyM3gjNzEzW}
Now I will sleep for a while (so that you could find me with 'ps').
^C

```

## What I learned

I learned how to list out processes in terminal, using ps command.


## References

NIL

..................................................................

# 2. Killinng Processes

### killing processes using kill command

**Flag:** `pwn.college{My4NgTToXAA54IkiVZ1sVm56A7o.QXyQDO0wyM3gjNzEzW}`

as per the challenge, we are suppose to get the flag from /challenge/run but it wont run unless /challenge/dont_run is running in background.
we need to kill it and then run it so, we will use kill command. first we need to find the PID(parent proccess ID) so to do that we did `ps aux`.
in that we saw it is PID 136, so we did `kill 136` and then ran the command `/challenge/run` and thus got the flag.



```
hacker@processes~killing-processes:~$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.4  0.0   1056   640 ?        Ss   17:14   0:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-works
root           7  0.2  0.0 231708  2560 ?        S    17:14   0:00 /run/dojo/bin/sleep 6h
root         135  0.0  0.0   5204  3520 ?        S    17:14   0:00 su -c /challenge/.launcher hacker
hacker       136  0.0  0.0 231576  3520 ?        Ss   17:14   0:00 /challenge/dont_run
hacker       137  0.0  0.0 231708  2560 ?        S    17:14   0:00 sleep 6h
hacker       148  0.4  0.0  36972 21760 ?        Sl   17:14   0:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.
hacker       151  0.5  0.0 231576  3520 pts/0    Ss   17:14   0:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-inte
hacker       157  0.0  0.0 231940  4160 pts/0    S    17:14   0:00 /run/dojo/bin/bash --login
hacker       168  0.0  0.0 231940  4160 pts/1    Ss+  17:14   0:00 /run/dojo/bin/bash --login
hacker       178  0.0  0.0 233600  3840 pts/0    R+   17:14   0:00 ps aux
hacker@processes~killing-processes:~$ kill 136
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{My4NgTToXAA54IkiVZ1sVm56A7o.QXyQDO0wyM3gjNzEzW}
hacker@processes~killing-processes:~$

```

## What I learned

I learned how to use kill command.


## References

NIL

..................................................................

# 3. Interrupting Processes

### interrupting processes using ^c command

**Flag:** `pwn.college{cCJm3uLimTCCh9bTVgWw9CfsfCA.QXzQDO0wyM3gjNzEzW}`

as per the challenge, we had to run the progran /challenge/run and we need to do ^c to interrupt it, thus got the flag.



```
hacker@processes~interrupting-processes:~$ /challenge/run
I could give you the flag... but I won't, until this process exits. Remember,
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{cCJm3uLimTCCh9bTVgWw9CfsfCA.QXzQDO0wyM3gjNzEzW}
hacker@processes~interrupting-processes:~$

```

## What I learned

I learned how to use ^c


## References

NIL

..................................................................


# 4. Killing Misbehaving Processes 

### 

**Flag:** ``



```


```

## What I learned


## References

NIL

..................................................................


# 5. Suspending Processes

### 

**Flag:** ``



```


```

## What I learned


## References

NIL

..................................................................


# 6. Resuming Processes

### 

**Flag:** ``



```


```

## What I learned


## References

NIL

..................................................................


# 7. Background Processes

### 

**Flag:** ``



```


```

## What I learned


## References

NIL

..................................................................


# 8. foreground Processes

### 

**Flag:** ``



```


```

## What I learned


## References

NIL

..................................................................


# 9. Starting Background Processes 

### 

**Flag:** ``



```


```

## What I learned


## References

NIL

..................................................................


# 10. Process Exit Codes

### 

**Flag:** ``



```


```

## What I learned


## References

NIL

..................................................................
