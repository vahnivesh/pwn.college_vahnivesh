# 1. cat: not the pet, but the command

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


# 2. catting absolute paths

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

# 3. more catting practice

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

# 4. grepping for a neddle in a haystack

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


# 5. Comparing files

### comparing files and finding the difference in them

**Flag:** `pwn.college{QHknZOec1NoL89MuvAz16S_6y2-.01MwMDOxwyM3gjNzEzW}`

so as per the challenge, there are about 100 decoy flags txt and 100(decoy and real flag) txt, using the diff command, to compare contents of two files. using `diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt` we get the output, with the flag, along with the location of the flag, in this case the real flag among the decoy was in `3a2>`. this indicates that after line 3 in the first file, add the content from line 2 of the second file, thus getting us the real flag.



```
hacker@commands~comparing-files:~$ diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt
3a4
> pwn.college{QHknZOec1NoL89MuvAz16S_6y2-.01MwMDOxwyM3gjNzEzW}
hacker@commands~comparing-files:~$

```

## What I learned
i learned how to use diff.
also the format to understand where the difference is present using < & > and eeg 3a2 >



## References

NIL

..................................................................

# 6. Listing files

### listing files using ls.

**Flag:** `pwn.college{Miftf-z4H5kK83qyAiyzKR4mPK1.QX4IDO0wyM3gjNzEzW}`

so as the per challenge, we are suppose to find the flag which is in some random file name inside the `/challenge` directory. so we first used `ls` to list out all the folders, files in that directory. we found the file with the random name in it `23724-renamed-run-19725`. 
then we typed /challenge/23724-renamed-run-19725 to get the flag.

```
hacker@commands~listing-files:~$ ls /challenge
23724-renamed-run-19725  DESCRIPTION.md
hacker@commands~listing-files:~$ ls /challenge/23724-renamed-run-19725
/challenge/23724-renamed-run-19725
hacker@commands~listing-files:~$ /challenge/23724-renamed-run-19725
Yahaha, you found me! Here is your flag:
pwn.college{Miftf-z4H5kK83qyAiyzKR4mPK1.QX4IDO0wyM3gjNzEzW}
hacker@commands~listing-files:~$

```

## What I learned
we use ls to list out files and folders etc, in the directory. 

## References

NIL

..................................................................

# 7. Touching files

### creating blank files using touch command

**Flag:** `pwn.college{swdBg26VcfgS5klKH0SNBDalvLJ.QXwMDO0wyM3gjNzEzW}`

as per the challenge, we are suppose to create two files pwn and college in the `/tmp` directory.
at first we are in the home directory. we use `cd /tmp` to navigate to the /tmp directory.
in that using the touch command we created pwn & college files. like `touch pwn` & `touch college`. and then run the program. `/challenge/run`, thus obtaining the flag



```
hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ touch pwn
hacker@commands~touching-files:/tmp$ touch college
hacker@commands~touching-files:/tmp$ ls
bin  college  hsperfdata_root  pwn  tmp.TpSOPGOVKK
hacker@commands~touching-files:/tmp$ /challenge/run
Success! Here is your flag:
pwn.college{swdBg26VcfgS5klKH0SNBDalvLJ.QXwMDO0wyM3gjNzEzW}
hacker@commands~touching-files:/tmp$

```

## What I learned
we can create blank files in the terminal. by directing towards the desired directory and using `touch file_name`

## References

NIL

..................................................................

# 8. Removing files

### removing files using rm command

**Flag:** `pwn.college{4Gk0Pu2VStalbTJJ8t9jlP_c2o8.QX2kDM1wyM3gjNzEzW}`

In this challenge, we are suppose the remove a file named `delete_me`
so we use rm command to remove it like `hacker@commands~removing-files:~$ rm delete_me` . which removed the file. now we run the `/challenge/check` argument to check whether the delete_me is removed or not. if it is removed it would give the flag. in this case, thus getting the flag.

```
hacker@commands~removing-files:~$ ls
Desktop  a  delete_me
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ ls
Desktop  a
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{4Gk0Pu2VStalbTJJ8t9jlP_c2o8.QX2kDM1wyM3gjNzEzW}
hacker@commands~removing-files:~$

```

