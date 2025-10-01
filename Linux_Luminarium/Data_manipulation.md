# 1. Translating characters

### translating characters using tr command

**Flag:** `pwn.college{YGrWHvDT8NqhBeWVL3kLabM_y9c.01MxEzNxwyM3gjNzEzW}`

as per the challenge we are suppose to swapp the captial letters with the small ones and vice versa. to do this we will use tr and agrument of `a-zA-Z` to be swapped with `A-Za-z` like `/challenge/run | tr 'a-zA-Z' 'A-Za-z'` and thus got the flag.



```
hacker@data~translating-characters:~$ /challenge/run | tr 'a-zA-Z' 'A-Za-z'
yOUR CASE-SWAPPED FLAG:
pwn.college{YGrWHvDT8NqhBeWVL3kLabM_y9c.01MxEzNxwyM3gjNzEzW}

hacker@data~translating-characters:~$

```

## What I learned

I learned how to swapp characters using tr command


## References

NIL

..................................................................

# 2. Deleting characters.

### deleting characters using tr -d command

**Flag:** `pwn.college{oZiNHnGEF-Lq0F27UywBc9fU-ql.0FNxEzNxwyM3gjNzEzW}`

as per the challenge we are suppose to delete certain characters such as ^ and % from the flag. to do this we will use tr -d command. 
like `/challenge/run | tr -d ^%` and thus got the flag.


```
hacker@data~deleting-characters:~$ /challenge/run | tr -d ^%
Your character-stuffed flag:
pwn.college{oZiNHnGEF-Lq0F27UywBc9fU-ql.0FNxEzNxwyM3gjNzEzW}
hacker@data~deleting-characters:~$

```

## What I learned

I learned how to delete characters using tr -d command.


## References

NIL

..................................................................

# 3. Deleting newlines

### deleting newlines using tr -d "\n"

**Flag:** `pwn.college{g8lml4K7Tlp1EFO1FVkD7zyC8uc.0VNxEzNxwyM3gjNzEzW}`

as per the challenge we are suppose to delete the newlines using tr -d but we need to keep it in double quotes so the shell can interpret it. so we will do `/challenge/run | tr -d "\n"`  and thus got the flag.



```
hacker@data~deleting-newlines:~$ /challenge/run | tr -d "\n"
Your line-split flag: pwn.college{g8lml4K7Tlp1EFO1FVkD7zyC8uc.0VNxEzNxwyM3gjNzEzW}

```

## What I learned

I learned how to delete new lines combining the tr delete command with "\n"


## References

NIL

..................................................................

# 4. Extracting the first lines with head

### extracting a few lines using head command

**Flag:** `pwn.college{AIg4tKpOQttlatfNC5hv-QHL5gW.0lNxEzNxwyM3gjNzEzW}`

as per the challenge , the file has to much information and we only need the first 7 lines of code, so we will use head command to extract the first 7 lines of the context and pipe it /challenge/college. like `/challenge/pwn | head -n 7| /challenge/college` and thus got the flag.



```
hacker@data~extracting-the-first-lines-with-head:~$ /challenge/pwn | head -n 7
SECRET-CODE-10554
SECRET-CODE-12059
SECRET-CODE-21146
SECRET-CODE-4116
SECRET-CODE-13940
SECRET-CODE-7707
SECRET-CODE-1353
hacker@data~extracting-the-first-lines-with-head:~$ /challenge/pwn | head -n 7| /challenge/college
Congratulations, you piped the right codes!
pwn.college{AIg4tKpOQttlatfNC5hv-QHL5gW.0lNxEzNxwyM3gjNzEzW}
hacker@data~extracting-the-first-lines-with-head:~$

```

## What I learned

I learned how to extract first few lines of code using head command


## References

NIL

..................................................................

# 5. extracting specific sections of text

### extracting specific sections of text using cut command

**Flag:** `pwn.college{UetHXh62LGQBbplv2T38DHeEGtq.01NxEzNxwyM3gjNzEzW}`

