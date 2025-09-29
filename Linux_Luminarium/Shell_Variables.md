# 1. Printing Variables

### printing flag as a variable using echo

**Flag:** `pwn.college{YqERvqxXsqoFZrmzxrqDMnyCrB4.QX3UTN0wyM3gjNzEzW}`
as per the challenge we are suppose to print the flag as a variable. we can do this using `echo $FLAG` the $ indicates the variable name. hence got the flag.


```
hacker@variables~printing-variables:~$ echo $FLAG
pwn.college{YqERvqxXsqoFZrmzxrqDMnyCrB4.QX3UTN0wyM3gjNzEzW}
hacker@variables~printing-variables:~$

```

## What I learned

I learned how to print variables using `echo $something.`


## References

NIL

..................................................................

# 2. Setting Variables

### setting up variables or assigning using '='

**Flag:** `pwn.college{8F7TA2cSCcehXDlU-_IJJl1ZMpi.QX5UTN0wyM3gjNzEzW}`

as per the challenge we need to set PWN variable the value of COLLEGE, we can do this using "=", like `PWN=COLLEGE`, so thus got the flag.



```
hacker@variables~setting-variables:~$ PWN=COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{8F7TA2cSCcehXDlU-_IJJl1ZMpi.QX5UTN0wyM3gjNzEzW}
hacker@variables~setting-variables:~

```

## What I learned

I learned how to assign values to variables with help of "=", 
we need to be careful not to add space between assigning the value. 
they are also case senstive.


## References

NIL

..................................................................

# 3. Multi word variables

### assigning multi word variables using quotes

**Flag:** `pwn.college{QTnkDddeWYYgCFAMtFgithpkc6Z.QXwYTN0wyM3gjNzEzW}`

as per the challenge we must assign the COLLEGE YEAH to PWN, but since its a multi word, we cant simply use =, we need to quote it, like
`PWN="COLLEGE YEAH"` and thus got the flag.

```
hacker@variables~multi-word-variables:~$ PWN="COLLEGE YEAH"
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{QTnkDddeWYYgCFAMtFgithpkc6Z.QXwYTN0wyM3gjNzEzW}
hacker@variables~multi-word-variables:~$


```

## What I learned

I learned how to set multi word value into a variable using quotes.


## References

NIL

..................................................................

# 4. Exporting Variables.

### exporting a variable using export command

**Flag:** `pwn.college{MfP_Gy1oHAsrVHnf4WRBvnjJlaa.QXyYTN0wyM3gjNzEzW}`

as per the challenge we must export COLLEGE value into PWN variable and not export but assign PWN value into COLLEGE variable. thus creating a inhertiance.
so at first i did export `PWN=COLLEGE` and then i did `COLLEGE=PWN` and then i did `/challenge/run PWN`
and thus got the flag.



```
hacker@variables~exporting-variables:~$ export PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ echo $PWN
COLLEGE
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run PWN
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great
job! Here is your flag:
pwn.college{MfP_Gy1oHAsrVHnf4WRBvnjJlaa.QXyYTN0wyM3gjNzEzW}
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!

```

## What I learned

I learned how to export a variable after or while assigning it a value.


## References

NIL

..................................................................

# 5. Printing exported variables

### printing exported variables using env

**Flag:** `pwn.college{IRNZ-gISxA-0pHf5ILPguYByBbR.QX4UTN0wyM3gjNzEzW}`

as per the challenge, the FLAG variable is already assigned the value of flag and exported, using env command we can print all the exported variables and found the flag.



```
hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=8cdc5728bcc7c02388bbc3b211a0df572429c6ad3235b34cd32c192bdcf82feb
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{IRNZ-gISxA-0pHf5ILPguYByBbR.QX4UTN0wyM3gjNzEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env

```

## What I learned

I learned we can print the exported variables using env command


## References

NIL

..................................................................

# 6. Storing command outputs.

### storing commands outputs using $()

**Flag:** `pwn.college{ghidc7zjKha_zJA0xy5sne3hHkq.QX1cDN1wyM3gjNzEzW}`

as per the challenge we must directly read the output of /challenge/run command directly into the PWN variable. so we did `PWN=$(/challenge/run)`
and did `echo $PWN` to print out the flag value.



```
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out
and submit it!
hacker@variables~storing-command-output:~$ echo $PWN
pwn.college{ghidc7zjKha_zJA0xy5sne3hHkq.QX1cDN1wyM3gjNzEzW}
hacker@variables~storing-command-output:~$

```

## What I learned

I learned how to run the command subsitutions using $()


## References

NIL

..................................................................

# 7. Reading Inputs.

### reading inputs using read -p

**Flag:** `pwn.college{YWSk4cAvfViufmZus_USsIIzWjY.QX4cTN0wyM3gjNzEzW}`

as per the challenge we are suppose to assign the PWN the value of COLLEGE, using a user input. so we will use read -p command. like `read -p "INPUT:" PWN` in which we need to input the value of PWN which is COLLEGE. and thus got th value of flag.



```
hacker@variables~reading-input:~$ read -p "INPUT:" PWN
INPUT:COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{YWSk4cAvfViufmZus_USsIIzWjY.QX4cTN0wyM3gjNzEzW}
hacker@variables~reading-input:~$

```

## What I learned

I learned how to take inputs from a user and assign it into a variable


## References

NIL

..................................................................

# 8. Reading Files

### Reading files using redirecting inputs.

**Flag:** `pwn.college{IsSuhBZvr9JzLpOjpZA3VNAk43M.QXwIDO0wyM3gjNzEzW}`

as per the challenge we are suppose to redirect the inputs of /challenge/read_me to PWN variable, but we need to read it so we will use `read PWN < /challenge/read_me` and thus got the flag,

```
hacker@variables~reading-files:~$ read PWN < /challenge/read_me
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{IsSuhBZvr9JzLpOjpZA3VNAk43M.QXwIDO0wyM3gjNzEzW}
hacker@variables~reading-files:~$

```

## What I learned

I learned we can redirect the inputs into a variable and read it. using read command `eg read PWN > /challenge/read_me`


## References

NIL

..................................................................


