# The Root

### invoke the pwn program using its absolute path
**Flag:** `pwn.college{UNf7TZOGLLquS4zIYXSFw8HQCRo.QX4cTO0wyM3gjNzEzW}`

the '/' indicates the root directory, and suppose when typed with a /your_filename then it becomes the absolute path.
Meaning in this, the root searches for a "your_filename" in the directory and excute it if present.
In this case, when typed pwn as a absolute path, it finds the excutable file and run it, hence giving the flag
```
hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{UNf7TZOGLLquS4zIYXSFw8HQCRo.QX4cTO0wyM3gjNzEzW}
hacker@paths~the-root:~$
```

## What I learned

Absolute paths start with '/' and point to a specific file from the root. eg `/pwn`.
I also learnt what a root directory is and how we can access different files and directories from the terminal.

## References

NIL

..................................................................

# Porgram and absolute paths

### execute the program using its absolute path
**Flag:** `pwn.college{UN8plLGxAv340qW8xibCI3KOxeD.QX1QTN0wyM3gjNzEzW}`


since `/challenge/run` is an absolute path, executable run inside the /challenge directory so invoking /challenge/run runs that specific program which prints the flag.


```
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{UN8plLGxAv340qW8xibCI3KOxeD.QX1QTN0wyM3gjNzEzW}
hacker@paths~program-and-absolute-paths:~$
```

## What I learned

Absolute paths start with '/' and point to a specific file from the root.
We can also specifying an absolute path ensures that it run's the exact file you intended. eg `/challenge/run`.

## References

NIL

..................................................................

# Postion thy shelf

### execute the program at a specific path using cd(change directory)
**Flag:** `pwn.college{c9vGM5J-xuJUEQeavNWQzKdTDV8.QX2QTN0wyM3gjNzEzW}`


at first we are in ~ directory, using cd we are navigating to /usr, once entered in this /usr, we need enter `/usr/share/doc` to enter in the specific directory where the program is to be runned.
once reaching we just invoked the absolute path which is `/challenge/run` and got the flag.

```
hacker@paths~position-thy-self:~$ cd /usr
hacker@paths~position-thy-self:/usr$ cd /usr/share/doc
hacker@paths~position-thy-self:/usr/share/doc$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{c9vGM5J-xuJUEQeavNWQzKdTDV8.QX2QTN0wyM3gjNzEzW}
```

## What I learned

Absolute paths start with '/' and point to a specific file from the root.
I learned to use cd(change directory) to navigate through directories, and run the program, eg(cd /usr)

## References

NIL

..................................................................

# Postion elsewhere

### execute the program at a specific path using cd(change directory)
**Flag:** `pwn.college{8GbsdOekPCCTuJV_u5AWKmOFLNS.QX3QTN0wyM3gjNzEzW}`

as simlar to the previous challenge, the location(path has not changed).
at first we are in ~ directory, using cd we are navigating to /usr, once entered in this /usr, we need enter `/usr/share/doc` to enter in the specific directory where the program is to be runned.
once reaching we just invoked the absolute path which is `/challenge/run` and got the flag.

```
hacker@paths~position-thy-self:~$ cd /usr
hacker@paths~position-thy-self:/usr$ cd /usr/share/doc
hacker@paths~position-thy-self:/usr/share/doc$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{8GbsdOekPCCTuJV_u5AWKmOFLNS.QX3QTN0wyM3gjNzEzW}
```

## What I learned

Absolute paths start with '/' and point to a specific file from the root.
I learned to use cd(change directory) to navigate through directories, and run the program, eg(cd /usr)

## References

NIL

..................................................................

# Postion yet elsewhere

### execute the program at a specific path using cd(change directory)
**Flag:** `pwn.college{Y1O_335S06iafB1Yt22TYLeDiKs.QX4QTN0wyM3gjNzEzW}`

at first we are in ~ directory,we need enter `cd /etc` to enter in the specific directory where the program is to be runned.
once reaching we just invoked the absolute path which is `/challenge/run` and got the flag.

```
hacker@paths~position-yet-elsewhere:~$ cd /etc
hacker@paths~position-yet-elsewhere:/etc$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{Y1O_335S06iafB1Yt22TYLeDiKs.QX4QTN0wyM3gjNzEzW}

```

## What I learned

Absolute paths start with '/' and point to a specific file from the root.
I learned to use cd(change directory) to navigate through directories, and run the program, eg(cd /etc)

## References

NIL

..................................................................


# Implicits relative paths, from\

### execute the program at a specific path in our cwd(curret working directory)
**Flag:** `pwn.college{4-up_KVcLH2X2JXSQHemeDkkkV7.QX5QTN0wyM3gjNzEzW}`

