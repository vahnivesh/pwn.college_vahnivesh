# 1. chaining with semicolons

### using semicolons to pass multiple commands.

**Flag:** `pwn.college{Q5qnzxYDcRIZVrtmL7FIep8_0PQ.QX1UDO0wyM3gjNzEzW}`

as per the challenge, we are suppose to run /challenge/pwn and /challenge/college togther, so we used the semicolon ; to pass multiple commands. thus got the flag.



```
hacker@chaining~chaining-with-semicolons:~$ /challenge/pwn ; /challenge/college
Yes! You chained /challenge/pwn and /challenge/college! Here is your flag:
pwn.college{Q5qnzxYDcRIZVrtmL7FIep8_0PQ.QX1UDO0wyM3gjNzEzW}
hacker@chaining~chaining-with-semicolons:~$

```

## What I learned

I learned we can pass multiple commands, using ;


## References

NIL

..................................................................

# 2. Building on Success

### chaining 2nd command if 1st command succeseds using && operator

**Flag:** `pwn.college{ES3DA6RqLdpA_r5aWcZioPWdU6b.0lM0MDOxwyM3gjNzEzW}`

as per the challenge, we are suppose to chain the command, and the /challenge/second will only run if /challenge/firs-success runs first.
so we used && to do this, and thus got the flag.



```
hacker@chaining~building-on-success:~$ /challenge/first-success
hacker@chaining~building-on-success:~$ /challenge/second
Error: /challenge/first-success must be successfully chained with
/challenge/second using &&
hacker@chaining~building-on-success:~$ /challenge/first-success && /challenge/second
Nice chaining! Flag: pwn.college{ES3DA6RqLdpA_r5aWcZioPWdU6b.0lM0MDOxwyM3gjNzEzW}
hacker@chaining~building-on-success:~$

```

## What I learned

I learned how to satisfy two conditions togther using && operator.


## References

NIL

..................................................................



# 3. Handling Failure

### handling failure using || operator

**Flag:** `pwn.college{gP41wrKuWEEcskJK6LXnfqKLyWk.01M0MDOxwyM3gjNzEzW}`

as per the challenge, we needed to run /challenge/second if /challenge/first-failure program fails, so we used || operator which is OR, and thus got the flag.



```
hacker@chaining~handling-failure:~$ /challenge/first-failure || /challenge/second
Nice chaining! Flag: pwn.college{gP41wrKuWEEcskJK6LXnfqKLyWk.01M0MDOxwyM3gjNzEzW}
hacker@chaining~handling-failure:~$

```

## What I learned

I learned what OR operator does, it basically says run second command if 1st fails, like if the 1st command runs, it would not run the second command.


## References

NIL

..................................................................



# 4. Your first shell script

### using shell script to pass multiple commands, using .sh

**Flag:** `pwn.college{gK4rmvLI-n_jjCjQGmYmbumGBoQ.QXxcDO0wyM3gjNzEzW}`

as per the challenge, we were suppose to pass `/challenge/pwn ; /challenge/college` in a file named x.sh.
at first i pasted the script in x.sh using nano `x.sh`  command
and thus got the flag.



```
hacker@chaining~your-first-shell-script:~$ nano x.sh
hacker@chaining~your-first-shell-script:~$ bash x.sh
Great job, you've written your first shell script! Here is the flag:
pwn.college{gK4rmvLI-n_jjCjQGmYmbumGBoQ.QXxcDO0wyM3gjNzEzW}
hacker@chaining~your-first-shell-script:~$

```

## What I learned

I learned how to use shell script.


## References

NIL

..................................................................



# 5. Redirecting Script Output

### Redirecting scripts output using piping and shell

**Flag:** `pwn.college{wjOMZefAHtQe03qkS5C5dKQjeEM.QX4ETO0wyM3gjNzEzW}`

as per the challenge, we were suppose to pipe the output from the run.sh and output it to /challenge/solve, did `bash run.sh | /challenge/solve` and thus got the flag.

```
hacker@chaining~redirecting-script-output:~$ cat run.sh
/challenge/pwn ; /challenge/college
hacker@chaining~redirecting-script-output:~$ ls
COLLEGE  a             not-the-flag      pwn         the-flag
Desktop  instructions  not-the-flag.bak  pwn_output  x.sh
PWN      myflag        output.sh         run.sh
hacker@chaining~redirecting-script-output:~$ ls -l run.sh
-rwxr--r-- 1 hacker hacker 36 Oct  9 17:40 run.sh
hacker@chaining~redirecting-script-output:~$ bash run.sh | /challenge/solve
Correct! Here is your flag:
pwn.college{wjOMZefAHtQe03qkS5C5dKQjeEM.QX4ETO0wyM3gjNzEzW}

```