## What I learned
we can remove files or folders using `rm` command.
eg `rm delete_me`

## References

NIL

..................................................................

# 9. Moving files

### moving files using mv command

**Flag:** `pwn.college{4ndJWxcGb_uAVn45RycKcOF2Su-.0VOxEzNxwyM3gjNzEzW}`

at first typing the `cat /flag` would give a output of permission denied. we need to first move the flag file to desired location. using mv command we moved like `mv /flag /tmp/hack-the-planet`. it follows a format of `mv my_file my_desired_moving_location`. after sucessfully moving a confirmation was outputted saying "Correct! Performing 'mv /flag /tmp/hack-the-planet'." . and then to find the flag, we used  `/challenge/check` to check if the file was moved to correct location or not, thus giving us the flag.


```
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{4ndJWxcGb_uAVn45RycKcOF2Su-.0VOxEzNxwyM3gjNzEzW}

hacker@commands~moving-files:~$

```

## What I learned
using rm command we can move files from one directory to another.
it follows a format of `mv my_file my_desired_moving_location`

## References

NIL

..................................................................


# 10. hidden files

### listing out hidden files using ls -a

**Flag:** `pwn.college{4p3wBILugySlFHmnT05H6DvVR1f.QXwUDO0wyM3gjNzEzW}`

as per the linux commands any file haveing a .something_file_name is basically a hidden file.
normal ls command, would NOT list it out. in such cases, we use `ls -a` to list out all the files. in this case we first when to `/` directory and using ls -a we found `.flag-277614933968`
. i just simply put `cat /.flag-277614933968` thus getting the flag.


```
hacker@commands~hidden-files:~$ ls
Desktop  a
hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls
bin        dev   lib    libx32  nix   root  srv  usr
boot       etc   lib32  media   opt   run   sys  var
challenge  home  lib64  mnt     proc  sbin  tmp
hacker@commands~hidden-files:/$ ls -a
.                   bin        etc    lib64   nix   run   tmp
..                  boot       home   libx32  opt   sbin  usr
.dockerenv          challenge  lib    media   proc  srv   var
.flag-277614933968  dev        lib32  mnt     root  sys
hacker@commands~hidden-files:/$ cat .flag-277614933968
pwn.college{4p3wBILugySlFHmnT05H6DvVR1f.QXwUDO0wyM3gjNzEzW}
hacker@commands~hidden-files:/$

```

## What I learned
using `ls -a` we can list out all the files present in that directory, normal and hidden

## References

NIL

..................................................................

# 11. An epic filesystem quest

### finding the flag from what we learned in before challenges

**Flag:** `pwn.college{EW-LbEXPmAVYOp3NE2WogeHLAy0.QX5IDO0wyM3gjNzEzW}`

this challenge took me a alot of tries. i would always get struck at not cding hint. but i figured it out with a little patience. at first, as the instruction in the challenge we are suppose to go to `/` directory, after reaching there, i `ls` to list all the files and folders. one file got my attention whic was `BLUEPRINT` when i `cat BLUEPRINT` i got the hint which said me to cd to `/opt/linux/linux-5.4/drivers/gpu/drm/scheduler` after reaching that directory, i ls to find a file named TIP, i `cat TIP` to find my next clue which told me a hidden file in `/usr/share/locale/fo` i cd there. after invoking the `ls -a` command i got a hidden file named .HINT 
I `cat .HINT` to find the next clue which was trapped in a directory and if i CD there, the clue would self destruct. so i used `ls /usr/share/racket/pkgs/srfi-lib/srfi/%3a19` to list out the files. in which i `cat /usr/share/racket/pkgs/srfi-lib/srfi/%3a19/TRACE-TRAPPED` to get the next hint saying to go the next directory. this followed on untill i finally reached a README file. I have given the code in below.

