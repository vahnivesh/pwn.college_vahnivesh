# 1. Matching with *

### using glob command *

**Flag:** `pwn.college{EXbEAXo_tTD8mzTWAsj8T1WG3lV.QXxIDO0wyM3gjNzEzW}`

as per the challenge, we are suppose to cd to the challenge directory with only four characters, so we use `cd /ch*` to cd into /challenge directory since /ch consist of it. after reaching the directory, we did `/challenge/run` and those got the flag

```
hacker@globbing~matching-with-:~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{EXbEAXo_tTD8mzTWAsj8T1WG3lV.QXxIDO0wyM3gjNzEzW}
hacker@globbing~matching-with-:/challenge$

```

## What I learned

i learned how to use glob * which basically finds the similar or letter it already has

## References

NIL

..................................................................

# 2. Matching with ?

### mataching with single character.

**Flag:** `pwn.college{Yw7pHCadTMmwhT2YRKqd1uCTPTG.QXyIDO0wyM3gjNzEzW}`

as per the challenge, we are suppose to cd to /challenge without using letters c, l.
so to do this we use `?` which takes single character. so we just ran `/?ha??enge` hence it navigated to `/challenge` directory in that we ran the program `/challenge/run` to get the flag



```
Connected!
This challenge resets your working directory to /home/hacker unless you change
directory properly...
This challenge resets your working directory to /home/hacker unless you change
directory properly...
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{Yw7pHCadTMmwhT2YRKqd1uCTPTG.QXyIDO0wyM3gjNzEzW}

```

## What I learned
i leanred how to use `?` which only takes a any single character to matching

## References

NIL
..................................................................

# 3. Matching with []

### matching with a selected letters. instead of any letters.

**Flag:** `pwn.college{QdSi_5ID4Pqd3Mfhejn7va0RguW.QXzIDO0wyM3gjNzEzW}`

as per the challenge instead of taking any random letters to matching like ? we will take selected few letters file using [xyz] where x,y,z are the letters you need to match with.
so first i cd to `/challenge/files` in that i first verified if the files exist using the globbing. `echo look: file_[bash]` it gave a output of `look: file_a file_b file_h file_s` thus verifying that the files exist.
so we as per instruction of the challenge run `/challenge/run file_[bash]` and thus got the flag



```
hacker@globbing~matching-with-:~$ cd /challenge
hacker@globbing~matching-with-:/challenge$ cd ./files
hacker@globbing~matching-with-:/challenge/files$ ls
file_a  file_e  file_i  file_m  file_q  file_u  file_y
file_b  file_f  file_j  file_n  file_r  file_v  file_z
file_c  file_g  file_k  file_o  file_s  file_w
file_d  file_h  file_l  file_p  file_t  file_x
hacker@globbing~matching-with-:/challenge/files$ echo look: file_[bash]
look: file_a file_b file_h file_s
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{QdSi_5ID4Pqd3Mfhejn7va0RguW.QXzIDO0wyM3gjNzEzW}

```

## What I learned
i learned how to use [] which instead of searching for random letters to match with like ?, it searches for a selected few letters.


## References

NIL

..................................................................

# 4. Matching Paths with []

### globbing files from home directory

**Flag:** `pwn.college{wIzFoEjX3u1QCds2LB6YR6eIvwG.QX0IDO0wyM3gjNzEzW}`

as per the challenge, we needed to globb the file from /challenge/files from our home directory.
at first i did `/challenge/run /challenge/files file_[bash]` which gave a output of i need to call wiht more than one agrument. thats when i understood that the globbing of file from a other directory requires properly addressing the file location along with the files. so i did `/challenge/run /challenge/files/file_[bash]` thus giving me the flag.



```
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files file_[bash]
Error: you called this command with more than 1 argument (pre-globbing)! Please
call me with one argument.
hacker@globbing~matching-paths-with-:~$ /challenge/run file_[bash]
Error: you will need to specify the path to the files as part of your glob
argument, since they are in a different directory than your current working
directory!
hacker@globbing~matching-paths-with-:~$ /challenge/run ./files file_[bash]
Error: you called this command with more than 1 argument (pre-globbing)! Please
call me with one argument.
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{wIzFoEjX3u1QCds2LB6YR6eIvwG.QX0IDO0wyM3gjNzEzW}

```

## What I learned
i learned how to globb for the files from the home directory using proper addressing of directory along with the file.

## References

NIL

..................................................................

# 5. Multiple Globs

### globbing multiple files

**Flag:** `pwn.college{snWrgRWGdf_vRxnmGFAfh1dzJGu.0lM3kjNxwyM3gjNzEzW}`

so we need to find the flag in the `/challenge/files`. so i cd there then i run the command to `echo look: *p*` to get the all the files consisting of p in it. then i ran the `/challenge/run *p*` to get the flag.



```
hacker@globbing~multiple-globs:~$ cd /challenge/files
hacker@globbing~multiple-globs:/challenge/files$ ls
amazing      fantastic   kind        pwning     uplifting   zesty
beautiful    great       laughing    queenly    victorious
challenging  happy       magical     radiant    wonderful
delightful   incredible  nice        splendid   xenial
educational  jovial      optimistic  thrilling  youthful
hacker@globbing~multiple-globs:/challenge/files$ echo look: *p*
look: happy optimistic pwning splendid uplifting
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*'
> ^C
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{snWrgRWGdf_vRxnmGFAfh1dzJGu.0lM3kjNxwyM3gjNzEzW}
hacker@globbing~multiple-globs:/challenge/files$

```

## What I learned

