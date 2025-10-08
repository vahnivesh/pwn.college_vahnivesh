# 1. Zahard's Welcome

### 

**Flag:** `citadel{7h3_c174d3l_b3ck0n5}`

the first challenge, we had to join the discord and go to the “The path begins in the gathering place. There, candidates are chosen.” and in description we get the flag.



```


```

## What I learned


## References

discord.

NIL

..................................................................
# 2. The Social Network

### 

**Flag:** `citadel{17_1s_jus7_7h3_b3g1nn1ng}`

going to instagram page of `https://www.instagram.com/citadweller/` in the highlights, we get first half of the flag, it says follow me on X, going to x in bio the rest of the flag was there.



```


```

## What I learned


## References

instagram, x

..................................................................

# 3. Omniscient Flag's Metadata

### 

**Flag:** `citadel{th1s_ch4ll3ng3_1s_f0r_th4t_0n3_ex1ft00l_4nd_b1nw4lk_enthus14st}`

we did exiftool and we found `kdj had a habit of hiding images within images` is a hint, so we will use foremost to get the hinted message.



```
vahnivesh@VAHNI:/mnt/e$ exiftool challenge.jpg
ExifTool Version Number         : 12.76
File Name                       : challenge.jpg
Directory                       : .
File Size                       : 371 kB
File Modification Date/Time     : 2025:10:08 06:44:12+00:00
File Access Date/Time           : 2025:10:08 06:44:23+00:00
File Inode Change Date/Time     : 2025:10:08 06:44:12+00:00
File Permissions                : -rwxrwxrwx
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
XMP Toolkit                     : Image::ExifTool 12.57
Author                          : kdj had a habit of hiding images within images
Image Width                     : 640
Image Height                    : 1017
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 640x1017
Megapixels                      : 0.651
vahnivesh@VAHNI:/mnt/e$ foremost challenge.jpg
Command 'foremost' not found, but can be installed with:
sudo apt install foremost
vahnivesh@VAHNI:/mnt/e$ sudo apt install foremost
[sudo] password for vahnivesh:
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following packages were automatically installed and are no longer required:
  libdrm-nouveau2 libdrm-radeon1 libgl1-amber-dri libglapi-mesa libllvm17t64 libxcb-dri2-0
Use 'sudo apt autoremove' to remove them.
The following NEW packages will be installed:
  foremost
0 upgraded, 1 newly installed, 0 to remove and 99 not upgraded.
Need to get 34.8 kB of archives.
After this operation, 88.1 kB of additional disk space will be used.
Get:1 http://archive.ubuntu.com/ubuntu noble/universe amd64 foremost amd64 1.5.7-11 [34.8 kB]
Fetched 34.8 kB in 1s (35.2 kB/s)
Selecting previously unselected package foremost.
(Reading database ... 48808 files and directories currently installed.)
Preparing to unpack .../foremost_1.5.7-11_amd64.deb ...
Unpacking foremost (1.5.7-11) ...
Setting up foremost (1.5.7-11) ...
Processing triggers for man-db (2.12.0-4build2) ...
vahnivesh@VAHNI:/mnt/e$ foremost challenge.jpg
Processing: challenge.jpg
|*|
vahnivesh@VAHNI:/mnt/e$

```

## What I learned


## References

used exiftool and foremost.

..................................................................

# 4. 

### 

**Flag:** `citadel{add_vinegar_twice}`

we use the key panchiko to decrpt to get the flag.



```
twj eys zpr ukm 'viamnwqw' bx lzgo: esmqqui{yyr_oshwwcm_bwupa}
now use the key 'panchiko' on flag: rigckmv{osd_ikumqog_tjkjm}

```

## What I learned


## References

NIL

..................................................................

# 5. Test of Sweetness

### 

**Flag:** `citadel{fru1tc4k3_4nd_c00k13s}`

as per the challenge, we add the become admin to get the flag, so we went to developer tools using crtl-shift-I and when to application where, in that we went to cookies, 
and then in user value we changed it to admin, and thus got the flag.




```


```

## What I learned


## References

crt - shift - I to get developer tools.

..................................................................


# 6. Rotten Apple


### 

**Flag:** `citadel{b3tt3r_ROTt3n}`

as per the challenge, we had to use rot 13 to decrypt rot 13 and then decrypt that with rot 47, and thus got the flag.



```

4:R256=Y3oRRoP0#~%Ro?A
```

## What I learned


## References

NIL

..................................................................


# 7. Randomly accessed memories

### 

**Flag:** `citadel{w3_4r3_up_4ll_n1t3_t0_g1t_lucky}`

as per the challenge, we had to go to the github page of evilcryptonite and find the flag, as per the hint, we had to view the commits, about 300+ commits where, there, i went through suspusio ones
it said added and chunk and removed a chunk, about 3 peices, it that,, it was base64 encoded, after decoding that, and thus got the flag.



```
clone it, pull it, reset it, stage it, 
commit, push it, fork, rebase it. 
merge it, branch it, tag it, log it, 
add it, stash it, diff, untrack it … 

```

## What I learned


## References

NIL

..................................................................

# 8. Selected Ambient Work

### 

**Flag:** `citadel{1_L0V3_1DM}`

after converting the wav to spectogram, we can see the flag, in morse code, we had to decode it and thus got the flag.



```


```

## What I learned


## References

NIL

..................................................................


# 9. The Robot's Trail

### 

**Flag:** `citadel{p4th_tr4v3rs4l_m4st3ry_4ch13v3d}`

this is a code snippet.

```

"Directory listing for /home/ctf/.secret:\n"
            "total 12\n"
            "drwx------ 2 ctf ctf 4096 Jan  1 10:00 .\n"
            "drwxr-xr-x 5 ctf ctf 4096 Jan  1 09:55 ..\n"
            "-r-------- 1 ctf ctf   48 Jan  1 10:00 flag.txt\n"
            "\n"
```

## What I learned


## References

NIL

..................................................................

# 10. Rotting in the Deep

### 

**Flag:** `citadel{br0_r34lly_unr0tt3d_m3_b4ck_t0_l1f3}`

as per the challenge, the python file, and key was out was given little bit of editing the python file and thus got the flag.



```
from Crypto.Util.number import *
ct = '6895840967002953721051398351211751734500850509315790892845302801984496338433523326225010635779036738800318'
flag = ''
for digit in ct:
    flag += str((int(digit)-3)%10)

print(long_to_bytes(int(flag)))
```

## What I learned


## References

NIL

..................................................................


# 11. 

### 

**Flag:** ``



```


```

## What I learned


## References

NIL

..................................................................







