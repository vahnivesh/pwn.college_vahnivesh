# Intro to Commands

### In this challenge, you will invoke your first command! When you type a command and hit enter, the command will be invoked, as so:

**Flag:** `pwn.college{M9Jf4eJjlnRMFF2oUZNazq70Byo.QX3YjM1wyM3gjNzEzW}`

when we type a word, the shell runs its as a command and looks for functions etc
since the the challenge is to invoke our first command, on connecting to the dojo, using ssh -i key hacker@dojo.pwn.college, it only gives the flag (which is unique to every person)
when typed hello according to the challenge, 
since the commands in linux are case sensitive, if typing HELLO or Hello would not give the flag since HELLO and Hello are not the same as hello.
Only the exact hello command matched the executable provided by the challenge will give the flag.



## What I learned
Linux commands are case sensitive(hello & Hello are not the same)
simple commands like whoiam just prints the username, in this case hacker in the terminal.
hello is a custom command specific to this challenge to get the flag.

## References
NIL


.....................................................

# Intro to Arguments

### In this challenge, we will learn about commands with arguments.

**Flag:** `pwn.college{ktoe66mGxfzQGV1V4uwCo1Z7_7_.QX4YjM1wyM3gjNzEzW}`

the shell works on principle of taking the first word as command and second word as its argument
for example "echo hello hackers" would print the "hello hackers" in the terminal instead of giving the flag
according to this challenge to obtain the flag we must type "hello" which is the command, and when matched with the right agrument in this case "hackers" would give the the flag
since the argument is also case senstive, spelling mistakes will not give flags

## What I learned

The echo command prints its arguments back to the terminal.
I had to run the hello command with a single argument hackers.
Commands and arguments are case sensitive so hackers is different from Hackers.

## References
NIL

.......................................................


# Command History



### history of every command you invoke.


**Flag:** `pwn.college{sFS_Wysj4_fks_9MB9L0qjoij9o.0lNzEzNxwyM3gjNzEzW}`




The shell records a history of commands you run, so you don’t have to retype everything.
in this challenge the flag was already injected into the history of the terminal, by pressing the arrow key, we can go to through the history, thus obtaining the flag
history is the commands with its agrument run before.
by typing the command "history" we get the history of the commands we have written before.


## What I learned
The shell keeps a history of commands I’ve typed.
we can use the arrow up and down to scroll through the history
we can type history mainly, to get a numbered history

![screenshot of terminal with history](pwn.college_vahnievsh/Linux_Luminarium/image1.png)


## References
NIL

.......................................................



