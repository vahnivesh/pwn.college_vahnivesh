# 1. Learning from Documentation

### invoking the challenge using the right agrument

**Flag:** `pwn.college{QU8B_r7fK58kP4mBZuiMQCwRbwZ.QX0ITO0wyM3gjNzEzW}`

so as per the challenge, we need to pass a agrument of a program `/challenge/challenge` the agrument is that `--giveflag` so we get the flag.
```
hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{QU8B_r7fK58kP4mBZuiMQCwRbwZ.QX0ITO0wyM3gjNzEzW}
hacker@man~learning-from-documentation:~$

```

## What I learned
i learned that if a documentation is there, to run it we would use the agrument. eg `--giveflag`
## References

NIL

..................................................................

# 2. Learning complex usage

### invoking complex agruments

**Flag:** `pwn.college{IF3ghSeQm3wgSSS0-RuIUF20puX.QX1ITO0wyM3gjNzEzW}`

In this challenge i had to first pass a aagrument using `--printfile`. i did it wrong many times, buti finally ran the program `/challenge/challenge --printfile /flag` which gave the flag.



```
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /challenge/flag
Correct argument! Here is the /challenge/flag file:
cat: /challenge/flag: No such file or directory
hacker@man~learning-complex-usage:~$ cat /challenge/flag
cat: /challenge/flag: No such file or directory
hacker@man~learning-complex-usage:~$ cat flag
cat: flag: No such file or directory
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{IF3ghSeQm3wgSSS0-RuIUF20puX.QX1ITO0wyM3gjNzEzW}

```

## What I learned
i learned how to pass complex agruments like `--printfile.`

## References

NIL

..................................................................


# 3. Reading Manuals

### reading manuals using the man command

**Flag:** `pwn.college{YZzXH66la7dyEePtg0Su1gLGR__.QX0EDO0wyM3gjNzEzW}`

as per the challenge, we need a read the manual page for challenge (man for short). in that there will be a hint to print the flag. so at first i ran the man command as `man challenge` that gave the manual page for manual. in that in `DESCRIPTION` ` --zladye NUM
              print the flag if NUM is 667` caught my eye. it basically said if we ran the `/challenge/challenge --zladye 667` would print out the flag.
Thus i got the flag.



```
hacker@man~reading-manuals:~$ man challenge
hacker@man~reading-manuals:~$ challenge/challenge -zladye 667
bash: challenge/challenge: No such file or directory
hacker@man~reading-manuals:~$ challenge/challenge --zladye 667
bash: challenge/challenge: No such file or directory
hacker@man~reading-manuals:~$ /challenge/challenge --zladye 667
Correct usage! Your flag: pwn.college{YZzXH66la7dyEePtg0Su1gLGR__.QX0EDO0wyM3gjNzEzW}
hacker@man~reading-manuals:~$

```

## What I learned

i learned about the `man` command which basically gives the manual of libaries etc.
eg `man challenge or man yes`
man is stored in `/usr/share/man`.
if i do `man yes` . the yes page would open up, instead if i did `man /usr/share/yes` 
it would just print out garbage


## References

NIL

..................................................................



# 4. Searching Manuals

### using special commands inside manual page to search for the flag

**Flag:** `pwn.college{MWyfC0o8TOquXZD1jb8yMj8GzhL.QX1EDO0wyM3gjNzEzW}`

as per the challenge we are suppose to find the flag . reading the the manual page, but since the manual page is about 1637 lines. and reading and finding is basically impossible to do.
so we use specail commmands inside the manual page `./flag` to search for the keyword flag. `n` & `N` to go next and previous respectively. so it found 5 flag keywords in which one was ` --dtbtdnj
              This argument will give you the flag!` 

after running that with `/challenge/challenge --dtbtdnj` hence gave the flag. 

```
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$
hacker@man~searching-manuals:~$ /challenge/challenge --dtbtdnj
Initializing...
Correct usage! Your flag: pwn.college{MWyfC0o8TOquXZD1jb8yMj8GzhL.QX1EDO0wyM3gjNzEzW}
hacker@man~searching-manuals:~$

```

## What I learned
i learned how to search for keywords within a manual using `./ , n, N , ?` for searching, next result, previous result, searching backwards respectively. 

## References

NIL

..................................................................


# 5. Searching for manuals

### searching for manuals using man commands

**Flag:** `pwn.college{kSdiqAtd_ens5baW584lPpJkCtT.QX2EDO0wyM3gjNzEzW}`

as per the challenge the manual for the challenge has some other hidden name. to find that at first we did `man man` to go to manual page of man. in that we found a command which said finding a content inside a manual page. which is basically `man -k challenege` which gave a output of `kdiqtdensb` doing `man kdiqtdensb` i found a ` --kdiqtd NUM
              print the flag if NUM is 558` 

so i did  `/challenge/challenge --kdiqtd 558` and thus got the flag.




```
hacker@man~searching-for-manuals:~$ man -k challenge
kdiqtdensb (1)       - print the flag!
hacker@man~searching-for-manuals:~$ man kdiqtdensb
hacker@man~searching-for-manuals:~$ /challenge/challenge --kdiqtd 558
Correct usage! Your flag: pwn.college{kSdiqAtd_ens5baW584lPpJkCtT.QX2EDO0wyM3gjNzEzW}
hacker@man~searching-for-manuals:~$

```

## What I learned
i learned how to search for manuals using keywords, going `man man` and using `man -k keyword`


## References

NIL

..................................................................

# 6. Helpful Programs

### using documentations for man less pages using --help or -h

**Flag:** `pwn.college{EEdYlY-TMqhw2ZoPDOvVk07cE1L.QX3IDO0wyM3gjNzEzW}`

as per the challenge, using /challenge/challenge --help to get the help page.  after reading the optional agruments it said about `-g value` and `-p print_value` so first i did `/challenge/challenge -p` the value then i got secret value as 207, then i did `/challenge/challenge -g 207` and thus got flag

```
hacker@man~helpful-programs:~$ help challenge
bash: help: no help topics match `challenge'.  Try `help help' or `man -k challenge' or `info challenge'.
hacker@man~helpful-programs:~$ /challenge --help
bash: /challenge: Is a directory
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v]
                                            [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g
                        option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 207
hacker@man~helpful-programs:~$ /challenge/challenge -g 207
Correct usage! Your flag: pwn.college{EEdYlY-TMqhw2ZoPDOvVk07cE1L.QX3IDO0wyM3gjNzEzW}

```

## What I learned

i learned how to use --help and other optional arguments.


## References

NIL

..................................................................

# 7. Help for builtins

### invoking the flag using builtins

**Flag:** `pwn.college{gYAVtqmEFDw9WwHLy6PXTDfGDLl.QX0ETO0wyM3gjNzEzW}`

as per the challenge, using builtins we are suppose to get the documentation of challenge.
using `help challenge` gave the builtin command for the challenge.
in that there was `--secret VALUE` which prints the flag if the value is correct. then the ran the command `challenge --secret gYAVtqmE` to get the flag.




```
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!

    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "gYAVtqmE".
hacker@man~help-for-builtins:~$ challenge --secret gYAVtqmE
Correct! Here is your flag!
pwn.college{gYAVtqmEFDw9WwHLy6PXTDfGDLl.QX0ETO0wyM3gjNzEzW}

```

## What I learned
i learned what buitins are, and how to invoke them and read them

## References

NIL

..................................................................
