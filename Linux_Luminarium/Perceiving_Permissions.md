# 1. Changing file ownership

### 

**Flag:** `pwn.college{cHhRrv39rzrf4BoDrbRKlGuIqTz.QXxEjN0wyM3gjNzEzW}`



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

**Flag:** ``



```


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
