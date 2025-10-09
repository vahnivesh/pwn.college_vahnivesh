# 1. Launching screen

### using screen commands to create a virtual terminal session

**Flag:** `pwn.college{Ed9y8KRWmdIjTJIGDZ3U41PpBCt.0VN4IDOxwyM3gjNzEzW}`

as per the challenge, we need to run `screen` and then exit from there, and thus got the flag.



```
Congratulations! You're inside a screen session!
Here's your flag:
pwn.college{Ed9y8KRWmdIjTJIGDZ3U41PpBCt.0VN4IDOxwyM3gjNzEzW}
hacker@terminal-multiplexing~launching-screen:~$

```

## What I learned

I learned what screen is. 


## References

NIL

..................................................................

# 2. Detaching & attaching

### detaching and attaching using ctrl-a d

**Flag:** `pwn.college{UGPEOnwgPA28Rmls5R5MFV_aE8r.0lN4IDOxwyM3gjNzEzW}`

as per the challenge, we needed to first open `screen`, and detach using `crtl-A d` which bought us to normal terminal. and then ran /challenge/run which said that the flag is in the session, so we reattached `screen -r ` and thus got the flag.



```

hacker@terminal-multiplexing~detaching-and-attaching:~$ echo Yes! Flag is: pwn.college{UGPEOnwgPA28Rmls5R5MFV_aE8r.0lN4IDOxwyM3gjNzEzW}
Yes! Flag is: pwn.college{UGPEOnwgPA28Rmls5R5MFV_aE8r.0lN4IDOxwyM3gjNzEzW}hacker@terminal-multiplexing~detaching-and-attaching:~$


```

## What I learned

I learned how to reattach and detach


## References

NIL

..................................................................



# 3. finding sessions

### listing sessions using screen -ls command.

**Flag:** `pwn.college{AjniRwVlOK9kkmq_fIew3bSxIT3.01N4IDOxwyM3gjNzEzW}`

we did `screen -ls` to list out all the session with id, and then got the actual session hidden with the flag, which was `144.session_c24218b7a4fa361c ` using `screen -r 144.session_c24218b7a4fa361c ` and thus got the flag.

```
hacker@terminal-multiplexing~finding-sessions:~$ screen -ls
There are screens on:
        164.pts-0.terminal-multiplexing~launching-screen        (Remote or dead)
        163.pts-0.terminal-multiplexing~detaching-and-attaching (Remote or dead)
        144.session_c24218b7a4fa361c    (Detached)
        147.session_d48b975c184523e1    (Detached)
        150.session_f0b8bec0ee966e42    (Detached)
5 Sockets in /home/hacker/.screen.
hacker@terminal-multiplexing~finding-sessions:~$ screen -r session_c24218b7a4fa361c
[detached from 144.session_c24218b7a4fa361c]
hacker@terminal-multiplexing~finding-sessions:~$

```

## What I learned

i learned how to list out sessions.


## References

NIL

..................................................................



# 4. Switching windows

### switching windows.

**Flag:** `pwn.college{IfH1R_fn1xAKCq8m4mnRzGrWilZ.0FO4IDOxwyM3gjNzEzW}`

as per the challeneg, it was said the flag was hidden in window 0, we were at window 1, we reached window 1 by doing `screen -r` and then did `crt-a 0` for switching to window 0 and thus got the flag.



```
hacker@terminal-multiplexing~switching-windows:~$ screen -r
[detached from 135.challenge_session]
hacker@terminal-multiplexing~switching-windows:~$

```

```

hacker@terminal-multiplexing~switching-windows:~$  cat <<MSG
> Excellent work! You found window 0!
> Here is your flag: pwn.college{IfH1R_fn1xAKCq8m4mnRzGrWilZ.0FO4IDOxwyM3gjNzEzW}
> MSG
Excellent work! You found window 0!
Here is your flag: pwn.college{IfH1R_fn1xAKCq8m4mnRzGrWilZ.0FO4IDOxwyM3gjNzEzW}
hacker@terminal-multiplexing~switching-windows:~$

```

## What I learned

I learned how to switch windows in session using crt-a [number to switch]


## References

NIL

..................................................................



# 5. detaching & attaching(tmux)

### detaching & attaching using tmux

