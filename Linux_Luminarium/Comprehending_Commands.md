# cat: not the pet, but the command

### Reading the Flag in a file named flag using cat

**Flag:** `pwn.college{cMWiTczktEhpeYsaZ_Z8KK_uVVl.QXxcTN0wyM3gjNzEzW}`

in the directory, as per the challenge, the flag is copied on to a file named flag in the home directory `~`. so we use the cat command to concatenate the file.
hence giving as the flag

```
hacker@commands~cat-not-the-pet-but-the-command:~$ ls
Desktop  a  flag
hacker@commands~cat-not-the-pet-but-the-command:~$ cat flag
pwn.college{cMWiTczktEhpeYsaZ_Z8KK_uVVl.QXxcTN0wyM3gjNzEzW}
hacker@commands~cat-not-the-pet-but-the-command:~$

```

## What I learned
cat is a command used to read a file in terminal, it basically outputs the contents of that file onto to the terminal.
cat commannd be used to read multiply files if provided multiply arguments at once.


## References

NIL

..................................................................


# catting absolute paths

### Reading the Flag in a absolute path

**Flag:** `pwn.college{YPGvmCTWP11xoBLOuhNXP_lE0qn.QX5ETO0wyM3gjNzEzW}`

in the directory, as per the challenge, the flag is not exactly copied in the file. to get the flag, we should define the flag file as a absolute path using /
so when we type `cat /flag` it reads the flag inside the given absolute path, thus getting the flag

```
hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{YPGvmCTWP11xoBLOuhNXP_lE0qn.QX5ETO0wyM3gjNzEzW}
hacker@commands~catting-absolute-paths:~$

```

## What I learned
cat is a command used to read a file in terminal, it basically outputs the contents of that file onto to the terminal.
we can also cat absolute paths eg `cat /flag`
cat commannd be used to read multiply files if provided multiply arguments at once.


## References

NIL

..................................................................

# more catting practice

### catting practice

**Flag:** `pwn.college{EtH6I1mC2dd4yjDMu99ZS1uL6fY.QXwITO0wyM3gjNzEzW}`

as per the challenge, we can not use cd command to navigate to the desired directory, but instead we can take the directory as a whole absolute path and read the cat.
thus getting the flag

```
You cannot use the 'cd' command in this level, and must retrieve the flag by
absolute path. Plus, I hid the flag in a different directory! You can find it
in the file /usr/include/sepol/flag. Go cat it out **without** cding into that
directory!
hacker@commands~more-catting-practice:~$ cat /usr/include/sepol/flag
pwn.college{EtH6I1mC2dd4yjDMu99ZS1uL6fY.QXwITO0wyM3gjNzEzW}
hacker@commands~more-catting-practice:~$

```

## What I learned
cat is a command used to read a file in terminal, it basically outputs the contents of that file onto to the terminal.
cat command can process or take multiply directories, as a absolute path
cat commannd be used to read multiply files if provided multiply arguments at once.


## References

NIL

..................................................................

# grepping for a neddle in a haystack

### using grep command to search a string from a big file.

**Flag:** `pwn.college{gLRWYyWrAz95nIaauSYJTVOkuDN.QX3EDO0wyM3gjNzEzW}`

as per the challenge, we need to find the flag inside a data.txt, which is a absolute path of `/challenge/data.txt`.
we can use cat to read, but as given there are about 100 words in. and finding the flag is very hard.
so we use grep command to search for a string like a keyword to get the flag. As the hint given the flag starts with pwn.college. so typing `grep pwn.college /challenge/data.txt`
would search the string pwn.college and give all the possible results in the terminal. and thus got the flag.

```
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
pwn.college{gLRWYyWrAz95nIaauSYJTVOkuDN.QX3EDO0wyM3gjNzEzW}
hacker@commands~grepping-for-a-needle-in-a-haystack:~$

```

## What I learned
to find a string or a keyword in the big data, we can use grep command.
grep command basically searches for the given string in the absolute path or the data file.
grep command helps in reducing the time to find a keyword(eg pwn.college, would give all the words named as it in terminal) in case a big data type instead of cat.

## References

NIL

..................................................................


# comparing files

### comparing files and finding the difference in them

**Flag:** `pwn.college{YPGvmCTWP11xoBLOuhNXP_lE0qn.QX5ETO0wyM3gjNzEzW}`


```


```

## What I learned



## References

NIL

..................................................................
