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


# 11.Coco Conjecture 

### 

**Flag:** `citadel{k1ryu_c0c0_h4s_4_g0_4t_4n_uns0lv3d_m4th3m4t1cs_pr0bl3m}`

as per the challenge,it was a math problem, with py script, With the help of the pdf we can make a function that will calculate the collatz steps for each number returned by the server, and using helper.md which is provided along with the pdf, we can modify the script to communicate with the instance via socket or pwntools.



```


```

## What I learned


## References

NIL

..................................................................

# 12. schlagenheim

### 

**Flag:** `citadel{8lackM1D1wa5c00l}`

as per the challenge, we are suppose to convert the wav to midi, using hex editor, after successfully, editing the audio played, after that, i put it in spectogram to read the flag and thus got it.



```


```

## What I learned


## References

NIL

..................................................................

# 13. XOR Slide

### 

**Flag:** `citadel{pyr4m1d+x0r}`

as per the challenge, i edited the script and thus got the flag.



```
from pwn import xor

ct = bytes.fromhex('b31113bd631c7207ec9587b32e686c8b6df255d66f4a987adacf6c283875ded5d1633b5f8823fa0b9bbbfab3195f1a51506afd54e03392ae338d872445c9025d88c8d4425a00a9b4478f86acadbd781df6a4194e376c09145a6f9afcbe02d36b5709f74d910edf94552dc4680041d6717fea824718c21385bdfd6176f722100548336d10ead87f01a95c5497dcb6c2')
wrapper = [
    b'bro i have a cRAzy story to tell you i went to ant4rctica and BOOM i saw a random citadel{', 
    b'} it was crazy like how did it get there??'
]

lf = len(ct)
lks = len(wrapper[0] + wrapper[1])
lr = lf - lks

ks = bytearray(lks)
x0 = lambda i, arr: xor(ct[i], wrapper[0][i], *arr)
x1 = lambda i, arr: xor(ct[i], wrapper[1][i], *arr)

for i in range(len(wrapper[0])):
    ks[i] = int.from_bytes(x0(i, ks[max(0, i - lr):i]))

for i in range(-1, -len(wrapper[1]) - 1, -1):
    a = ks[lks + i : min(lks + i + lr + 1, lks)]
    ks[i] = int.from_bytes(x1(i, a))

print(f'ks: {ks.hex()}')

flag = bytearray(ct)

for i in range(len(flag) - len(ks) + 1):
    for j in range(len(ks)):
        flag[i + j] = flag[i + j] ^ ks[j]

print(flag.decode())

```

## What I learned


## References

NIL

..................................................................


# 14. The Sound of Music

### 

**Flag:** `citadel{c0mputers_st0pped_exchang1ng_1nf0rmat10n_n_started_shar1ng_st0r1es_n_then_they_were_n0where_t0_be_f0und}`

this a part 2 oinst for citadweller, first i went to last.fm where in description i found the first half the flag, then in the music board, there i found the 2nd half, and following the link below it, i went to spotify page, where i would the final half, and thus joined and got the flag.



```


```

## What I learned


## References

NIL

..................................................................


# 15. Echoes and Pings

### 

**Flag:** `citadel{1_r34lly_w4nt_t0_st4y_4t_y0ur_h0us3}`

using wireshark getting the pings, and then uploading those url to aduacity got me the flag.



```


```

## What I learned


## References

NIL

..................................................................


# 16. The Ripper

### 

**Flag:** `citadel{fake_flag_4_fake_pl4y3rs}`

this was really easy, as practice in pwn college, i used john the ripper, and thus got the flag.



```
vahnivesh@VAHNI:/mnt/e$ john --wordlist=wordlist.txt hash.txt
Loaded 1 password hash (bcrypt [Blowfish 32/64 X3])
No password hashes left to crack (see FAQ)
vahnivesh@VAHNI:/mnt/e$ john --show hash.txt
?:fake_flag_4_fake_pl4y3rs

1 password hash cracked, 0 left
vahnivesh@VAHNI:/mnt/e$

```

## What I learned


## References

NIL

..................................................................

# 17. AetherCorp NetprobeX

### 

**Flag:** `citadel{bl4ck51t3_4cc3ss_gr4nt3d}`

as per the challenge, we had to bypass the ping commands, and use cat %0atac etc commands,
so we did that and i found a path with blacksite.dat file,and thus got the flag.



```
Figure out that %0A can be used to chain commands.
Using ls command, we can find the files in the directory.
Using less command, we can read the contents of the mission_briefing.txt file.
The file hints that the key is hidden deep within the AetherCorp network.
Find the aethercorp directory in /var/lib/ and navigate to it.
Use ls command to find the files in the aethercorp directory.
Use ls /var/lib/aethercorp/archive -a command to find .secrets directory.
Use ls /var/lib/aethercorp/archive/.secrets command to find blacksite_key.dat file.
Use less /var/lib/aethercorp/archive/.secrets/blacksite_key.dat command to read the contents of the blacksite_key.dat file and get

```

## What I learned


## References

NIL

..................................................................

..................................................................












