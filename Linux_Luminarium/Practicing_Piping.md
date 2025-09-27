# 1.  Redirecting Outputs.

### using > to redirect outputs.

**Flag:** `pwn.college{cuZzace1zTzc64oBuztQkWldkbx.QX0YTN0wyM3gjNzEzW}`

as per the challenge. we need to redirect a PWN in file name called COLLEGE.
to do this we will use `echo text > target_file_name` so then we will use the actually command which is `echo PWN > COLLEGE`
and thus got the flag.


```
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your
flag:
pwn.college{cuZzace1zTzc64oBuztQkWldkbx.QX0YTN0wyM3gjNzEzW}

```

## What I learned
i learned how to redirect output on to a file. basically using a echo command with a text and agrument to where to redirect it.
in this case a eg is `ehco i love cryptonite > cryptonite.txt`


## References

NIL

..................................................................

# 2. Redirecting more Outputs.

### using a path to printout outputs.

**Flag:** `pwn.college{EpfzpkKuy3jDex-2K9ettBMkN4C.QX1YTN0wyM3gjNzEzW}`

as per the challenge a path is given with a redirecting to a file named myflag. if the condition is satisfied then the code will printout the flag.
so i did first `/challenge/run > myflag`. basically redirectly my contents to myflag. it checked the conditions and then i did `cat myflag` as per instruction and got the flag.

```
hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{EpfzpkKuy3jDex-2K9ettBMkN4C.QX1YTN0wyM3gjNzEzW}

```

## What I learned

i Learned that we can even redirect of the path to a file.

## References

NIL

..................................................................

# 3. Apprending Outputs.

### outputing more than one command using >>

**Flag:** `pwn.college{kkM4jIlJwD3HHJUZNi6qLHbZOOa.QX3ATO0wyM3gjNzEzW}`

as per the challenge. there are two parts of code. if we use a `>` it would give the second half to the flag. and if we do again it will overwrite the flag with the first one.
so to avoid rewriting we will use >> which will use mulitple writes and thus will give us the full the flag. so we will use `/challenge/run >> home/hacker/the-flag`.
after that i just did `cat /home/hacker/the-flag`  and thus got the flag.



```
hacker@piping~appending-output:~$ /challenge/run >> /home/hacker/the-flag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /home/hacker/the-flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] Good luck!

[TEST] You should have redirected my stdout to a file called /home/hacker/the-flag. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
I will write the flag in two parts to the file /home/hacker/the-flag! I'll do
the first write directly to the file, and the second write, I'll do to stdout
(if it's pointing at the file). If you redirect the output in append mode, the
second write will append to (rather than overwrite) the first write, and you'll
get the whole flag!
hacker@piping~appending-output:~$ cat /home/hacker/the-flag
 |
\|/ This is the first half:
 v
pwn.college{kkM4jIlJwD3HHJUZNi6qLHbZOOa.QX3ATO0wyM3gjNzEzW}
                              ^
     that is the second half /|\
                              |

If you only see the second half above, you redirected in *truncate* mode (>)
rather than *append* mode (>>), and so the write of the second half to stdout
overwrote the initial write of the first half directly to the file. Try append
mode!
hacker@piping~appending-output:~$


```

## What I learned

I learned we can use >> to pass multiple agruments to get outputs instead of rewriting the flag.

## References

NIL

..................................................................


# 4. Redirecting errors.

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


# 7. 

### 

**Flag:** ``



```


```

## What I learned


## References

NIL

..................................................................


# 8. 

### 

**Flag:** ``



```


```

## What I learned


## References

NIL

..................................................................


# 9. 

### 

**Flag:** ``



```


```

## What I learned


## References

NIL

..................................................................


# 10. 

### 

**Flag:** ``



```


```

## What I learned


## References

NIL

..................................................................


# 11. 

### 

**Flag:** ``



```


```

## What I learned


## References

NIL

..................................................................


# 12. 

### 

**Flag:** ``



```


```

## What I learned


## References

NIL

..................................................................


# 13. 

### 

**Flag:** ``



```


```

## What I learned


## References

NIL

..................................................................


# 14. 

### 

**Flag:** ``



```


```

## What I learned


## References

NIL

..................................................................