```
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
BLUEPRINT  challenge  flag  lib32   media  opt   run   sys  var
bin        dev        home  lib64   mnt    proc  sbin  tmp
boot       etc        lib   libx32  nix    root  srv   usr
hacker@commands~an-epic-filesystem-quest:/$ cat BLUEPRINT
Congratulations, you found the clue!
The next clue is in: /opt/linux/linux-5.4/drivers/gpu/drm/scheduler

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/$ cd /opt/linux/linux-5.4/drivers/gpu/drm/scheduler
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/scheduler$ ls
Makefile  gpu_scheduler_trace.h  sched_fence.c
TIP       sched_entity.c         sched_main.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/scheduler$ cat TIP
Tubular find!
The next clue is in: /usr/share/locale/fo

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/scheduler$ cd /usr/share/locale/fo
hacker@commands~an-epic-filesystem-quest:/usr/share/locale/fo$ ls -a
.  ..  .HINT  LC_MESSAGES
hacker@commands~an-epic-filesystem-quest:/usr/share/locale/fo$ cat .HINT
Tubular find!
The next clue is in: /usr/share/racket/pkgs/srfi-lib/srfi/%3a19

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/share/locale/fo$ ls  /usr/share/racket/pkgs/srfi-lib/srfi/%3a19
TRACE-TRAPPED  compiled  time.rkt
hacker@commands~an-epic-filesystem-quest:/usr/share/locale/fo$ cat  /usr/share/racket/pkgs/srfi-lib/srfi/%3a19/TRACE-TRAPPED
Great sleuthing!
The next clue is in: /opt/busybox/busybox-1.33.2/include/config/unicode/neutral

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/share/locale/fo$ cd /opt/busybox/busybox-1.33.2/include/config/unicode/neutral
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/unicode/neutral$ ls -a
.  ..  .MEMO  table.h
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/unicode/neutral$ cat .MEMO
Yahaha, you found me!
The next clue is in: /usr/share/racket/pkgs/macro-debugger-text-lib/macro-debugger/util

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/unicode/neutral$ cd /usr/share/racket/pkgs/macro-debugger-text-lib/macro-debugger/util
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/macro-debugger-text-lib/macro-debugger/util$ ls -a
.  ..  .INFO  compiled  eomap.rkt  mpi.rkt
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/macro-debugger-text-lib/macro-debugger/util$ cat .INFO
Congratulations, you found the clue!
The next clue is in: /usr/share/racket/pkgs/scheme-lib/scheme/lang

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/macro-debugger-text-lib/macro-debugger/util$ ls /usr/share/racket/pkgs/scheme-lib/scheme/lang
NOTE-TRAPPED  compiled  reader.rkt
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/macro-debugger-text-lib/macro-debugger/util$ cat /usr/share/racket/pkgs/scheme-lib/scheme/lang/NOTE-TRAPPED
Lucky listing!
The next clue is in: /usr/share/icons/Adwaita/96x96/mimetypes

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/macro-debugger-text-lib/macro-debugger/util$ cd /usr/share/icons/Adwaita/96x96/mimetypes
hacker@commands~an-epic-filesystem-quest:/usr/share/icons/Adwaita/96x96/mimetypes$ ls
MESSAGE
application-certificate-symbolic.symbolic.png
application-x-executable-symbolic.symbolic.png
x-office-presentation-symbolic.symbolic.png
hacker@commands~an-epic-filesystem-quest:/usr/share/icons/Adwaita/96x96/mimetypes$ ls -a
.        application-certificate-symbolic.symbolic.png
..       application-x-executable-symbolic.symbolic.png
MESSAGE  x-office-presentation-symbolic.symbolic.png
hacker@commands~an-epic-filesystem-quest:/usr/share/icons/Adwaita/96x96/mimetypes$ cat MESSAGE
Lucky listing!
The next clue is in: /usr/local/lib/python3.8/dist-packages/jedi/third_party/typeshed/third_party/2and3/cachetools
hacker@commands~an-epic-filesystem-quest:/usr/share/icons/Adwaita/96x96/mimetypes$ cd /usr/local/lib/python3.8/dist-packages/jedi/third_party/typeshed/third_party/2and3/cachetools
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/jedi/third_party/typeshed/third_party/2and3/cachetools$ ls
README        abc.pyi    decorators.pyi  lfu.pyi  rr.pyi
__init__.pyi  cache.pyi  func.pyi        lru.pyi  ttl.pyi
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/jedi/third_party/typeshed/third_party/2and3/cachetools$ cat README
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{EW-LbEXPmAVYOp3NE2WogeHLAy0.QX5IDO0wyM3gjNzEzW}
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/jedi/third_party/typeshed/third_party/2and3/cachetools$

```

