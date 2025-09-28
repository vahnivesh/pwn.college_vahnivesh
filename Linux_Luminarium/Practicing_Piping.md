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

### redirecting errors using 2>

**Flag:** `pwn.college{AKhk_V7wQjrK7tzBoAI3FMyeGOT.QX3YTN0wyM3gjNzEzW}`

In this challenge to successfully to get the flag, we must standard output the output to the myflag and output the standard error to the instructions.
to do this we must use `1> or >` for standard output and `2>` for standard error.
we can also pass multiple agruments such has, we did `/challenge/run > myflag 2> instructions` and thus got the flag.



```
hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2> instructions
hacker@piping~redirecting-errors:~$ cat instructions
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will check that error output is redirected to a specific file path : instructions
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!

[TEST] You should have redirected my stderr to instructions. Checking...

[PASS] The file at the other end of my stderr looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-errors:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{AKhk_V7wQjrK7tzBoAI3FMyeGOT.QX3YTN0wyM3gjNzEzW}

```

## What I learned

I learned there are multiple file descriptor numbers. that are
FD 0 standard input.
fD 1 standard output
FD 2 standard error
`> and 1>` is basically same
we can use multiple agruments, such as eg `/challenge/run > myflag 2> instructions`


## References

NIL

..................................................................


# 5. Redirecting Inputs

### redirecting inputs using <

**Flag:** `pwn.college{0QvoJ-igEzXQl2yJDHyJZh-DIC_.QXwcTN0wyM3gjNzEzW}`

as per the challenge, we are suppose to redirect the file PWN with a value of COLLEGE in it to `/challenge/run`.
to get this we must add the value of `COLLEGE` in `PWN` file.
to do this we used echo command and standard output. using `echo COLLEGE > PWN` it was succesfull.
just to cross check i did `cat PWN` and it read `COLLEGE`. after this we are suppose to redirect to /challenge/run to standard input the value of flag.
to do this we did `/challenge/run < PWN` and thus got the flag.



```
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ cat PWN
COLLEGE
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{0QvoJ-igEzXQl2yJDHyJZh-DIC_.QXwcTN0wyM3gjNzEzW}
hacker@piping~redirecting-input:~$

```

## What I learned

I learned how to use standard inputs, which is used to redirect inputs back using `<` eg `/challenge/run < PWN`


## References

NIL

..................................................................


# 6. Grepping Stored results

### grepping stored results from redirecting outputs.

**Flag:** `pwn.college{kO-DJoeAfu7F8c8DrZp8Zl9jBGd.QX4EDO0wyM3gjNzEzW}`

in this challenge, we are suppose to redirect the outputs to a file name data.txt in a directory given. in that about 1000 words are given in that we have find the flag,(using grep).
this is very simple, i first redirected the outputs to the desired file. to do this i did `/challenge/run > /tmp/data.txt` , after this i got a confirmation saying satisfied all execution requirements.
after that to find the flag, i did `grep pwn.college /tmp/data.txt` which gave me the flag.

```
hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /tmp/data.txt
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to a file called /tmp/data.txt. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~grepping-stored-results:~$ grep pwn.college /tmp/data.txt
pwn.college{kO-DJoeAfu7F8c8DrZp8Zl9jBGd.QX4EDO0wyM3gjNzEzW}

```

## What I learned

i got a pratice of combining both redirecting outputs to a file in a directory and finding it using grep


## References

NIL

..................................................................


# 7. Grepping Live outputs.

### Grepping live outputs using pipe operator |

**Flag:** `pwn.college{g0jxihJ60ooYBQn76rbbDO3Olzn.QX5EDO0wyM3gjNzEzW}`

as per the challenge, instead of redirecting the standard outputs to a file and then grep the flag from it, to do this we used the pipe operator.
to get the flag i did `/challenge/run | grep pwm.college`. this basically inside of redirecting the outputs to file, we are searching for pwn.college simultanousesly using grep. and thus got the flag



