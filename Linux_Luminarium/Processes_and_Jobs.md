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

### killing decoy flags

**Flag:** `pwn.college{gXJbMNgihVdnDgR2IXGhzUrUafc.0FNzMDOxwyM3gjNzEzW}`

as per the challenge we are supposed to kill decoys, so at first we need to send the flag to /tmp/flag_fifo. before that we need to kill decoys program which is 142 PID, after that cat, thus got the flag.



```
hacker@processes~killing-misbehaving-processes:~$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.0  0.0   1056   640 ?        Ss   19:05   0:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-works
root           7  0.0  0.0 231708  2560 ?        S    19:05   0:00 /run/dojo/bin/sleep 6h
root         137  0.0  0.0   4132  1280 ?        S    19:05   0:00 /bin/bash /challenge/.init
root         138  0.0  0.0   4132  1280 ?        S    19:05   0:00 /bin/bash /challenge/.init
root         140  0.0  0.0   2744  1600 ?        S    19:05   0:00 sleep 6h
root         141  0.0  0.0   2744  1600 ?        S    19:05   0:00 sleep 6h
hacker       153  0.0  0.0  36972 21760 ?        Sl   19:05   0:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.
hacker       167  0.0  0.0 231972  4160 pts/0    Ss+  19:05   0:00 /run/dojo/bin/bash --login
hacker       177  0.0  0.0 231576  3520 pts/1    Ss   19:06   0:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-inte
hacker       183  0.0  0.0 231972  4160 pts/1    S    19:06   0:00 /run/dojo/bin/bash --login
hacker       205  0.0  0.0 233600  3840 pts/1    R+   19:08   0:00 ps aux
hacker@processes~killing-misbehaving-processes:~$ /challenge/run
Sending the flag to /tmp/flag_fifo!
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo
pwn.college{gXJbMNgihVdnDgR2IXGhzUrUafc.0FNzMDOxwyM3gjNzEzW}
^C

```

## What I learned

I got practice of using kill command


## References

NIL

..................................................................


# 5. Suspending Processes

### Suspending Processes using ^z command

**Flag:** `pwn.college{8716bH2PXHl7y9_V0CHzPVnBlTq.QX1QDO0wyM3gjNzEzW}`

as per the challenge we are suppose to suspend the code using ^z which suspends instead of intercepting the code, thus /challenge/run at first we suspended, then again /challenge/run and thus got the flag.



```
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         162     129  0 19:13 pts/0    00:00:00 bash /challenge/run
root         164     162  0 19:13 pts/0    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can
background me with Ctrl-Z or, if you're not ready to do that for whatever
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         162     129  0 19:13 pts/0    00:00:00 bash /challenge/run
root         169     129  0 19:13 pts/0    00:00:00 bash /challenge/run
root         171     169  0 19:13 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{8716bH2PXHl7y9_V0CHzPVnBlTq.QX1QDO0wyM3gjNzEzW}
hacker@processes~suspending-processes:~$

```

## What I learned

I learned how to susepend processes using ^z command

## References

NIL

..................................................................


# 6. Resuming Processes

### Resuming processes using fg command

**Flag:** `pwn.college{kDQaKeVAMICv7W7CbO0MnGsaf7q.QX2QDO0wyM3gjNzEzW}`

as per the challenge we need to suspend the program first and re terminate it, we need to run it first /challenge/run and then ^z to suspend it and then `fg` which resumes it and thus got the flag.



```
hacker@processes~resuming-processes:~$ /challenge/run
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with
the 'fg' command! Or just press Enter to quit me!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg
/challenge/run
I'm back! Here's your flag:
pwn.college{kDQaKeVAMICv7W7CbO0MnGsaf7q.QX2QDO0wyM3gjNzEzW}
Don't forget to press Enter to quit me!

Goodbye!
hacker@processes~resuming-processes:~$

```

## What I learned

I learned how to resume a processes using fg.


## References

NIL

..................................................................


# 7. Background Processes

### 

**Flag:** `pwn.college{YRD581DPrqzSnJPFBJ7GfmPBEVy.QX3QDO0wyM3gjNzEzW}`

as per the challenge, instead of resumming the program in foreground using fg we will resume it in bg background so we can run another copy to get the flag. 
so first we need to `/challenge/run` and suspend it using ^z and run in `bg` , using ps aux it says it runs in background, i do `/challenge/run` and thus get the flag.



