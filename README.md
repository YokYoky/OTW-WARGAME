# OTW-WARGAME BANDIT

# Level 0 
*The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 page to find out how to beat Level 1.*

![level 1](https://lh3.googleusercontent.com/vpkDm4ElFGg6z_2JKtRwl9C7cQRbORi8r9zXLHqAs3T38eQS6QS52WKkx0oVAVHBeJr2HvZNgFxc1g1fl3H1a3WdHfb1-pf__6mBflMefl_V-TZyffbvz8h83DGujx1hHLKkYn5-RmqN3tkm5c1MhME)

SSH is an encrypted communication, used to connect to a device remotely.
To use SSH you need a username, IP address or domain name, and password.
In this level our password is bandit 0
```console
ssh [username]@[server IP]
```
```console
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

# Level  0 - 1
*The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game*

![level0-1](https://lh4.googleusercontent.com/s0NxVXkq9TlxyKjQK8psUwrim2SrZcWMm4wZSbkVSIfV08WJF0Je6toSf5NFwLHZK-COQISy_iaZRUVMxfvzqQx5PdCPRX8imYDdBFFyPa6bWn6m9d8vNsSZ0WZD-qMn94Uro3FqY9XFd76VLOVSBEQ)

> ls - **display the files and directories of your current directory**
> 
> file - **identify what kind of file type of a file**
> 
> cat - **display the contents of a file**
> 
> cd - **change directory**
> 
> du - **displays the number of blocks used for files**.
> 
> find - **find files and directories with operations**

**we don't need to use every command**

After loggin in to the ssh server, we can see that it contains readme file by using ls command. We can use cat command to display the contents of the file.

```console
bandit0@bandit:~$ ls                                                                                                    readme                                                                                                                  bandit0@bandit:~$ file readme                                                                                           readme: ASCII text                                                                                                      bandit0@bandit:~$ cat readme                                                                                            NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
```
Flag: NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
use the flag for the next level

# Level 1 - 2
```console
login: ssh bandit1@bandit.labs.overthewire.org -p 2220
password: NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
```
*The password for the next level is stored in a file called - located in the home directory*

![level1-2](https://lh4.googleusercontent.com/5N3pZo_X6L-QH6_xC-nk4BhD1w6Y2F2MJLJ_SMgMfmSUI06AfoX-YPObTOQWTJL1N2M_pQPZkuNdHPPZL4TxnHabUXVFrjbEvdi23Rr7rVWbI94RVxTUbtBduRGdRLHogYG65eJZZnHJHw6nL4yFOSQ)

[dashed filename explanation](https://www.webservertalk.com/dashed-filename)
to open a dashed file you can use redirection **<** or full path of a file ./
```console
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat < -
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
```
Flag: rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
use the flag for the next level

# Level 2 - 3
```console
login: ssh bandit2@bandit.labs.overthewire.org -p 2220
password: rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
```
*The password for the next level is stored in a file called spaces in this filename located in the home directory*
**![](https://lh4.googleusercontent.com/ie5Gx_SrEzG62BfYMNPH_15HAWkT9T1xDuXHzBWv02erQx-qELtNIoWq_D4mtBhKlLosqLcf1BwMCq-18ewn03FTdeOSxxnZv3LNFsPxw3F3CwGK9iv4b8ENqAiqukUBjRcnWIYyRAJEmsIpUCkFVDM)**

to handle the file that has spaces, you need to use blackslash before the spaces.
```console
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ cat spaces\ in\ this\ filename
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
```
Flag: aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
use the flag for the next level

# Level 3 - 4
```console
login: ssh bandit3@bandit.labs.overthewire.org -p 2220
password: aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
```
*The password for the next level is stored in a hidden file in the inhere directory.*

**![](https://lh3.googleusercontent.com/VZmrYxgPhNL5H-q8Ecy9wgKOkeyXXF7ARJr_oi5aptbuzx7WgAdWd_-SijmVAqgKT6ssIkBlXqFIHgvewa1s6s5SlRMyt0fFZBDeD4rJObK5lCE5d2389Zg3RAyOhHFe-29Vj3bFK9e8cRJTXlkiJOU)**

> ls - **display the files and directories of your current directory**
> 
> file - **identify what kind of file type of a file**
> 
> cat - **display the contents of a file**
> 
> cd - **change directory**
> 
> du - **displays the number of blocks used for files**.
> 
> find - **find files and directories with operations**

**we don't need to use every command**

```console
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere/
bandit3@bandit:~/inhere$ ls
bandit3@bandit:~/inhere$ find
.
./.hidden
bandit3@bandit:~/inhere$ cat ./.hidden
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
```
OR
```console
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ find inhere/
inhere/
inhere/.hidden
bandit3@bandit:~$ cat inhere/.hidden
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
```
Flag: 2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
use the flag for the next level

# Level 4 - 5
```console
login: ssh bandit4@bandit.labs.overthewire.org -p 2220
password: 2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
```
*The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.*
**![](https://lh4.googleusercontent.com/ncJDQeTAvLB60XPbaPzuQDe3v6EfIMYwe5Xcbe1KUz5aqT9qkH0YWwy7I0c3joUxqdf7MmBh2HYbiRjEFHj0d4TaidU-P7qvX0WqJe3r9KBVrENU-58VKp90cmmjZjDt0WseKZp0uUtbrWaHeLo1I8Y)**
by using ls command we see that it has 9 dashed files. To find the flag use file command to identify which file might contain the flag.

To get the all filetype at once use wildcard * , the asterisk or wildcard means select all files in the current directory.
```console
$ rm *.txt
```
The example above will remove all .txt files

```console
bandit4@bandit:~$ ls
inhere
bandit4@bandit:~$ cd inhere/
bandit4@bandit:~/inhere$ ls
-file00  -file01  -file02  -file03  -file04  -file05  -file06  -file07  -file08  -file09
bandit4@bandit:~/inhere$ file ./*
./-file00: data
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: data
bandit4@bandit:~/inhere$ cat ./-file07
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
```
Flag: lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
use the flag for the next level

# Level 5 - 6
```console
login: ssh bandit5@bandit.labs.overthewire.org -p 2220
password: lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
```
*The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:*
**![](https://lh6.googleusercontent.com/K5vblHlYs1ym20AoC86X2FoACiCuFMHOe2du1Y3tD1wMujTvDDrE2rFn1PKr8hwrmvNJLTPeIEldAm7z44ef_OWjpFKkw4Jiqpi1OQ-CwuIpLsoyLmqXf2txHYYbP5pGyulo4zj8uLaqFeUIOiHrnI8)**
| properties | description |
| ----------- | ----------- |
| -readable | File is readable |
| ! -executable | Not executable |
| -size 1033c | File size (n)c c = bytes |

Use the properties to solve this.
```console
bandit5@bandit:~$ cd inhere
bandit5@bandit:~/inhere$ find -readable ! -executable -size 1033c
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
```
Flag: P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

# Level 6 - 7
```console
login: ssh bandit6@bandit.labs.overthewire.org -p 2220
password: P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
```
*The password for the next level is stored **somewhere in the server** and has all of the following properties:*
**![](https://lh5.googleusercontent.com/eyPvjyksKeuB70x7pajlGbjGQJL1vbReN7nDeBJx8jluyMx0dpXPqSiJpxoOYUb0raqpVxmEiT44TuTJLyKozzMhbc3O29FkOhqamwYzjOroQYbkrQ5DMELGV8wHBgGGcQGzOaezF546ZKkvra8_QG0)**
| properties | description |
| ----------- | ----------- |
| -user | owned by user |
| -group | owned by group |
| -size 33c | File size (n)c c = bytes |

```console
bandit6@bandit:~$ find / -group bandit6 -user bandit7 -size 33c | grep password
```
the command above will find a lot of permission denied and highlight the password file because of grep. To remove the **permission denied** use /dev/null
```console
bandit6@bandit:~$ find / -group bandit6 -user bandit7 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
```
Flag: z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S