i learned how to globb multi files togther.

## References

NIL

..................................................................

# 6. Mixing Globbs

### matching a file using multiple globs agruments.

**Flag:** `pwn.college{82MDTwgTJ6Gi8rirW1iwKSTKW65.QX1IDO0wyM3gjNzEzW}`

as per the challenge we need to globb a file with 6 character or less. so at first need to go the challenge/files directory using `cd /challenge/files` as per the condition the keyword must satisfy the following which are `challenging, educational, pwning` so i decided to use [cep]* using a few selected keywords including wild card search. so to verify this i get these files i did `echo look: [cep]*` which gave the output which i wanted . so we ran it as `/challenge/run [cep]*` and thus got the flag.



```
hacker@globbing~mixing-globs:~$ cd /challenge/files
hacker@globbing~mixing-globs:/challenge/files$ echo look: [cep]*
look: challenging educational pwning
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{82MDTwgTJ6Gi8rirW1iwKSTKW65.QX1IDO0wyM3gjNzEzW}
hacker@globbing~mixing-globs:/challenge/files$

```

## What I learned
I learned how to mix the globs and get a file eg `[cep]*`

## References

NIL

..................................................................

# 7. Exclusoionary Globbing

### excluding or filtering files using [!]

**Flag:** `pwn.college{QLP0gJFlvr2vPydh6amhdwZBDlQ.QX2IDO0wyM3gjNzEzW}`

at first we needed to challenge/files directory using `cd /challenge/files`. after that i needed to verify if the files are single charater files or words. using `ls` i listed all the files, and they were words. as per the challenge we need to run all the files excluding the ones having "p,w,n" so i ran the /challenge/run [!pwn]* and got the flag



```
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ ls
amazing      fantastic   kind        pwning     uplifting   zesty
beautiful    great       laughing    queenly    victorious
challenging  happy       magical     radiant    wonderful
delightful   incredible  nice        splendid   xenial
educational  jovial      optimistic  thrilling  youthful
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{QLP0gJFlvr2vPydh6amhdwZBDlQ.QX2IDO0wyM3gjNzEzW}
hacker@globbing~exclusionary-globbing:/challenge/files$

```

## What I learned
I learned that using [!something_letters] would exclude those searches and give all other files. basically a way of filtering out unwanted files.


## References

NIL

..................................................................

# 8. Tab Completion

### running commands using tab

**Flag:** `pwn.college{4alH9ZIefM9ZXmk6r7BbkLNFMX3.0FN0EzNxwyM3gjNzEzW}`

as per the challenge, it is simple we must use tab to let the linux figure out what we will type next. so first we need to go to `cd /challenge` and in that `ls` i find a pwncollege.
as per the challenge, we cant be able to cat it normally without using tab. 
so we just type `/challenge/pwn{then_tab}` and it automatically prints `/challenge/pwncollege `



```
hacker@globbing~tab-completion:~$ cd /challenge
hacker@globbing~tab-completion:/challenge$ ls
DESCRIPTION.md  pwncollege​
hacker@globbing~tab-completion:/challenge$ cat /challenge/pwncollege
cat: /challenge/pwncollege: No such file or directory
hacker@globbing~tab-completion:/challenge$ cat /challenge/pwncollege​
pwn.college{4alH9ZIefM9ZXmk6r7BbkLNFMX3.0FN0EzNxwyM3gjNzEzW}
hacker@globbing~tab-completion:/challenge$

```

## What I learned
I learned that the pressing the tab command will let the linux figure out what to type next, thus saving time and fast.

## References

NIL

..................................................................

# 9. Multiple options for tab completion

### using tab again to for tab completion for multiple results.

**Flag:** `pwn.college{8Kps6N5J-eIuZkJO8UJeP9H5jy6.0lN0EzNxwyM3gjNzEzW}`

as per the challenge, there are multiply files starting with 'pwn' so we need to press tab again to get the list of files starting from that word. so using `cat /challenge/files/pwncollege-flag`. to get the flag.



```
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ /challenge/files/pwncollege-flamigo
bash: /challenge/files/pwncollege-flamigo: No such file or directory
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat /challenge/files/pwn
pwn                    pwncollege-family      pwncollege-flyswatter
pwn-college            pwncollege-flag        pwncollege-hacking
pwn-the-planet         pwncollege-flamingo
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat /challenge/files/pwn
No flag in this file!
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat /challenge/files/pwn-college
No flag in this file!
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat /challenge/files/pwncollege-hacking
No flag in this file!
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat /challenge/files/pwncollege-flag
pwn.college{8Kps6N5J-eIuZkJO8UJeP9H5jy6.0lN0EzNxwyM3gjNzEzW}

```

## What I learned
using mulitple tabs will list out all the options of that keyword. 

## References

NIL

..................................................................

# 10. Tab completion on commands.

### using tab as a command

**Flag:** `pwn.college{wmcbpODv736PoDWWjhlScQf5N3Y.0VN0EzNxwyM3gjNzEzW}`

as per this challenge we need to use pwncollege as a command and then hit tab for the linux to complete it so. we did `pwncollege<tab>` that print `pwncollege-28046` which gave us the flag.


```
hacker@globbing~tab-completion-on-commands:~$ pwncollege-28046
Correct! Here is your flag:
pwn.college{wmcbpODv736PoDWWjhlScQf5N3Y.0VN0EzNxwyM3gjNzEzW}
hacker@globbing~tab-completion-on-commands:~$

```

## What I learned
tab can do more than just complete the files name but also complete the commands.

## References

NIL

..................................................................



