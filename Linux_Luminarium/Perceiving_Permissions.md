# 1. Changing file ownership

### changing file ownerships using chown command

**Flag:** `pwn.college{cHhRrv39rzrf4BoDrbRKlGuIqTz.QXxEjN0wyM3gjNzEzW}`

as per the challenge, we need to enter the privelaged access, we can not do `cat /flag` since, we are in hacker and the permission access is given to root user.
so we do `chown hacker /flag` to change the permission of root to hacker user and then do `cat /flag`, and thus get the flag.



```
hacker@permissions~changing-file-ownership:~$ ls -l /flag
-r-------- 1 root root 60 Oct  1 20:20 /flag
hacker@permissions~changing-file-ownership:~$ cat /flag
cat: /flag: Permission denied
hacker@permissions~changing-file-ownership:~$ chown hacker /flag
hacker@permissions~changing-file-ownership:~$ ls -l /flag
-r-------- 1 hacker root 60 Oct  1 20:20 /flag
hacker@permissions~changing-file-ownership:~$ cat /flag
pwn.college{cHhRrv39rzrf4BoDrbRKlGuIqTz.QXxEjN0wyM3gjNzEzW}
hacker@permissions~changing-file-ownership:~$

```

## What I learned

I learned how to change file ownership using chown command.


## References

NIL

..................................................................

# 2. Groups and files

### 

**Flag:** `pwn.college{sj0dQEdFntOOuKDrMwSHf-yPmhz.QXxcjM1wyM3gjNzEzW}`



```

hacker@permissions~groups-and-files:~$ id
uid=1000(hacker) gid=1000(hacker) groups=1000(hacker)
hacker@permissions~groups-and-files:~$ chgrp hacker /flag
hacker@permissions~groups-and-files:~$ cat /flag
pwn.college{sj0dQEdFntOOuKDrMwSHf-yPmhz.QXxcjM1wyM3gjNzEzW}

```

## What I learned


## References

NIL

..................................................................



# 3. fun with group names

### 

**Flag:** `pwn.college{AgZ3ybihwJHLzgGdLrZc0aFUOGv.QXycjM1wyM3gjNzEzW}`



```
hacker@permissions~fun-with-groups-names:~$ id
uid=1000(hacker) gid=1000(grp23704) groups=1000(grp23704)
hacker@permissions~fun-with-groups-names:~$ whoami
hacker
hacker@permissions~fun-with-groups-names:~$ cat /flag
cat: /flag: Permission denied
hacker@permissions~fun-with-groups-names:~$ chgrp grp23704 /flag
hacker@permissions~fun-with-groups-names:~$ cat /flag
pwn.college{AgZ3ybihwJHLzgGdLrZc0aFUOGv.QXycjM1wyM3gjNzEzW}
hacker@permissions~fun-with-groups-names:~$

```

## What I learned


## References

NIL

..................................................................



# 4. changing permissions

### 

**Flag:** `pwn.college{whD0teOAgeI51ptnyDgbE3Xb9hy.QXzcjM1wyM3gjNzEzW}`



```
hacker@permissions~changing-permissions:~$ cat /flag
cat: /flag: Permission denied
hacker@permissions~changing-permissions:~$ ls -l /flag
-r-------- 1 root root 60 Oct  1 20:36 /flag
hacker@permissions~changing-permissions:~$ chmod go-u+r /flag
hacker@permissions~changing-permissions:~$ ls -l /flag
-r--r--r-- 1 root root 60 Oct  1 20:36 /flag
hacker@permissions~changing-permissions:~$ cat /flag
pwn.college{whD0teOAgeI51ptnyDgbE3Xb9hy.QXzcjM1wyM3gjNzEzW}
hacker@permissions~changing-permissions:~$

```

## What I learned


## References

NIL

..................................................................



# 5. excecutable files

### 

**Flag:** `pwn.college{Y68Spcc6N2Ws7Ig4x0CYOzbHixb.QXyEjN0wyM3gjNzEzW}`