## What I learned
i got pratice of using cd, ls -a, ls, cat.


## References

NIL

..................................................................

# 12. Making directories

### making directories using mkdir

**Flag:** `pwn.college{wB-kP1ZWRhUk1LNGoGvr5XJOegQ.QXxMDO0wyM3gjNzEzW}`

in this challenge, they asked us to make a directory named pwn inside the `/tmp` directory.
i first cd into `cd /tmp` and create a pwn folder using mkdir like `mkdir pwn`. just to cross check i typed `ls` which  listed oyt pwn as a folder. i used cd into a relative path using `cd ./pwn`. in this i created a file named college using `touch college`. thus i followed all the instruction so i ran the `/challenge/run` which gave the flag


```
hacker@commands~making-directories:~$ cd /tmp
hacker@commands~making-directories:/tmp$ ls
bin  hsperfdata_root  tmp.TpSOPGOVKK
hacker@commands~making-directories:/tmp$ mkdir pwn
hacker@commands~making-directories:/tmp$ ls
bin  hsperfdata_root  pwn  tmp.TpSOPGOVKK
hacker@commands~making-directories:/tmp$ cd /pwn
bash: cd: /pwn: No such file or directory
hacker@commands~making-directories:/tmp$ cd ./pwn
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ ls
college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:
pwn.college{wB-kP1ZWRhUk1LNGoGvr5XJOegQ.QXxMDO0wyM3gjNzEzW}
hacker@commands~making-directories:/tmp/pwn$

```

## What I learned
i learned how to make directories using mkdir eg `mkdir pwn`

## References

NIL

..................................................................


# 13. Finding files

### finding files using find command

**Flag:** `pwn.college{wVNvrigJHfIigewlcmHHsz_GIIl.QXyMDO0wyM3gjNzEzW}`

as per instruction we are suppose the search for the file named `flag`. so i used the find command to find it like `find / -name flag`. This command listed out all the folders or files named with flag. at first i thought it will take a lot of time. but then i started reading the files named. many where permission denied. so it was not possible for the read the flag from there. i did option elimination based on the names of directories and after about a 3 tries, i got lukcy and got the actual flag directory which was `/usr/lib/x86_64-linux-gnu/gap/obj/src/flag` i did `cat /usr/lib/x86_64-linux-gnu/gap/obj/src/flag` and thus obtained the flag