as per the challenge we are suppose to cut the specific sections of text using cut command and join them togther with tr -d "\n" so we selected the 2 column.
so we did `/challenge/run | cut -d " " -f 2 | tr -d "\n"` and thus got the flag.





```
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d " " -f 3 | tr -d "\n"
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d " " -f 2 | tr -d "\n"
pwn.college{UetHXh62LGQBbplv2T38DHeEGtq.01NxEzNxwyM3gjNzEzW}hacker@data~extracting-specific-sections-of-text:~$

```

## What I learned

I learned how to use cut command to select a specific section(column) in a file.


## References

NIL

..................................................................

# 6. Sorting data

### using sort command to sort data

**Flag:** `pwn.college{kwjcNWk3Cg8AoiAlXTuCTCqRCvN.0FM0MDOxwyM3gjNzEzW}`

as per the challenge, there are about 100 fake flags and one real flag, when sorted in correct order the flag will be last. so we use sort command to do this.
like `sort /challenge/flags.txt`



```
hacker@data~sorting-data:~$ sort /challenge/flags.txt
ovm.coklefe{kwjcMWk3Cg7AniAlWTuCTCqQCvN.0EM0MCNxwxL3gjNzEzW}
ovn.bnlldgd{jwjbMWk2Cg8AoiAlWSuCTCpRBvM.0FM0MDOxwyM2giNzDzV}
ovn.bollefe{kwjcNWk3Bg8AoiAkWTuCTCpQCvN.0FM0LDNxwyM3giNzDzV}
ovn.cnllege{kwicMWk3Cg8AoiAkWTuCTCpRCuN.0FL0MDOwvyM3gjNyEzW}
ovn.coklege{kwicNWk2Cf8AoiAlXSuBSCqRCvM.0EM0LCOwwyM3gjNzEzW}
ovn.colkege{kwjbNWj2Cg7AnhAkXTtBSBqQCuN.0FM0MCOwwxM3fiNyEyW}
owm.bolkege{kvjbNWk3Bf8AohAkWTtCSBpRBvN.0EM0MDOxwxM3fiNzEzW}
owm.bollefe{kwjbNWj3Cf7AniAlXTuCSCqRCvM.0FM0MCNxvyL3gjMzDzW}
own.bnllege{kvicNWk3Cg8AniAlXTtBTBqRCuM.0EM0MDOxwxM3gjNzEzV}
own.bnllege{kwjbNVj2Bg7AohAlXStBSBqRBuN.0FM0LDNxvyM3gjNzDyV}
own.bolkege{jwicNWk3Cg8AohAlWTtCTBqRCvM.0FM0MDOwwyL2gjNzEzW}
own.bollefe{kwicMVk3Cg8AnhAlXStCTBpRBuN.0FM0MDOxvyM2fjNyDzW}
own.bollege{jvjcNWk3Cg8AoiAlWSuBTCqQCvN.0EM0MDOxvyL3fjNzEyW}
own.cnklegd{jvjbNWk2Cf8AniAlXTuBSBqQBuM.0FM0LDNxvyM3giMzDzW}
own.coklege{kwjcMWj3Cf8AoiAlXTuCTCpRCvN.0EM0MDOwwyM3gjMzEyV}
own.colkege{kvjcNVj3Bf8AnhAlXStCSCqRCvN.0FM0MCNxvyM3gjMzEzW}
own.college{jwjcMWk3Cg8AniAlWTuCTBqQCuN.0FL0MCOwwyM2gjNyEzW}
own.college{kwjcNWk3Cf7AohAlXSuCTCpRCvN.0FM0MDOxwyM3fjMzEzW}
pvm.bolldge{jwibMVk3Bg7AoiAlXSuCTCqRCvN.0EM0LDNxvyM3gjNzEzW}
pvm.cnkldge{jvjcMVj3Cf8AniAlXSuCSCpRCvN.0FM0MDOxwxM2giNzEyW}
pvm.cokkegd{jvjcMWj2Bf8AnhAlXSuBSCqQBuN.0FM0MCOxvyM3gjNzEyW}
pvm.colldge{kwjbNVj3Cg7AniAkXSuCSBqRBvM.0FL0MDOxwyM3giNzEyW}
pvm.collefe{kwicNVj3Cg8AoiAkWTuBTCqQCvM.0FM0MDOxwyL3gjNzEyV}
pvm.collegd{jwjcNVk2Cf8AohAlWSuBTCqRBvN.0EM0LDNxwyL3gjNyEyW}
pvn.bnlkefe{kwjcNVk2Bg7AoiAlXStCTCqQBuN.0EL0MDOwwyM3gjMzDyV}
pvn.bnllege{kvibMWj3Cg7AoiAlWTuCTCpRBuN.0EM0LDOwwyM3gjMyEzV}
pvn.bolkdge{kwjcNVk3Bg8AohAkXSuCSCqRCvN.0EL0LDOxwyM2fiNzDyV}
pvn.cnlkdge{kwjcNVk3Bf8AohAlWTtBTCqQCvN.0FM0LDNxvyL3gjNyEzV}
pvn.cnllege{kwjcNWk3Cg8AoiAlXTuCTCqRCvN.0FM0MDNxwyM3gjNzEzW}
pvn.colkdge{jvicNWk3Bg8AoiAlXTtBTBpRCvM.0FL0LCOxvyM3fiNzDzW}
pvn.colkegd{kwjcMVk3Cg7AoiAlXTuCTCqRCvN.0FL0MDOxwyM3gjNzEzW}
pvn.college{kvjcNWj3Cf8AohAlXTuCTBpQCuN.0FL0LCOxwyM3gjNyDyW}
pvn.college{kwjcNWk2Cg8AoiAlXTuCTBpQCuN.0FM0LDOxvyM3gjNyEzW}
pwm.bnkldge{kwjcNVj3Cg8AnhAlXTuCTBqRCvN.0FM0LDNxwyM3gjNzEzW}
pwm.bnklefe{kwjcMWj2Cg7AoiAlXTuCTCpRCuN.0FM0MCOwwyM3gjNzEzV}
pwm.bnllefe{jwjbMVk2Cf7AoiAkXTuBTCpRCuN.0FM0MCNxwxL2gjNzEzW}
pwm.bolkege{kvjcNWk3Bg8AohAlXStCTCqRCvN.0FM0MDNxwxM3gjNzEzW}
pwm.bolkege{kwibNVk3Bg7AoiAlXTtBTCqRCvM.0EM0MDOxwyM3fjNzEzW}
pwm.cnklegd{jvicNWj2Cf8AoiAlXSuCSBpRCvN.0FL0MDNwwxM3fjNzEyW}
pwm.cnlldfe{kwjcNWk3Bf8AohAkXSuCSCqQCuM.0FL0MDOwwyL3gjNyEyV}
pwm.cokkege{kwicNWj3Cf8AoiAlXTtCSCpRCuN.0EM0MDNxwyL3gjNzEzW}
pwm.colkdgd{jvicNWj3Cg8AniAlXStCTCqRBvM.0FM0MDNwwyL3giNzDyV}
pwm.colkdgd{jwicMWk3Cg7AohAkWTuCSBqQCuN.0FM0MCOwwxM3fjMzEyW}
pwm.colkege{kwjcNWj3Cg8AohAlXTuCTCqRCvN.0FM0MDOwwyM3fjNzEzW}
pwn.bnlldge{jwjcMVk3Cg8AniAkWStCSBqRBvN.0FL0MDOwvyM3fjNyEzW}
pwn.bnlldge{kwicMWk2Bg8AohAlXTuBTCpQCuM.0EM0MCNxwyL3fjNzEzW}
pwn.bnllege{kwjcNWk3Cg8AohAlXTuCTCqQCvN.0FL0MCOxwyL2fiNzEzV}
pwn.bolkegd{kwibMWk2Bg8AniAkWStBTBqRCuN.0FM0MDOxwyL2gjMzEzW}
pwn.bolkege{jwjbNWk3Cf8AoiAlXTuCTCqQBvN.0EL0MDOwvxL2gjNzEzW}
pwn.bolldge{kwicNWk3Bf7AoiAlXTtCTCqRCvN.0FM0LDOxwyM3giMzEzV}
pwn.bollefe{kvjcNWj2Cg8AohAlWTuBTCqRBvN.0FM0LCOxvyM3gjNzDyW}
pwn.bollege{jwjcNWk2Cf8AoiAlXTuCTBqRCuN.0FL0MDOxwyM3gjMzEzV}
pwn.cnkkege{kvjcNWk3Cf8AoiAkWTuCTCqRCvN.0EM0MDOwwyM3gjNzDyW}
pwn.cnklegd{kvicNWk3Cg8AoiAlWTtBTCqRCvM.0FM0LDOxvyM3gjMzEzW}
pwn.cnlkdfd{kwibNWk3Cg8AoiAlXTuCTCpQCvN.0FM0LCOxvyM3fiMyEyW}
pwn.cnlkege{kwicNWk3Bg7AohAlXTuBTCqRCuN.0FM0MDOxvyM3gjNzEzW}
pwn.cnllege{kvjbNWk3Cg8AoiAlXTuCTBqRCvN.0FM0MDOxwyM3gjNzEzW}
pwn.cnllege{kwibMWj3Cg8AoiAlWTuCTCqRCvN.0FL0MCOwwyM3giNzEzW}
pwn.cnllege{kwjbNWk3Bg8AoiAlWTtBTBqRCvN.0FM0MDOxwxM2giNzEzW}
pwn.cnllege{kwjcMWk3Cg8AoiAlXTtCTCpQCvN.0FL0MDOwwyL3gjNzDzW}
pwn.cnllege{kwjcNVk3Cg8AoiAlXTuCTCqRCvN.0FM0MDOxwyM3gjNyEyW}
pwn.cnllege{kwjcNWk2Cg8AoiAlXTuBTCqRCvN.0EM0MDOxwyM3gjMzEzV}
pwn.cnllege{kwjcNWk2Cg8AoiAlXTuCTCqRCvN.0EM0MDOxwyM3gjNzEzW}
pwn.cnllege{kwjcNWk3Cg8AoiAkXTtCTCpRCvN.0FM0MDOxwyM3gjMzEzW}
pwn.cokkdgd{kvjcMWj2Cf8AohAkXSuCSCqRBvM.0FM0MDOxwyM2fjNyDzW}
pwn.coklegd{kvjbNVk3Cg8AoiAlXTtCTCpRCvN.0EL0LDOwwyM3fjNyEzW}
pwn.coklege{jwjcMWk3Cg7AoiAlXTuCTCqRCvN.0FM0MDNxwyM3gjNzDzW}
pwn.coklege{jwjcNVk3Cf8AnhAlXTtCTCqRCvN.0FM0MDOwvyL3gjNzEzW}
pwn.coklege{kvjcNWj2Cg8AniAkXTuCTBqRCuN.0FM0MCOxwyM2gjMzDzW}
pwn.colkdfe{kvjcMWk3Cf7AniAkXTuCSCqQBuM.0FM0MDOxwyL3gjNzDzV}
pwn.colkefd{kwjcNWj2Cf7AoiAkWSuCSBqRCvN.0FM0MDOxwyM3fjNzDyV}
pwn.colkegd{kwicNWk2Cg8AoiAlXTuCTBqRCvN.0FM0MDOxwyM2fjNzEzW}
pwn.colkege{kwjcNWk3Cg8AniAlXTtCTCqRCvN.0FL0LDOxwyM3fjNzEyW}
pwn.colldfd{kwjcMVj3Cf7AoiAlWStCTBqRCvN.0EL0MDOxwxM3giNzEzW}
pwn.colldfe{jwjcNWk2Bg8AnhAkXTuCSBqRBvN.0EM0MDOxvyM2fjMzEzV}
pwn.colldge{kwjcNVk3Cf8AoiAkXTuCTCpRCvN.0FL0MDOwwyM3gjNzEzW}
pwn.collefd{kwibNVj3Cf8AniAlWSuCTCqQCuN.0EM0MCOxwxL3gjMzEzW}
pwn.collefe{kvjcNWk3Cg8AoiAkWTuCSBqRCvM.0FM0MCNxwyM3gjNyEzW}
pwn.collefe{kwjcNVk2Bf7AniAlXSuCTCpRBvN.0FL0MDNxwxM3gjMyEzW}
pwn.collefe{kwjcNWk3Cg8AoiAkXTuCTCqRCvN.0FM0MDOxwyM3gjNzEyW}
pwn.collefe{kwjcNWk3Cg8AoiAlXTuCTCqRCvN.0FM0MDOxwxM3fiNzEzW}
pwn.collegd{kwicNWj3Cg8AoiAlXSuCTCqQCvN.0FL0MDOxwyL3giNyEzW}
pwn.college{jwicNWk2Cg7AoiAlWTuCSCqQCvN.0FM0MDNxwyM2gjNzEzW}
pwn.college{jwjbNVj3Cg8AoiAlXStCTBqRCvN.0FM0MDOxwyM3gjNzEzW}
pwn.college{jwjcNWk3Cg8AoiAlXTuCTCqRCvN.0FM0MDOxwyM3giNzEzW}
pwn.college{jwjcNWk3Cg8AoiAlXTuCTCqRCvN.0FM0MDOxwyM3gjNzEzW}
pwn.college{kwicMWk3Bg8AoiAlXTuCTCpRCvN.0FM0MCNwvyM3fjMzEzW}
pwn.college{kwicNWk3Cg8AohAlWTuCTCpRCvN.0FM0MDOxwyM3gjNzEzW}
pwn.college{kwicNWk3Cg8AoiAlXTtBSCpRCvN.0FM0MDNxwyM3giNzDzW}
pwn.college{kwjcNVk3Cf8AoiAlXTuCTBqRBvM.0FM0MDOxvyM3gjMzEzW}
pwn.college{kwjcNVk3Cg8AoiAlXTuCTCqQCvN.0FM0MDOxwyM3gjNzEzW}
pwn.college{kwjcNWk2Cg8AohAlXTuCTCqRCvN.0FM0MDOxwyM3gjNzEzW}
pwn.college{kwjcNWk2Cg8AoiAlXTuCTCqRCvN.0FM0MDOxwyM3gjNzEzW}
pwn.college{kwjcNWk3Bg8AoiAlXTuCTCqRCuN.0FM0MDOxwyM3gjNzEzW}
pwn.college{kwjcNWk3Bg8AoiAlXTuCTCqRCvN.0FM0MDOxwyM3gjNzEzW}
pwn.college{kwjcNWk3Cg7AoiAlXTuCTCpRCvN.0FM0MDOwwyM3gjNzEzV}
pwn.college{kwjcNWk3Cg8AohAlXTuCTCqRCvN.0FM0MDOxvyL3gjNzEyW}
pwn.college{kwjcNWk3Cg8AoiAlWTuCSCqQCvN.0FM0MDOxwyM3gjNzEzW}
pwn.college{kwjcNWk3Cg8AoiAlXTuCSCqRCvN.0FM0MDOxwyM3gjNzEyW}
pwn.college{kwjcNWk3Cg8AoiAlXTuCTBqRBvN.0FM0LDOxwyM3gjNzEzW}
pwn.college{kwjcNWk3Cg8AoiAlXTuCTCqRCvN.0FM0MDOxwyM3gjNzEzW}
hacker@data~sorting-data:~$

```

## What I learned

I learned how to sort data using sort command, with special sorts like -r, -u -n for rev, unqiue, numbers etc.

## References

NIL

..................................................................
