# The Root

### nvoke the pwn program using its absolute path
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

Absolute paths start with '/' and point to a specific file from the root. eg `/pwn`

## References

NIL

..................................................................