```
hacker@commands~finding-files:~$ find / -name flag
find: ‘/tmp/tmp.TpSOPGOVKK’: Permission denied
find: ‘/etc/ssl/private’: Permission denied
/usr/lib/x86_64-linux-gnu/gap/obj/src/flag
/usr/local/lib/python3.8/dist-packages/pwnlib/flag
find: ‘/var/cache/apt/archives/partial’: Permission denied
find: ‘/var/cache/ldconfig’: Permission denied
find: ‘/var/cache/private’: Permission denied
find: ‘/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/mysql-files’: Permission denied
find: ‘/var/lib/private’: Permission denied
find: ‘/var/lib/mysql’: Permission denied
find: ‘/var/lib/mysql-keyring’: Permission denied
find: ‘/var/lib/php/sessions’: Permission denied
find: ‘/var/log/private’: Permission denied
find: ‘/var/log/apache2’: Permission denied
find: ‘/var/log/mysql’: Permission denied
find: ‘/run/mysqld’: Permission denied
find: ‘/run/sudo’: Permission denied
find: ‘/root’: Permission denied
/opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag
find: ‘/proc/tty/driver’: Permission denied
find: ‘/proc/1/task/1/fd’: Permission denied
find: ‘/proc/1/task/1/fdinfo’: Permission denied
find: ‘/proc/1/task/1/ns’: Permission denied
find: ‘/proc/1/fd’: Permission denied
find: ‘/proc/1/map_files’: Permission denied
find: ‘/proc/1/fdinfo’: Permission denied
find: ‘/proc/1/ns’: Permission denied
find: ‘/proc/8/task/8/fd’: Permission denied
find: ‘/proc/8/task/8/fdinfo’: Permission denied
find: ‘/proc/8/task/8/ns’: Permission denied
find: ‘/proc/8/fd’: Permission denied
find: ‘/proc/8/map_files’: Permission denied
find: ‘/proc/8/fdinfo’: Permission denied
find: ‘/proc/8/ns’: Permission denied
/nix/store/ka6xbd6z6wj5d6frl7ym4nzfc6p2wkdx-radare2-5.9.8/share/radare2/5.9.8/flag
/nix/store/f31j0igg7ms3yrj5gm3cm76bjcmdl8w5-python3.12-pwntools-4.13.1/lib/python3.12/site-packages/pwnlib/flag
/nix/store/7ns27apnvn4qj4q5c82x0z1lzixrz47p-radare2-5.9.8/share/radare2/5.9.8/flag
/nix/store/5z3sjp9r463i3siif58hq5wj5jmy5m98-python3.12-pwntools-4.13.1/lib/python3.12/site-packages/pwnlib/flag
/nix/store/n6vb30rd7kkwjj595pgm0dmsmfaqi6i5-rizin-0.7.3/share/rizin/flag
/nix/store/5n5lp1m8gilgrsriv1f2z0jdjk50ypcn-rizin-0.7.3/share/rizin/flag
/nix/store/bnlabj2vsbljhp597ir29l51nrqhm89w-rizin-0.7.4/share/rizin/flag
/nix/store/s8b49lb0pqwvw0c6kgjbxdwxcv2bp0x4-radare2-5.9.8/share/radare2/5.9.8/flag
/nix/store/8qvj9mzdq2qxgjigw4ysqgbkcx1zi80y-python3.13-pwntools-4.14.1/lib/python3.13/site-packages/pwnlib/flag
/nix/store/1hyxipvwpdpcxw90l5pq1nvd6s6jdi5m-python3.12-pwntools-4.14.1/lib/python3.12/site-packages/pwnlib/flag
/nix/store/dz2qxywk6d8hc1gkarpwbhyxb50sh2ak-pwntools-4.14.0/lib/python3.13/site-packages/pwnlib/flag
hacker@commands~finding-files:~$ cat /nix/store/dz2qxywk6d8hc1gkarpwbhyxb50sh2ak-pwntools-4.14.0/lib/python3.13/site-packages/pwnlib/flag
cat: /nix/store/dz2qxywk6d8hc1gkarpwbhyxb50sh2ak-pwntools-4.14.0/lib/python3.13/site-packages/pwnlib/flag: Is a directory
hacker@commands~finding-files:~$ ls /nix/store/dz2qxywk6d8hc1gkarpwbhyxb50sh2ak-pwntools-4.14.0/lib/python3.13/site-packages/pwnlib/flag
__init__.py  __pycache__  flag.py
hacker@commands~finding-files:~$ ls /tmp/tmp.TpSOPGOVKK
ls: cannot open directory '/tmp/tmp.TpSOPGOVKK': Permission denied
hacker@commands~finding-files:~$ ls /nix/store/ka6xbd6z6wj5d6frl7ym4nzfc6p2wkdx-radare2-5.9.8/share/radare2/5.9.8/flag
tags.r2
hacker@commands~finding-files:~$ ls /usr/lib/x86_64-linux-gnu/gap/obj/src/flag
/usr/lib/x86_64-linux-gnu/gap/obj/src/flag
hacker@commands~finding-files:~$ cat /usr/lib/x86_64-linux-gnu/gap/obj/src/flag
pwn.college{wVNvrigJHfIigewlcmHHsz_GIIl.QXyMDO0wyM3gjNzEzW}hacker@commands~finding-files:~$

```

## What I learned

i learned how to find the file using find command.

## References

NIL

..................................................................

# 14. 

### 

**Flag:** ``



```

```

## What I learned


## References

NIL

..................................................................