```
hacker@permissions~executable-files:~$ ls -l /challenge/run
-r--r--r-- 1 hacker hacker 32 Jan 14  2025 /challenge/run
hacker@permissions~executable-files:~$ chmod u+x /challenge/run
hacker@permissions~executable-files:~$ ls -l /challenge/run
-r-xr--r-- 1 hacker hacker 32 Jan 14  2025 /challenge/run
hacker@permissions~executable-files:~$ /challenge/run
Successful execution! Here is your flag:
pwn.college{Y68Spcc6N2Ws7Ig4x0CYOzbHixb.QXyEjN0wyM3gjNzEzW}
hacker@permissions~executable-files:~$

```

## What I learned


## References

NIL

..................................................................



# 6. permission tweaking practice

### 

**Flag:** `pwn.college{EtsHBxUY08vVOP-99qz8UkfCNSq.QXwEjN0wyM3gjNzEzW}`



```
hacker@permissions~permission-tweaking-practice:~$ /challenge/run
Round 1 of 8!

Current permissions of "/challenge/pwn": rw-r--r--
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": rwxr-xr-x
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
* the group does have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
* the world does have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod 755 /challenge/pwn
You set the correct permissions!
Round 2 of 8!

Current permissions of "/challenge/pwn": rwxr-xr-x
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
* the group does have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": rwxr-xrwx
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
* the group does have execute permissions
* the world does have read permissions
* the world does have write permissions
* the world does have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod 757 /challenge/pwn
You set the correct permissions!
Round 3 of 8!

Current permissions of "/challenge/pwn": rwxr-xrwx
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
* the group does have execute permissions
* the world does have read permissions
* the world does have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": rwxrwxrwx
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
* the world does have read permissions
* the world does have write permissions
* the world does have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod 777 /challenge/pwn
You set the correct permissions!
Round 4 of 8!

Current permissions of "/challenge/pwn": rwxrwxrwx
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
* the world does have read permissions
* the world does have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": ---rwx---
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod 070 /challenge/pwn
You set the correct permissions!
Round 5 of 8!

Current permissions of "/challenge/pwn": ---rwx---
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": ----w----
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
* the group does have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod 020 /challenge/pwn
You set the correct permissions!
Round 6 of 8!

Current permissions of "/challenge/pwn": ----w----
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
* the group does have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": r-xrwxr-x
* the user does have read permissions
- the user doesn't have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
* the world does have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod 575 /challenge/pwn
You set the correct permissions!
Round 7 of 8!

Current permissions of "/challenge/pwn": r-xrwxr-x
* the user does have read permissions
- the user doesn't have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": r-x-wx--x
* the user does have read permissions
- the user doesn't have write permissions
* the user does have execute permissions
- the group doesn't have read permissions
* the group does have write permissions
* the group does have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
* the world does have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod 531 /challenge/pwn
You set the correct permissions!
Round 8 of 8!

Current permissions of "/challenge/pwn": r-x-wx--x
* the user does have read permissions
- the user doesn't have write permissions
* the user does have execute permissions
- the group doesn't have read permissions
* the group does have write permissions
* the group does have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": ----wx--x
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
* the group does have write permissions
* the group does have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
* the world does have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod 031 /challenge/pwn
You set the correct permissions!
You've solved all 8 rounds! I have changed the ownership
of the /flag file so that you can 'chmod' it. You won't be able to read
it until you make it readable with chmod!

Current permissions of "/flag": ---------
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod 400 /flag
hacker@permissions~permission-tweaking-practice:~$ cat /flag
pwn.college{EtsHBxUY08vVOP-99qz8UkfCNSq.QXwEjN0wyM3gjNzEzW}
hacker@permissions~permission-tweaking-practice:~$

```

## What I learned


## References

NIL

..................................................................



# 7. permission setting practice

### 

**Flag:** ``



```


```

## What I learned


## References

NIL

..................................................................



# 8. the SUID Bit

### 

**Flag:** ``



```


```

## What I learned


## References

NIL

..................................................................
