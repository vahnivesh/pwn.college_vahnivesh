# 1.Becoming root with su 

### becoming root user using su command

**Flag:** `pwn.college{YVr_XsDErhMevHZ9jNlnBlxbY4E.QX1UDN1wyM3gjNzEzW}`

as per the challenge, we need to enter the root using su command, and then do /flag, but before entering we need to enter the password which is `hack-the-planet`
and then did cat /flag, and thus got the flag.



```
hacker@users~becoming-root-with-su:~$ su flag
su: user flag does not exist
hacker@users~becoming-root-with-su:~$ su
Password:
su: Authentication failure
hacker@users~becoming-root-with-su:~$ su
Password:
root@users~becoming-root-with-su:/home/hacker# cat /flag
pwn.college{YVr_XsDErhMevHZ9jNlnBlxbY4E.QX1UDN1wyM3gjNzEzW}
root@users~becoming-root-with-su:/home/hacker#

```

## What I learned

I learned how to use su to enter into root command.


## References

NIL

..................................................................


# 2. other users using su

### entering other root users

**Flag:** `pwn.college{w0U4j0NgkYnE15-nTrxW5h90z7D.QX2UDN1wyM3gjNzEzW}`

as per the challenge, we need to enter the root user as zardus and run `/challenge/run`,
so at first we did `su zardus` and gave the password which was `dont-hack-me` and then /challenge/run and thus got the flag.




```
hacker@users~other-users-with-su:~$ su zardus
Password:
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{w0U4j0NgkYnE15-nTrxW5h90z7D.QX2UDN1wyM3gjNzEzW}
zardus@users~other-users-with-su:/home/hacker$

```

## What I learned

I learned we can enter other users by entering `su username`.


## References

NIL

..................................................................


# 3. Cracking Passwords

### cracking passwords using john the ripper.

**Flag:** `pwn.college{ckqrFUSzv0PpAqiVTGW8vDnMs5z.QX3UDN1wyM3gjNzEzW}`

as per the challenge, there are hash password for zardus, to enter the root and enter /challenge/run,
so at first we need to find the password, so first we cd to /challenge.
then we do `john ./shadow-leak` and thus got the password which is `aardvark`
and then enter the root using `su zardus` and then run `/challenge/run` and thus got the flag.



```
hacker@users~cracking-passwords:/challenge$ cat shadow-leak
root:*:20182:0:99999:7:::
daemon:*:20182:0:99999:7:::
bin:*:20182:0:99999:7:::
sys:*:20182:0:99999:7:::
sync:*:20182:0:99999:7:::
games:*:20182:0:99999:7:::
man:*:20182:0:99999:7:::
lp:*:20182:0:99999:7:::
mail:*:20182:0:99999:7:::
news:*:20182:0:99999:7:::
uucp:*:20182:0:99999:7:::
proxy:*:20182:0:99999:7:::
www-data:*:20182:0:99999:7:::
backup:*:20182:0:99999:7:::
list:*:20182:0:99999:7:::
irc:*:20182:0:99999:7:::
gnats:*:20182:0:99999:7:::
nobody:*:20182:0:99999:7:::
_apt:*:20182:0:99999:7:::
systemd-timesync:*:20357:0:99999:7:::
systemd-network:*:20357:0:99999:7:::
systemd-resolve:*:20357:0:99999:7:::
mysql:!:20357:0:99999:7:::
messagebus:*:20357:0:99999:7:::
sshd:*:20357:0:99999:7:::
hacker::20357:0:99999:7:::
zardus:$6$fdpHIQFjxv7rqYkS$pe/fYuf1wmeJ7P27.2a/7gNp9cz5XonldHsdYBqsN/ypyc1LsI1drB5qem5gsvCq5CcqLs2vL5AU1pQ3lbHIP.:20362:0:99999:7:::
hacker@users~cracking-passwords:/challenge$ john ./shadow-leak
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
aardvark         (zardus)
1g 0:00:00:20 100% 2/3 0.04921g/s 286.5p/s 286.5c/s 286.5C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:/challenge$ su zardus
Password:
zardus@users~cracking-passwords:/challenge$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{ckqrFUSzv0PpAqiVTGW8vDnMs5z.QX3UDN1wyM3gjNzEzW}
zardus@users~cracking-passwords:/challenge$

```

## What I learned

I learned how to use john the ripper to decrypt the hash passwords.


## References

NIL

..................................................................


# 4. Using sudo

### using sudo commands instead of su

**Flag:** `pwn.college{kBVPO7RMz8dvdA-lJJ_L7Fv48bC.QX4UDN1wyM3gjNzEzW}`

as per the challenge we need to find the flag, which in normal cat /flag which will show permission denied, and so we will use sudo to get Privileged access, and thus did sudo cat /flag and thus got the flag.



```
hacker@users~using-sudo:~$ sudo
usage: sudo -h | -K | -k | -V
usage: sudo -v [-AknS] [-g group] [-h host] [-p prompt] [-u user]
usage: sudo -l [-AknS] [-g group] [-h host] [-p prompt] [-U user] [-u
            user] [command]
usage: sudo [-AbEHknPS] [-r role] [-t type] [-C num] [-g group] [-h
            host] [-p prompt] [-T timeout] [-u user] [VAR=value]
            [-i|-s] [<command>]
usage: sudo -e [-AknS] [-r role] [-t type] [-C num] [-g group] [-h
            host] [-p prompt] [-T timeout] [-u user] file ...
hacker@users~using-sudo:~$ sudo /flag
sudo: /flag: command not found
hacker@users~using-sudo:~$ sudo cat /flag
pwn.college{kBVPO7RMz8dvdA-lJJ_L7Fv48bC.QX4UDN1wyM3gjNzEzW}
hacker@users~using-sudo:~$

```

## What I learned

I learned how to invoke sudo commands to get more privileged access.


## References

NIL

..................................................................