```
hacker@piping~grepping-live-output:~$ /challenge/run | grep pwn.college
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stdout : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stdout!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{g0jxihJ60ooYBQn76rbbDO3Olzn.QX5EDO0wyM3gjNzEzW}

```

## What I learned

I learned how to use pipe operator which basically finds live outputs, instead of redirecting it to a file and then finding it.

## References

NIL

..................................................................


# 8. Grepping errors.

### 

**Flag:** `pwn.college{cgaqGsXhf5uBAUxmqXXOwOGNNLc.QX1ATO0wyM3gjNzEzW}`

as per the challenge we can grep a standard error by using pipe operator. so we will transfer the standard error to standard output using 2>&1 and then do grep using the pipe operator.
although, i hope you read this but, i think the pwn college should have given directory to run it from which is `/challenge/run` i did it, because of other challenges, so i finallly did `/challenge/run 2>&1 | grep pwn.college` and thus got the flag.



```
hacker@piping~grepping-errors:~$ /challenge/run 2>&1 | grep pwn.college
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stderr : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stderr to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stderr!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{cgaqGsXhf5uBAUxmqXXOwOGNNLc.QX1ATO0wyM3gjNzEzW}

```

## What I learned

I learned how to transfer the standard errors to standard outputs using 2>&1 and then grep the flag since pipe operator can only be used for standard outputs.


## References

NIL

..................................................................


# 9. Filtering with grep -v

### filtering out unwanted data using grep -v

**Flag:** `pwn.college{UVv5eQnBmJSKz12IN0NJX2aNutB.0FOxEzNxwyM3gjNzEzW}`

grep usually gives the words we are searching for but grep -v does the opposite, instead of finding and showing those results it basically filters them out and shows the rest.
as per the challenge, we are supposed to run /challenge/run which will give about a 1000 decoy flags with a decoy word in them. to filter that only we will use grep -v DECOY to find all the words which dont have DECOY in them so `/challenge/run | grep -v DECOY` and thus got the flag.




```
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v DECOY
pwn.college{UVv5eQnBmJSKz12IN0NJX2aNutB.0FOxEzNxwyM3gjNzEzW}
hacker@piping~filtering-with-grep-v:~$

```

## What I learned

I learned that if we need to find out the flag from a thousand decoys while live outputs, we can use `grep -v word` which basically finds out all the "word" and filter them out and show the rest.


## References

NIL

..................................................................


# 10. Duplicating piped data using tee

### using tee to read the outputs while redirecting.

**Flag:** `pwn.college{orBSswLeqS6fYJEkh9UOcy_uNuA.QXxITO0wyM3gjNzEzW}`

as per the challenge we will use tee, 
at first we need to cat pwn to get the secret key. which is `orBSswLe` then we must use `/challenge/pwn --secret orBSswLe | /challenge/college` and thus got the flag.


```
hacker@piping~duplicating-piped-data-with-tee:~$ cat pwn
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "orBSswLe"
hacker@piping~duplicating-piped-data-with-tee:~$ ^C
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret orBSswLe
Processing...
You must pipe the output of /challenge/pwn into /challenge/college (or 'tee'
for debugging).
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwm | /challenge/college
bash: /challenge/pwm: No such file or directory
/challenge/secret needs to the on the receiving end of the output of
'/challenge/pwn' (or 'tee' for debugging).
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret orBSswLe | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{orBSswLeqS6fYJEkh9UOcy_uNuA.QXxITO0wyM3gjNzEzW}

```

## What I learned

i learned about tee and how to it will printout the pipe operator.


## References

NIL

..................................................................


# 11. Process Subsitution for input

### process subsitution using >(command)

**Flag:** `pwn.college{o489ZDhC_V37vZxZHnUizHyMUEj.0lNwMDOxwyM3gjNzEzW}`

as per the challenge we are suppose the compare the outputs of two directories at the same time. we can do this by saving the file of directory 1 output and 2 output and then commparing them by diff. but ofcourse there is a faster way by using process subsitution. which is basically >(command). i did `diff >(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)` and thus got the flag

