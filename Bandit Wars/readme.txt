level 0----> 1:
bandit0@bandit:~$ ls
readme
bandit0@bandit:~$ cat readme
Congratulations on your first steps into the bandit game!!
Please make sure you have read the rules at https://overthewire.org/rules/
If you are following a course, workshop, walkthrough or other educational activity,
please inform the instructor about the rules as well and encourage them to
contribute to the OverTheWire community so we can keep these games free!

The password you are looking for is: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If

bandit0@bandit:~$
LEVEL 1 ----> 2 :
bandit1@bandit:~$ ls -l
total 4
-rw-r----- 1 bandit2 bandit1 33 Aug 15 13:16 -
bandit1@bandit:~$ cat ./-
263JGJPfgU6LtdEvgfWU1XP5yac29mFx
bandit1@bandit:~$
LEVEL 2 ----> 3 :
bandit2@bandit:~$ ls -l
total 4
-rw-r----- 1 bandit3 bandit2 33 Aug 15 13:16 --spaces in this filename--
bandit2@bandit:~$ cat ./--spaces\ in\ this\ filename--
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
bandit2@bandit:~$
LEVEL 3 ----> 4 :
bandit3@bandit:~/inhere$ cd ..
bandit3@bandit:~$ cd ./inhere
bandit3@bandit:~/inhere$ ls -l
total 0
bandit3@bandit:~/inhere$ ls -alps
total 12
4 drwxr-xr-x 2 root    root    4096 Aug 15 13:16 ./
4 drwxr-xr-x 3 root    root    4096 Aug 15 13:16 ../
4 -rw-r----- 1 bandit4 bandit3   33 Aug 15 13:16 ...Hiding-From-You
bandit3@bandit:~/inhere$ cat ./...Hiding-From-You
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
bandit3@bandit:~/inhere$ exit
logout
Connection to bandit.labs.overthewire.org closed.
vahnivesh@VAHNI:~$
LEVEL 4 ----> 5 :
bandit4@bandit:~/inhere$ cd ..
bandit4@bandit:~$ cd /inhere
-bash: cd: /inhere: No such file or directory
bandit4@bandit:~$ ls -l
total 4
drwxr-xr-x 2 root root 4096 Aug 15 13:16 inhere
bandit4@bandit:~$ cd ./inhere
bandit4@bandit:~/inhere$ ls
-file00  -file02  -file04  -file06  -file08
-file01  -file03  -file05  -file07  -file09
bandit4@bandit:~/inhere$ cat ./-file03
|g򸌎TUuhjaW1dS>Gycbandit4@bandit:~/inhere$ cat ./-file07
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
bandit4@bandit:~/inhere$ exit
logout
Connection to bandit.labs.overthewire.org closed.
vahnivesh@VAHNI:~$
LEVEL 5 ----> 6 :
bandit5@bandit:~$ ls
inhere
bandit5@bandit:~$ cd ./inhere
bandit5@bandit:~/inhere$ ls -l
total 80
drwxr-x--- 2 root bandit5 4096 Aug 15 13:16 maybehere00
drwxr-x--- 2 root bandit5 4096 Aug 15 13:16 maybehere01
drwxr-x--- 2 root bandit5 4096 Aug 15 13:16 maybehere02
drwxr-x--- 2 root bandit5 4096 Aug 15 13:16 maybehere03
drwxr-x--- 2 root bandit5 4096 Aug 15 13:16 maybehere04
drwxr-x--- 2 root bandit5 4096 Aug 15 13:16 maybehere05
drwxr-x--- 2 root bandit5 4096 Aug 15 13:16 maybehere06
drwxr-x--- 2 root bandit5 4096 Aug 15 13:16 maybehere07
drwxr-x--- 2 root bandit5 4096 Aug 15 13:16 maybehere08
drwxr-x--- 2 root bandit5 4096 Aug 15 13:16 maybehere09
drwxr-x--- 2 root bandit5 4096 Aug 15 13:16 maybehere10
drwxr-x--- 2 root bandit5 4096 Aug 15 13:16 maybehere11
drwxr-x--- 2 root bandit5 4096 Aug 15 13:16 maybehere12
drwxr-x--- 2 root bandit5 4096 Aug 15 13:16 maybehere13
drwxr-x--- 2 root bandit5 4096 Aug 15 13:16 maybehere14
drwxr-x--- 2 root bandit5 4096 Aug 15 13:16 maybehere15
drwxr-x--- 2 root bandit5 4096 Aug 15 13:16 maybehere16
drwxr-x--- 2 root bandit5 4096 Aug 15 13:16 maybehere17
drwxr-x--- 2 root bandit5 4096 Aug 15 13:16 maybehere18
drwxr-x--- 2 root bandit5 4096 Aug 15 13:16 maybehere19
bandit5@bandit:~/inhere$ find .- -f -size 1033
find: unknown predicate `-f'
bandit5@bandit:~/inhere$ find . -type f -size 1033c
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        bandit5@bandit:~/inhere$
LEVEL 6 ----> 7 :
bandit6@bandit:~$ pwd
/home/bandit6
bandit6@bandit:~$ ls -alps
total 20
4 drwxr-xr-x   2 root root 4096 Aug 15 13:15 ./
4 drwxr-xr-x 150 root root 4096 Aug 15 13:18 ../
4 -rw-r--r--   1 root root  220 Mar 31  2024 .bash_logout
4 -rw-r--r--   1 root root 3851 Aug 15 13:09 .bashrc
4 -rw-r--r--   1 root root  807 Mar 31  2024 .profile
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c
find: ‘/sys/kernel/tracing/osnoise’: Permission denied
find: ‘/sys/kernel/tracing/hwlat_detector’: Permission denied
find: ‘/sys/kernel/tracing/instances’: Permission denied
find: ‘/sys/kernel/tracing/trace_stat’: Permission denied
find: ‘/sys/kernel/tracing/per_cpu’: Permission denied
find: ‘/sys/kernel/tracing/options’: Permission denied
find: ‘/sys/kernel/tracing/rv’: Permission denied
find: ‘/sys/kernel/debug’: Permission denied
find: ‘/sys/fs/pstore’: Permission denied
find: ‘/sys/fs/bpf’: Permission denied
find: ‘/root’: Permission denied
find: ‘/boot/lost+found’: Permission denied
find: ‘/boot/efi’: Permission denied
find: ‘/run/udisks2’: Permission denied
find: ‘/run/chrony’: Permission denied
find: ‘/run/user/11028’: Permission denied
find: ‘/run/user/11030’: Permission denied
find: ‘/run/user/11001’: Permission denied
find: ‘/run/user/11008’: Permission denied
find: ‘/run/user/11003’: Permission denied
find: ‘/run/user/11004’: Permission denied
find: ‘/run/user/11009’: Permission denied
find: ‘/run/user/11014’: Permission denied
find: ‘/run/user/11023’: Permission denied
find: ‘/run/user/11007’: Permission denied
find: ‘/run/user/11021’: Permission denied
find: ‘/run/user/11011’: Permission denied
find: ‘/run/user/11019’: Permission denied
find: ‘/run/user/11000’: Permission denied
find: ‘/run/user/11006/systemd/inaccessible/dir’: Permission denied
find: ‘/run/user/11002’: Permission denied
find: ‘/run/user/11012’: Permission denied
find: ‘/run/user/11005’: Permission denied
find: ‘/run/user/11020’: Permission denied
find: ‘/run/user/11026’: Permission denied
find: ‘/run/user/11025’: Permission denied
find: ‘/run/user/11013’: Permission denied
find: ‘/run/user/11024’: Permission denied
find: ‘/run/sudo’: Permission denied
find: ‘/run/screen/S-bandit25’: Permission denied
find: ‘/run/screen/S-bandit24’: Permission denied
find: ‘/run/screen/S-bandit23’: Permission denied
find: ‘/run/screen/S-bandit20’: Permission denied
find: ‘/run/multipath’: Permission denied
find: ‘/run/cryptsetup’: Permission denied
find: ‘/run/lvm’: Permission denied
find: ‘/run/systemd/propagate/fwupd.service’: Permission denied
find: ‘/run/systemd/propagate/ModemManager.service’: Permission denied
find: ‘/run/systemd/propagate/polkit.service’: Permission denied
find: ‘/run/systemd/propagate/chrony.service’: Permission denied
find: ‘/run/systemd/propagate/systemd-logind.service’: Permission denied
find: ‘/run/systemd/propagate/irqbalance.service’: Permission denied
find: ‘/run/systemd/propagate/systemd-networkd.service’: Permission denied
find: ‘/run/systemd/propagate/systemd-resolved.service’: Permission denied
find: ‘/run/systemd/propagate/systemd-udevd.service’: Permission denied
find: ‘/run/systemd/inaccessible/dir’: Permission denied
find: ‘/run/lock/lvm’: Permission denied
find: ‘/dev/mqueue’: Permission denied
find: ‘/dev/shm’: Permission denied
find: ‘/lost+found’: Permission denied
find: ‘/drifter/drifter14_src/axTLS’: Permission denied
find: ‘/manpage/manpage3-pw’: Permission denied
find: ‘/var/log’: Permission denied
find: ‘/var/lib/private’: Permission denied
find: ‘/var/lib/udisks2’: Permission denied
find: ‘/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/update-notifier/package-data-downloads/partial’: Permission denied
find: ‘/var/lib/chrony’: Permission denied
find: ‘/var/lib/snapd/void’: Permission denied
find: ‘/var/lib/snapd/cookie’: Permission denied
find: ‘/var/lib/ubuntu-advantage/apt-esm/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/amazon’: Permission denied
find: ‘/var/lib/polkit-1’: Permission denied
/var/lib/dpkg/info/bandit7.password
find: ‘/var/spool/bandit24’: Permission denied
find: ‘/var/spool/rsyslog’: Permission denied
find: ‘/var/spool/cron/crontabs’: Permission denied
find: ‘/var/cache/pollinate’: Permission denied
find: ‘/var/cache/private’: Permission denied
find: ‘/var/cache/apt/archives/partial’: Permission denied
find: ‘/var/cache/ldconfig’: Permission denied
find: ‘/var/cache/apparmor/0fb44ac6.0’: Permission denied
find: ‘/var/cache/apparmor/208b6430.0’: Permission denied
find: ‘/var/crash’: Permission denied
find: ‘/var/tmp’: Permission denied
find: ‘/proc/tty/driver’: Permission denied
find: ‘/proc/2019594/task/2019594/fd/6’: No such file or directory
find: ‘/proc/2019594/task/2019594/fdinfo/6’: No such file or directory
find: ‘/proc/2019594/fd/5’: No such file or directory
find: ‘/proc/2019594/fdinfo/5’: No such file or directory
find: ‘/snap’: Permission denied
find: ‘/tmp’: Permission denied
find: ‘/etc/credstore’: Permission denied
find: ‘/etc/credstore.encrypted’: Permission denied
find: ‘/etc/sudoers.d’: Permission denied
find: ‘/etc/ssl/private’: Permission denied
find: ‘/etc/xinetd.d’: Permission denied
find: ‘/etc/stunnel’: Permission denied
find: ‘/etc/polkit-1/rules.d’: Permission denied
find: ‘/etc/multipath’: Permission denied
find: ‘/home/bandit31-git’: Permission denied
find: ‘/home/bandit5/inhere’: Permission denied
find: ‘/home/leviathan4/.trash’: Permission denied
find: ‘/home/bandit30-git’: Permission denied
find: ‘/home/bandit27-git’: Permission denied
find: ‘/home/leviathan0/.backup’: Permission denied
find: ‘/home/drifter6/data’: Permission denied
find: ‘/home/ubuntu’: Permission denied
find: ‘/home/bandit28-git’: Permission denied
find: ‘/home/bandit29-git’: Permission denied
find: ‘/home/drifter8/chroot’: Permission denied
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
bandit6@bandit:~$
LEVEL 7 ----> 8 :
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ grep millionth data.txt
millionth       dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
bandit7@bandit:~$
LEVEL 8 ----> 9 :
bandit8@bandit:~$ ls -alps
total 56
 4 drwxr-xr-x   2 root    root     4096 Aug 15 13:16 ./
 4 drwxr-xr-x 150 root    root     4096 Aug 15 13:18 ../
 4 -rw-r--r--   1 root    root      220 Mar 31  2024 .bash_logout
 4 -rw-r--r--   1 root    root     3851 Aug 15 13:09 .bashrc
36 -rw-r-----   1 bandit9 bandit8 33033 Aug 15 13:16 data.txt
 4 -rw-r--r--   1 root    root      807 Mar 31  2024 .profile
bandit8@bandit:~$ sort data.txt | uniq -u
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
bandit8@bandit:~$
LEVEL 9 ----> 10 :
bandit9@bandit:~$ ls
data.txt
bandit9@bandit:~$ strings data.txt | grep =
========== theg
VQ=97
[m=K1x
/i8D2[U?=
========== password
LU=W
========== is
=v$,
h{=,rw_c
=}%q
=D!7
YU=<
5=fq
vJ=ho
========== FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
=AdD
bandit9@bandit:~$
LEVEL 10 ----> 11 :
bandit10@bandit:~$ base64 -d data.txt
The password is dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
bandit10@bandit:~$
LEVEL 11 ----> 12 :