**Flag:** `pwn.college{89EIBjZ7rRr89wVhAdWbkFefLYg.0VO4IDOxwyM3gjNzEzW}`

as per the challenge, we needed to use tmux, we did `tmux` first and then we did `/challenge/run` in which it said the flag is sent to `tmux attach 0 t` and thus got the flag,

```
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$  echo Congratulations, here is your flag: pwn.college{89EIBjZ7rRr89wVhAdWbkFefLYg.0VO4IDOxwyM3gjNzEzW}
Congratulations, here is your flag: pwn.college{89EIBjZ7rRr89wVhAdWbkFefLYg.0VO4IDOxwyM3gjNzEzW}
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$

```

```
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ tmux
[detached (from session 0)]
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ /challenge/run
Found detached tmux session: 0
Sending flag to your tmux session...

Flag sent! Now reattach to your tmux session with:
  tmux attach

You'll find the flag waiting for you there!
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ tmux attach 0
command attach-session: too many arguments (need at most 0)
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ tmux a - 0
command attach-session: too many arguments (need at most 0)
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ tmux attach0
unknown command: attach0
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ tmux attach 0
command attach-session: too many arguments (need at most 0)
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ tmux attach -t 0
[detached (from session 0)]
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$

```

## What I learned

I learned how to use tmux commands.


## References

NIL

..................................................................



# 6. Switching windows tmux

### switching windows using tmux

**Flag:** `pwn.college{E4ZjUYP7uLzvVdaZL3lzgcyeVdo.0FM5IDOxwyM3gjNzEzW}`


as per the challenge, we needed to start the `tmux` and then exit using `crt-b d` after that i did `tmux ls` in that i went to `tmux attach -t challenge_session` in that it said to go to window 0, we were currently in window 1, then i went to window 0 using `crt b 0` and thus got the flag.

In `tmux attach -t challenge_session`

```
 cat <<MSG
Welcome to the tmux window switching challenge!
You are currently in window 1.
The flag is hidden in window 0.
Use Ctrl-B 0 to switch to window 0!
MSG
hacker@terminal-multiplexing~switching-windows-tmux:~$  cat <<MSG
> Welcome to the tmux window switching challenge!
> You are currently in window 1.
> The flag is hidden in window 0.
> Use Ctrl-B 0 to switch to window 0!
> MSG
Welcome to the tmux window switching challenge!
You are currently in window 1.
The flag is hidden in window 0.
Use Ctrl-B 0 to switch to window 0!
hacker@terminal-multiplexing~switching-windows-tmux:~$
```

In `tmux window 0:`
```

> Excellent work! You found window 0!
> Here is your flag: pwn.college{E4ZjUYP7uLzvVdaZL3lzgcyeVdo.0FM5IDOxwyM3gjNzEzW}
> MSG
Excellent work! You found window 0!
Here is your flag: pwn.college{E4ZjUYP7uLzvVdaZL3lzgcyeVdo.0FM5IDOxwyM3gjNzEzW}
hacker@terminal-multiplexing~switching-windows-tmux:~$


```
```
hacker@terminal-multiplexing~switching-windows-tmux:~$ tmux ls
1: 1 windows (created Thu Oct  9 19:26:34 2025)
challenge_session: 2 windows (created Thu Oct  9 19:26:15 2025)
hacker@terminal-multiplexing~switching-windows-tmux:~$ tmux attach 0 t
command attach-session: too many arguments (need at most 0)
hacker@terminal-multiplexing~switching-windows-tmux:~$ tmux attach 1 t
command attach-session: too many arguments (need at most 0)
hacker@terminal-multiplexing~switching-windows-tmux:~$ tmux attach -t 1
[detached (from session 1)]
hacker@terminal-multiplexing~switching-windows-tmux:~$ tmux ls
1: 1 windows (created Thu Oct  9 19:26:34 2025)
challenge_session: 2 windows (created Thu Oct  9 19:26:15 2025)
hacker@terminal-multiplexing~switching-windows-tmux:~$ tmux attach -t challenge_session
[detached (from session challenge_session)]
hacker@terminal-multiplexing~switching-windows-tmux:~$

```


## What I learned

i learned how to switch tmux using crt b [0 - 9]


## References

NIL

..................................................................