at first we are in ~ directory,we need enter `cd /` to enter in the specific directory where the program is to be runned.
now since the challeneg/run is a relative path we just enter `challenge/run` and will get the flag

```
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{4-up_KVcLH2X2JXSQHemeDkkkV7.QX5QTN0wyM3gjNzEzW}

```

## What I learned

relative paths do not require '/' and point to a specific file from the root.
I learned to use cd(change directory) to navigate through directories, and run the program, eg(cd /)

## References

NIL

..................................................................

# explicit relative paths, from\

### execute the program at a specific path in our cwd(curret working directory) using relative path
**Flag:** `pwn.college{4YYkOZtUNZrYmPRIyAEpPhSCv5j.QXwUTN0wyM3gjNzEzW}`

at first i faced issues while understanding the challenge, I intitally, took `/challenge/run`, but then i understood, that we are suppose to invoke it in the right directory which is `/` directory.
once i `cd /`. it asked for the relative path, but I was typing absolute path which was `/challenge/run` so i corrected and typed `./challenge/run` then i got flag

```
hacker@paths~explicit-relative-paths-from-:~$ /challenge/run
Incorrect...
You are not currently in the / directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$
hacker@paths~explicit-relative-paths-from-:/$ /challenge/run
Incorrect...
You invoked this challenge with an absolute path. This challenge needs a relative path!
hacker@paths~explicit-relative-paths-from-:/$ .challenge/run
bash: .challenge/run: No such file or directory
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{4YYkOZtUNZrYmPRIyAEpPhSCv5j.QXwUTN0wyM3gjNzEzW}

```

## What I learned

relative paths do not require '/' and point to a specific file from the root.
i learnt that in the previous problem our relative path was "naked": it directly specified the directory to descend into from the current directory. we can reference in paths: (.) and (..). ., refers right to the same directory, so the following absolute paths are all identical to each other.

## References

NIL

..................................................................


# Implicit relative path

### execute the program at a specific path using ./
**Flag:** `pwn.college{ExkgTMFRuvyQXdiBYfwzSwolpqy.QXxUTN0wyM3gjNzEzW}`

at first we are in ~ directory. we need to navigate to challenge, using `cd /challenge` we have reached it.
to run the program it must be a relative path. 
so we type `./run` which sucessfully fetches us the flag.

```
hacker@paths~implicit-relative-path:~$ /challenge/run
Incorrect...
You are not currently in the /challenge directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ /challenge/run
Incorrect...
You invoked this challenge with an absolute path. This challenge needs a relative path!
hacker@paths~implicit-relative-path:/challenge$ ./challenge/run
bash: ./challenge/run: No such file or directory
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{ExkgTMFRuvyQXdiBYfwzSwolpqy.QXxUTN0wyM3gjNzEzW}

```

## What I learned

relative paths start with `./`
I learnt that if Linux searched the current directory for programs every time we entera naked path, we could accidentally execute programs in our current directory that happened to have the same names as core system utilities.

## References

NIL

..................................................................


# Home sweet home

### In this challenge, /challenge/run will write a copy of the flag to any file we specify as an argument on the commandline, with these constraints: 1.Your argument must be an absolute path. 2.The path must be inside your home directory. 3.Before expansion, your argument must be three characters or less.

**Flag:** `pwn.college{oqckB5L5xAhPG1XO4gLiCi5VVBj.QXzMDO0wyM3gjNzEzW}`

using `pwd` we found that ~ is just our default home directory which is `home/hacker` 
when i typed `/challenge/run ~/abc` it said "The argument you provided must not have been longer than 3 characters (it's
currently 5 characters long)!"
thats when i understood that ~/ is also considered as a characters, so i typed `/challenge/run  ~/a` and thus got the flag

```
hacker@paths~home-sweet-home:~$ /challenge/run
You must provide an argument to /challenge/run when you invoke it!
hacker@paths~home-sweet-home:~$ pwd
/home/hacker
hacker@paths~home-sweet-home:~$ /challenge/run ~/abc
The argument you provided must not have been longer than 3 characters (it's
currently 5 characters long)!
hacker@paths~home-sweet-home:~$ /challenge/run ~/a
Writing the file to /home/hacker/a!
... and reading it back to you:
pwn.college{oqckB5L5xAhPG1XO4gLiCi5VVBj.QXzMDO0wyM3gjNzEzW}
hacker@paths~home-sweet-home:~$ ls
Desktop  a
hacker@paths~home-sweet-home:~$ cat a
pwn.college{oqckB5L5xAhPG1XO4gLiCi5VVBj.QXzMDO0wyM3gjNzEzW}
```

## What I learned
I learnt that ~$ is the shortform for /home/hacker , or the default directory I also learnt that ~ is an absolute path, and only the leading ~ is expanded. 
cd uses ~ as default directory.

## References

NIL

..................................................................







