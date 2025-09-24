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
**Flag:** `pwn.college{4-up_KVcLH2X2JXSQHemeDkkkV7.QX5QTN0wyM3gjNzEzW}}`

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