## What I learned

got practice of using piping outputs and shell script


## References

NIL

..................................................................



# 6. Executable Shell scripts

### execuating shell scripts without bash

**Flag:** `pwn.college{UKtyTB3Ui799P-4H128h2PRo6GJ.QX0cjM1wyM3gjNzEzW}`

as per the challenge, we need to execute `script.sh` with the command `/challenge/solve` in it. 
so did chmod 777 to make it executable, readable, writable to everyone. and thus did `./script.sh` and got the flag,

```
hacker@chaining~executable-shell-scripts:~$ nano script.sh
hacker@chaining~executable-shell-scripts:~$ ls -l script.sh
-rw-r--r-- 1 hacker hacker 17 Oct  9 17:54 script.sh
hacker@chaining~executable-shell-scripts:~$ chmod 777 script.sh
hacker@chaining~executable-shell-scripts:~$ ./script.sh
Congratulations on your shell script execution! Your flag:
pwn.college{UKtyTB3Ui799P-4H128h2PRo6GJ.QX0cjM1wyM3gjNzEzW}
hacker@chaining~executable-shell-scripts:~$

```

## What I learned

I got practice of using chmod commands, and executing shell scripts without bash.


## References

NIL

..................................................................



# 7. understanding shebangs

### using shebangs to understand the commands.

**Flag:** `pwn.college{gG0luuoy5SwZd1JNafxWpFxo_tJ.0VOzMDOxwyM3gjNzEzW}`

as per the challenge we needed use shebangs, `#!/bin/bash` command, to let the linux understand its a bash command, of a script.
so we did `echo hack the planet` in solve.sh and then ran the `/challenge/run` and thus got the flag.



```
in nano.
#!/bin/bash
echo hack the planet

hacker@chaining~understanding-shebangs:~$ nano /home/hacker/solve.sh
hacker@chaining~understanding-shebangs:~$ ls -l solve.sh
-rw-r--r-- 1 hacker hacker 33 Oct  9 18:02 solve.sh
hacker@chaining~understanding-shebangs:~$ chmod 777 solve.sh
hacker@chaining~understanding-shebangs:~$ /challenge/run
Testing your script...
Perfect! Your flag:
Flag: pwn.college{gG0luuoy5SwZd1JNafxWpFxo_tJ.0VOzMDOxwyM3gjNzEzW}

```

## What I learned

I learned how to use shebangs, and for #!/bin/bash for bash commands.etc


## References

NIL

..................................................................



# 8. Scripting with agruments

### using agruments in scripts.

**Flag:** `pwn.college{YwN4D64r9lXj0zVbX2Nju_WYi9L.0VNzMDOxwyM3gjNzEzW}`

as per the challenge, we needed to ./solve.sh pwn college, but the output should be reverse order, meaning college pwn.
so we did `nano /home/hacker/solve.sh` and then did shebangs of bash and `echo $2 $1` which indicates that the 2nd agrument will echo and then 1st agrument. and then `/challenge/run` and thus got the flag.

in nano
```
#!/bin/bash
echo $2 $1

```

```
hacker@chaining~scripting-with-arguments:~$ nano /home/hacker/solve.sh
hacker@chaining~scripting-with-arguments:~$ ./solve.sh pwn college
college pwn
hacker@chaining~scripting-with-arguments:~$ /challenge/run
Correct! Your script properly reversed the arguments.
Here's your flag:
pwn.college{YwN4D64r9lXj0zVbX2Nju_WYi9L.0VNzMDOxwyM3gjNzEzW}
hacker@chaining~scripting-with-arguments:~$

```

## What I learned

I learned how to pass agruments in script using $2 and $1 etc,


## References

NIL

..................................................................

# 9. Scripting with conditionals

### passing conditional agruments in bash

**Flag:** `pwn.college{gD9nzpvqVjDjeVRixYtSGGalBij.0lNzMDOxwyM3gjNzEzW}`

as per the challenge, if the first agrument is `pwn` then the output should be `college`, in the script `./solve.sh` we write the conditional logics just like c, but for ending a `if` statement we use `fi`, and thus run the `/challenge/run` and thus get the flag.