```
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         163 S+   bash /challenge/run
root         165 R+   ps -o user=UID,pid,stat,cmd

I don't see a second me!

To pass this level, you need to suspend me, resume the suspended process in the
background, and then launch a new version of me! You can background me with
Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to
do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~backgrounding-processes:~$ bg
[1]+ /challenge/run &
hacker@processes~backgrounding-processes:~$


Yay, I'm now running the background! Because of that, this text will probably
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times
to scroll this text out.

hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         163 S    bash /challenge/run
root         173 S    sleep 6h
root         174 S+   bash /challenge/run
root         176 R+   ps -o user=UID,pid,stat,cmd

Yay, I found another version of me running in the background! Here is the flag:
pwn.college{YRD581DPrqzSnJPFBJ7GfmPBEVy.QX3QDO0wyM3gjNzEzW}
hacker@processes~backgrounding-processes:~$

```

## What I learned

I learned how to resume programs in background using bg.


## References

NIL

..................................................................


# 8. foreground Processes

### Practicing more of fg and bg commands.

**Flag:** `pwn.college{UBovEvcCUHnRjjD9jOZRMoiPitd.QX4QDO0wyM3gjNzEzW}`

as per the challenge we need to need to suspend program, resume the suspended process in the
background, and *then* foreground it without re-suspending it, so we first did is suspend it, then bg and then instead of suspending we did enter. and then did fg. and thus got the flag. here is a code snippet to understand more detailed.



```
hacker@processes~foregrounding-processes:~$ /challenge/run
To pass this level, you need to suspend me, resume the suspended process in the
background, and *then* foreground it without re-suspending it! You can
background me with Ctrl-Z (and resume me in the background with 'bg') or, if
you're not ready to do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~foregrounding-processes:~$ bg
[1]+ /challenge/run &
hacker@processes~foregrounding-processes:~$


Yay, I'm now running the background! Because of that, this text will probably
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times
to scroll this text out. After that, resume me into the foreground with 'fg';
I'll wait.

hacker@processes~foregrounding-processes:~$ fg
/challenge/run
YES! Great job! I'm now running in the foreground. Hit Enter for your flag!

pwn.college{UBovEvcCUHnRjjD9jOZRMoiPitd.QX4QDO0wyM3gjNzEzW}
hacker@processes~foregrounding-processes:~$


```

## What I learned

I got practice of using fg and bg commannd.


## References

NIL

..................................................................


# 9. Starting Background Processes 

### starting background processes from starting using &

**Flag:** `pwn.college{Q8xn7xUqy2fZ7s2YR6sjat6lAdT.QX5QDO0wyM3gjNzEzW}`

as per the challenge we are suppose to run the process in the background, so we did /challenge/run & and thus got the flag.



```
hacker@processes~starting-backgrounded-processes:~$ /challenge/run &
[1] 163
hacker@processes~starting-backgrounded-processes:~$


Yay, you started me in the background! Because of that, this text will probably
overlap weirdly with the shell prompt, but you're used to that by now...

Anyways! Here is your flag!
pwn.college{Q8xn7xUqy2fZ7s2YR6sjat6lAdT.QX5QDO0wyM3gjNzEzW}

[1]+  Done                    /challenge/run
hacker@processes~starting-backgrounded-processes:~$

```

## What I learned

I learned how run a program in background right from start, instead of suspending and resuming it again.


## References

NIL

..................................................................


# 10. Process Exit Codes

### exiting codes using $? command

**Flag:** `pwn.college{YWCcxUi0PJ7o02oqvG_N4jbX5DL.QX5YDO1wyM3gjNzEzW}`

as per the challenge we need to first must retrieve the exit code returned by `/challenge/get-code` and then run `/challenge/submit-code CODE` with that error code as an argument, so to get the error code, we did `echo $?` and thus got the code as 254. and then did `/challenge/submit-code 254` and thus got the flag.



```
hacker@processes~process-exit-codes:~$ /challenge/get-code
Exiting with an error code!
hacker@processes~process-exit-codes:~$ echo $?
254
hacker@processes~process-exit-codes:~$ /challenge/submit-code 254
CORRECT! Here is your flag:
pwn.college{YWCcxUi0PJ7o02oqvG_N4jbX5DL.QX5YDO1wyM3gjNzEzW}
hacker@processes~process-exit-codes:~$

```

## What I learned

I learned how to use exit codes. which is $? command.


## References

NIL

..................................................................
