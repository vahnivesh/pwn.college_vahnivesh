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