```
hacker@piping~process-substitution-for-input:~$ diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)
84a85
> pwn.college{o489ZDhC_V37vZxZHnUizHyMUEj.0lNwMDOxwyM3gjNzEzW}
hacker@piping~process-substitution-for-input:~$



```

## What I learned

I learned how to use diff and output togther using subsitution process >(command)


## References

NIL

..................................................................


# 12. Writing multiple programss

### combining tee and  subsitution process

**Flag:** `pwn.college{k2hD95iJQn70U4mDFWyynglxRZu.QXwgDN1wyM3gjNzEzW}`

as per the challenge we must run /challenge/hack output into /challenge/the and /challenge/planet simultaneously. so using subsitution process and tee to duplicate the outputs.
so i ran `/challenge/hack | tee >(/challenge/the) >(/challenge/planet)`
and thus got the flag.

```
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >(/challenge/the) >(/challenge/planet)
This secret data must directly and simultaneously make it to /challenge/the and
/challenge/planet. Don't try to copy-paste it; it changes too fast.
12914235833212319
Congratulations, you have duplicated data into the input of two programs! Here
is your flag:
pwn.college{k2hD95iJQn70U4mDFWyynglxRZu.QXwgDN1wyM3gjNzEzW}
hacker@piping~writing-to-multiple-programs:~$

```

## What I learned
I got practice of using both pipe operator tee, subsitution process

## References

NIL

..................................................................


# 13. split piping stderr and stdout

### 

**Flag:** `pwn.college{cilKFuTDI0o9vo5p1uCP52bAobq.QXxQDM2wyM3gjNzEzW}`

as per the challenge we need to only stderr output to /challenge/the and stdout to  /challenge/planet. so i did `/challenge/hack 2>>(/challenge/the) | /challenge/planet` 
thus i got the flag.

```
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack 2> >(/challenge/the) | /challenge/planet
Congratulations, you have learned a redirection technique that even experts
struggle with! Here is your flag:
pwn.college{cilKFuTDI0o9vo5p1uCP52bAobq.QXxQDM2wyM3gjNzEzW}

```

## What I learned

i got practice for stderr and stdout.

## References

NIL

..................................................................


# 14. Named pipes

### naming pipes using fifo

**Flag:** `pwn.college{QP8dtgzDss-2zO70M7jbiJGCdeN.01MzMDOxwyM3gjNzEzW}`

in this we will use First (byte) In, First (byte) Out. FIFO to create a pipe name. using mkfifo. using `mkfifo /tmp/flag_fifo` it created a fifo file there.
then i had to redirect the stdout to from /challenge/run. doing this i had to use two terminals.
as per the critera of fifo file. it must be read too while stdoutputing it. so i ran `/challenge/run > /tmp/flag_fifo` and in another terminal i did `cat /tmp/flag_fifo` which gave me the flag

```
hacker@piping~named-pipes:~$ mkfifo /tmp/flag_fifo
hacker@piping~named-pipes:~$ /challenge/run > /tmp/flag_fifo
You're successfully redirecting /challenge/run to a FIFO at /tmp/flag_fifo!
Bash will now try to open the FIFO for writing, to pass it as the stdout of
/challenge/run. Recall that operations on FIFOs will *block* until both the
read side and the write side is open, so /challenge/run will not actually be
launched until you start reading from the FIFO!
hacker@piping~named-pipes:~$


terminal 2


hacker@piping~named-pipes:~$ cat /tmp/flag_fifo
You've correctly redirected /challenge/run's stdout to a FIFO at
/tmp/flag_fifo! Here is your flag:
pwn.college{QP8dtgzDss-2zO70M7jbiJGCdeN.01MzMDOxwyM3gjNzEzW}
hacker@piping~named-pipes:~$

```

## What I learned

I learned how to name pipes using mkfifo which creates fifo files.


## References

NIL

..................................................................