Inside Nano.
```
#!/bin/bash
if [ "$1" == "pwn" ]
then
    echo "college"
fi

```

```
hacker@chaining~scripting-with-conditionals:~$ nano /home/hacker/solve.sh
hacker@chaining~scripting-with-conditionals:~$ ./solve.sh pwn
college
hacker@chaining~scripting-with-conditionals:~$ /challenge/run
Correct! Your script properly handles all the conditions.
Here's your flag:
pwn.college{gD9nzpvqVjDjeVRixYtSGGalBij.0lNzMDOxwyM3gjNzEzW}

```

## What I learned

I learned how to use conditions similar to c language in shell script and run it.


## References

NIL

..................................................................




# 10. scripting with default cases

### using else in conditional statements.

**Flag:** `pwn.college{0sVssR35zOhQoIzIjpk03kvZT0S.01NzMDOxwyM3gjNzEzW}`

as per the challenge, we need to check if `$1` is `pwn` then the output should be `college`, and if anything else it should be nope. and thus did that in nano, and then ran the code, `/challenge/run` and thus got the flag.


In Nano
```
#!/bin/bash
if [ "$1" == "pwn" ]
then
    echo "college"
else
    echo "nope"
fi

```

```
hacker@chaining~scripting-with-default-cases:~$ nano ./solve.sh
hacker@chaining~scripting-with-default-cases:~$ ./solve.sh pwn
college
hacker@chaining~scripting-with-default-cases:~$ ./solve.sh test
nope
hacker@chaining~scripting-with-default-cases:~$ /challenge/run
Correct! Your script properly handles the if/else conditions.
Here's your flag:
pwn.college{0sVssR35zOhQoIzIjpk03kvZT0S.01NzMDOxwyM3gjNzEzW}

```

## What I learned

I learned how to use else statements.


## References

NIL

..................................................................




# 11. Scripting with Multiple conditions

### using elif statements.

**Flag:** `pwn.college{wRNcuMnTybtf3XqrldxmFT2b608.0FOzMDOxwyM3gjNzEzW}`

as per the challenge, we did elif statements, like if `$1` if `hack` then `the planet`, if `pwn` then `college` and so on.
then ran the /challenge/run and thus got the flag.

In Nano
```
#!/bin/bash
if [ "$1" == "hack" ]
then
    echo "the planet"
elif [ "$1" == "pwn" ]
then
    echo "college"
elif [ "$1" == "learn" ]
then
    echo "linux"
else
    echo "unknown"
fi
```



```

hacker@chaining~scripting-with-multiple-conditions:~$ nano ./solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ ./solve.sh hack
the planet
hacker@chaining~scripting-with-multiple-conditions:~$ ./solve.sh pwn
college
hacker@chaining~scripting-with-multiple-conditions:~$ ./solve.sh learn
linux
hacker@chaining~scripting-with-multiple-conditions:~$ ./solve.sh test
unknown
hacker@chaining~scripting-with-multiple-conditions:~$ /challenge/run
Correct! Your script properly handles all the conditions with elif.
Here's your flag:
pwn.college{wRNcuMnTybtf3XqrldxmFT2b608.0FOzMDOxwyM3gjNzEzW}

```

## What I learned

I learned how to pass elif statements.


## References

NIL

..................................................................




# 12. Reading shell scripts.

### reading shell scripts using cat to find the password.

**Flag:** `pwn.college{o-QGjptMANj5nhLqXI93rJsGP8T.0lMwgDOxwyM3gjNzEzW}`

as per the challenge, we need to run `/challenge/run` but it has a password encoded in the bash code. and thus we use `cat /challenge/run` to read the file, and figure out that the password is `hack the PLANET` and thus typed it, and got the flag.



```
hacker@chaining~reading-shell-scripts:~$ cat /challenge/run
#!/opt/pwn.college/bash

read GUESS
if [ "$GUESS" == "hack the PLANET" ]
then
        echo "CORRECT! Your flag:"
        cat /flag
else
        echo "Read the /challenge/run file to figure out the correct password!"
fi
hacker@chaining~reading-shell-scripts:~$ /challenge/run
hack the PLANET
CORRECT! Your flag:
pwn.college{o-QGjptMANj5nhLqXI93rJsGP8T.0lMwgDOxwyM3gjNzEzW}
hacker@chaining~reading-shell-scripts:~$

```

## What I learned

I got practice of using cat commands, to read the program for hints.


## References

NIL

..................................................................


