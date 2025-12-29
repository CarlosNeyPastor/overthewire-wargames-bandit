Este Projecto documentara la evolución en la resolucion de los niveles de Bandit (https://overthewire.org/wargames/bandit/)

### Level 0

The goal of this level is for you to log into the game using SSH. The host to which you need to connect is **bandit.labs.overthewire.org**, on port 2220. The username is **bandit0** and the password is **bandit0**. Once logged in, go to the [Level 1](https://overthewire.org/wargames/bandit/bandit1.html) page to find out how to beat Level 1.

##### Commands you may need to solve this level

[ssh](https://man7.org/linux/man-pages/man1/ssh.1.html)

##### Helpful Reading Material

- [Secure Shell (SSH) on Wikipedia](https://en.wikipedia.org/wiki/Secure_Shell)
- [How to use SSH on wikiHow](https://www.wikihow.com/Use-SSH)

```shell

┌─[charlie@Murkoff]─[~]
└──╼ $ssshpass -p 'bandit0' ssh bandit0@bandit.labs.overthewire.org -p2220

```

### Level 0 > Level 1

The password for the next level is stored in a file called **readme** located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

###### Commands you may need to solve this level

[ls](https://man7.org/linux/man-pages/man1/ls.1.html) , [cd](https://man7.org/linux/man-pages/man1/cd.1p.html) , [cat](https://man7.org/linux/man-pages/man1/cat.1.html) , [file](https://man7.org/linux/man-pages/man1/file.1.html) , [du](https://man7.org/linux/man-pages/man1/du.1.html) , [find](https://man7.org/linux/man-pages/man1/find.1.html)

```shell
┌─[charlie@Murkoff]─[~]
└──╼ $sshpass -p 'bandit0' ssh bandit0@bandit.labs.overthewire.org -p2220

bandit0@bandit:~$ export TERM=xterm

bandit1@bandit:~$ ls
readme

bandit1@bandit:~$ cat readme
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL

```

Conexión única: 
```shell
┌─[charlie@Murkoff]─[~]
└──╼ $sshpass -p 'bandit0' ssh bandit0@bandit.labs.overthewire.org -p2220 'cat readme'
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|
                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
```
### Level 1 > Level 2

The password for the next level is stored in a file called **-** located in the home directory

##### Commands you may need to solve this level

[ls](https://man7.org/linux/man-pages/man1/ls.1.html) , [cd](https://man7.org/linux/man-pages/man1/cd.1p.html) , [cat](https://man7.org/linux/man-pages/man1/cat.1.html) , [file](https://man7.org/linux/man-pages/man1/file.1.html) , [du](https://man7.org/linux/man-pages/man1/du.1.html) , [find](https://man7.org/linux/man-pages/man1/find.1.html)

##### Helpful Reading Material

- [Google Search for “dashed filename”](https://www.google.com/search?q=dashed+filename)
- [Advanced Bash-scripting Guide - Chapter 3 - Special Characters](http://tldp.org/LDP/abs/html/special-chars.html)

```shell 
┌─[charlie@Murkoff]─[~]
└──╼ $sshpass -p 'NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL' ssh bandit1@bandit.labs.overthewire.org -p2220

bandit1@bandit:~$ export TERM=xterm

bandit1@bandit:~$ ls
-

bandit1@bandit:~$ cat ./*
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
```

Opciones a lectura de flag
```bash
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi

bandit1@bandit:~$ cat /home/bandit1/*
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi

bandit1@bandit:~$ cat /home/bandit1/-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
```
### Level 2 > Level 3

The password for the next level is stored in a file called **spaces in this filename** located in the home directory

##### Commands you may need to solve this level

[ls](https://man7.org/linux/man-pages/man1/ls.1.html) , [cd](https://man7.org/linux/man-pages/man1/cd.1p.html) , [cat](https://man7.org/linux/man-pages/man1/cat.1.html) , [file](https://man7.org/linux/man-pages/man1/file.1.html) , [du](https://man7.org/linux/man-pages/man1/du.1.html) , [find](https://man7.org/linux/man-pages/man1/find.1.html)

#### Helpful Reading Material

- [Google Search for “spaces in filename”](https://www.google.com/search?q=spaces+in+filename)
```shell 
┌─[charlie@Murkoff]─[~]
└──╼ $sshpass -p 'rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi' ssh bandit2@bandit.labs.overthewire.org -p2220

bandit2@bandit:~$ export TERM=xterm

bandit2@bandit:~$ cat spaces\ in\ this\ filename
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG

```

Opciones a lectura de flag
```bash
bandit2@bandit:~$ cat ./*
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG

bandit2@bandit:~$ cat 'spaces in this filename'
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG

bandit2@bandit:~$ cat /home/bandit2/spaces\ in\ this\ filename
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
```
### Level 3 > Level 4

The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.

##### Commands you may need to solve this level

[ls](https://man7.org/linux/man-pages/man1/ls.1.html) , [cd](https://man7.org/linux/man-pages/man1/cd.1p.html) , [cat](https://man7.org/linux/man-pages/man1/cat.1.html) , [file](https://man7.org/linux/man-pages/man1/file.1.html) , [du](https://man7.org/linux/man-pages/man1/du.1.html) , [find](https://man7.org/linux/man-pages/man1/find.1.html)

```shell 
┌─[charlie@Murkoff]─[~]
└──╼ $sshpass -p 'aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG' ssh bandit3@bandit.labs.overthewire.org -p2220

bandit3@bandit:~$ export TERM=xterm

bandit3@bandit:~$ cd inhere/

bandit3@bandit:~/inhere$ ls -ltra
total 12
-rw-r----- 1 bandit4 bandit3   33 Oct  5 06:19 .hidden
drwxr-xr-x 3 root    root    4096 Oct  5 06:19 ..
drwxr-xr-x 2 root    root    4096 Oct  5 06:19 .

bandit3@bandit:~/inhere$ cat .hidden
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe


```

### Level 4 > Level 5

The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.

##### Commands you may need to solve this level

[ls](https://man7.org/linux/man-pages/man1/ls.1.html) , [cd](https://man7.org/linux/man-pages/man1/cd.1p.html) , [cat](https://man7.org/linux/man-pages/man1/cat.1.html) , [file](https://man7.org/linux/man-pages/man1/file.1.html) , [du](https://man7.org/linux/man-pages/man1/du.1.html) , [find](https://man7.org/linux/man-pages/man1/find.1.html)

```shell 
┌─[charlie@Murkoff]─[~]
└──╼ $

┌─[charlie@Murkoff]─[~]
└──╼ $sshpass -p '2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe' ssh bandit4@bandit.labs.overthewire.org -p2220

bandit4@bandit:~$ export TERM=xterm

bandit4@bandit:~$ file inhere/* | grep -i 'text' | cut -d ':' -f 1 | xargs cat
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR

```

### Level 5 > Level 6

The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:

- human-readable
- 1033 bytes in size
- not executable

##### Commands you may need to solve this level

[ls](https://man7.org/linux/man-pages/man1/ls.1.html) , [cd](https://man7.org/linux/man-pages/man1/cd.1p.html) , [cat](https://man7.org/linux/man-pages/man1/cat.1.html) , [file](https://man7.org/linux/man-pages/man1/file.1.html) , [du](https://man7.org/linux/man-pages/man1/du.1.html) , [find](https://man7.org/linux/man-pages/man1/find.1.html)

```shell 
┌─[charlie@Murkoff]─[~]
└──╼ $

┌─[charlie@Murkoff]─[~]
└──╼ $sshpass -p 'lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR' ssh bandit5@bandit.labs.overthewire.org -p2220

bandit5@bandit:~$ export TERM=xterm

bandit5@bandit:~$ ls -Rltra inhere/ | find ! -executable | find -size 1033c | xargs cat
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

```

### Level 6 > Level 7

The password for the next level is stored **somewhere on the server** and has all of the following properties:

- owned by user bandit7
- owned by group bandit6
- 33 bytes in size

##### Commands you may need to solve this level

[ls](https://man7.org/linux/man-pages/man1/ls.1.html) , [cd](https://man7.org/linux/man-pages/man1/cd.1p.html) , [cat](https://man7.org/linux/man-pages/man1/cat.1.html) , [file](https://man7.org/linux/man-pages/man1/file.1.html) , [du](https://man7.org/linux/man-pages/man1/du.1.html) , [find](https://man7.org/linux/man-pages/man1/find.1.html) , [grep](https://man7.org/linux/man-pages/man1/grep.1.html)

```shell
┌─[charlie@Murkoff]─[~]
└──╼ $sshpass -p 'lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR' ssh bandit6@bandit.labs.overthewire.org -p2220

bandit6@bandit:~$  export TERM=xterm

bandit6@bandit:~$ find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null | xargs cat
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S

```
### Level 7 > Level 8

The password for the next level is stored in the file **data.txt** next to the word **millionth**

##### Commands you may need to solve this level

[man](https://man7.org/linux/man-pages/man1/man.1.html), grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

```shell 
┌─[charlie@Murkoff]─[~]
└──╼ $sshpass -p 'z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S' ssh bandit7@bandit.labs.overthewire.org -p2220

bandit7@bandit:~$  export TERM=xterm

```

### Level 8 > Level 9

The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once

##### Commands you may need to solve this level

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

##### Helpful Reading Material

- [Piping and Redirection](https://ryanstutorials.net/linuxtutorial/piping.php)

```shell 
┌─[charlie@Murkoff]─[~]
└──╼ $

export TERM=xterm

```

### Level 9 > Level 10

The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.

##### Commands you may need to solve this level

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

```shell 
┌─[charlie@Murkoff]─[~]
└──╼ $

export TERM=xterm

```

### Level 10 > Level 11

The password for the next level is stored in the file **data.txt**, which contains base64 encoded data

##### Commands you may need to solve this level

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

##### Helpful Reading Material

- [Base64 on Wikipedia](https://en.wikipedia.org/wiki/Base64)

```shell 
┌─[charlie@Murkoff]─[~]
└──╼ $

export TERM=xterm

```

### Level 11 > Level 12

The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

##### Commands you may need to solve this level

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

##### Helpful Reading Material

- [Rot13 on Wikipedia](https://en.wikipedia.org/wiki/Rot13)

```shell 
┌─[charlie@Murkoff]─[~]
└──╼ $

export TERM=xterm

```

### Level 12 > Level 13

The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)

##### Commands you may need to solve this level

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd, mkdir, cp, mv, file

##### Helpful Reading Material

- [Hex dump on Wikipedia](https://en.wikipedia.org/wiki/Hex_dump)

```shell 
┌─[charlie@Murkoff]─[~]
└──╼ $

export TERM=xterm

```

### Level 13 > Level 14

The password for the next level is stored in **/etc/bandit_pass/bandit14 and can only be read by user bandit14**. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. **Note:** **localhost** is a hostname that refers to the machine you are working on

##### Commands you may need to solve this level

ssh, telnet, nc, openssl, s_client, nmap

##### Helpful Reading Material

- [SSH/OpenSSH/Keys](https://help.ubuntu.com/community/SSH/OpenSSH/Keys)

```shell 
┌─[charlie@Murkoff]─[~]
└──╼ $

export TERM=xterm

```

### Level 14 > Level 15

The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.

##### Commands you may need to solve this level

ssh, telnet, nc, openssl, s_client, nmap

##### Helpful Reading Material

- [How the Internet works in 5 minutes (YouTube)](https://www.youtube.com/watch?v=7_LPdttKXPc) (Not completely accurate, but good enough for beginners)
- [IP Addresses](http://computer.howstuffworks.com/web-server5.htm)
- [IP Address on Wikipedia](https://en.wikipedia.org/wiki/IP_address)
- [Localhost on Wikipedia](https://en.wikipedia.org/wiki/Localhost)
- [Ports](http://computer.howstuffworks.com/web-server8.htm)
- [Port (computer networking) on Wikipedia](https://en.wikipedia.org/wiki/Port_(computer_networking))

```shell 
┌─[charlie@Murkoff]─[~]
└──╼ $

export TERM=xterm
```

### Level 15 > Level 16

The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.

**Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…**

##### Commands you may need to solve this level

ssh, telnet, nc, openssl, s_client, nmap

##### Helpful Reading Material

- [Secure Socket Layer/Transport Layer Security on Wikipedia](https://en.wikipedia.org/wiki/Secure_Socket_Layer)
- [OpenSSL Cookbook - Testing with OpenSSL](https://www.feistyduck.com/library/openssl-cookbook/online/ch-testing-with-openssl.html)

```shell 
┌─[charlie@Murkoff]─[~]
└──╼ $

export TERM=xterm

```

### Level 16 > Level 17

The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

##### Commands you may need to solve this level

ssh, telnet, nc, openssl, s_client, nmap

##### Helpful Reading Material

- [Port scanner on Wikipedia](https://en.wikipedia.org/wiki/Port_scanner)

```shell 
┌─[charlie@Murkoff]─[~]
└──╼ $

export TERM=xterm

```

### Level 17 > Level 18

There are 2 files in the homedirectory: **passwords.old and passwords.new**. The password for the next level is in **passwords.new** and is the only line that has been changed between **passwords.old and passwords.new**

**NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19**

##### Commands you may need to solve this level

cat, grep, ls, diff

```shell 
┌─[charlie@Murkoff]─[~]
└──╼ $

export TERM=xterm

```
### Level 18 > Level 19

The password for the next level is stored in a file **readme** in the homedirectory. Unfortunately, someone has modified **.bashrc** to log you out when you log in with SSH.

##### Commands you may need to solve this level

ssh, ls, cat

```shell 
┌─[charlie@Murkoff]─[~]
└──╼ $

export TERM=xterm

```

### Level 19 > Level 20

To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.

##### Helpful Reading Material

- [setuid on Wikipedia](https://en.wikipedia.org/wiki/Setuid)

```shell 
┌─[charlie@Murkoff]─[~]
└──╼ $

export TERM=xterm

```

### Level 20 > Level 21

There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

**NOTE:** Try connecting to your own network daemon to see if it works as you think

##### Commands you may need to solve this level

ssh, nc, cat, bash, screen, tmux, Unix ‘job control’ (bg, fg, jobs, &, CTRL-Z, …)

```shell 
┌─[charlie@Murkoff]─[~]
└──╼ $

export TERM=xterm

```

### Level 21 > Level 22

A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

##### Commands you may need to solve this level

cron, crontab, crontab(5) (use “man 5 crontab” to access this)

```shell 
┌─[charlie@Murkoff]─[~]
└──╼ $

export TERM=xterm

```

### Level 22 > Level 23

A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** Looking at shell scripts written by other people is a very useful skill. The script for this level is intentionally made easy to read. If you are having problems understanding what it does, try executing it to see the debug information it prints.

##### Commands you may need to solve this level

cron, crontab, crontab(5) (use “man 5 crontab” to access this)

```shell 
┌─[charlie@Murkoff]─[~]
└──╼ $

export TERM=xterm
```

### Level 23 > Level 24

A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

**NOTE 2:** Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…

##### Commands you may need to solve this level

cron, crontab, crontab(5) (use “man 5 crontab” to access this)

```shell 
┌─[charlie@Murkoff]─[~]
└──╼ $

export TERM=xterm

```

### Level 24 > Level 25

A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.  
You do not need to create new connections each time

```shell 
┌─[charlie@Murkoff]─[~]
└──╼ $

export TERM=xterm
```

### Level 25 > Level 26

Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not **/bin/bash**, but something else. Find out what it is, how it works and how to break out of it.

##### Commands you may need to solve this level

ssh, cat, more, vi, ls, id, pwd

```shell 
┌─[charlie@Murkoff]─[~]
└──╼ $

export TERM=xterm

```

### Level 26 > Level 27

Good job getting a shell! Now hurry and grab the password for bandit27!

##### Commands you may need to solve this level

ls

```shell 
┌─[charlie@Murkoff]─[~]
└──╼ $

export TERM=xterm

```

### Level 27 > Level 28

There is a git repository at `ssh://bandit27-git@localhost/home/bandit27-git/repo` via the port `2220`. The password for the user `bandit27-git` is the same as for the user `bandit27`.

Clone the repository and find the password for the next level.

##### Commands you may need to solve this level

git

```shell 
┌─[charlie@Murkoff]─[~]
└──╼ $

export TERM=xterm

```

### Level 28 > Level 29

There is a git repository at `ssh://bandit28-git@localhost/home/bandit28-git/repo` via the port `2220`. The password for the user `bandit28-git` is the same as for the user `bandit28`.

Clone the repository and find the password for the next level.

##### Commands you may need to solve this level

git

```shell 
┌─[charlie@Murkoff]─[~]
└──╼ $

export TERM=xterm

```
### Level 29 > Level 30

There is a git repository at `ssh://bandit29-git@localhost/home/bandit29-git/repo` via the port `2220`. The password for the user `bandit29-git` is the same as for the user `bandit29`.

Clone the repository and find the password for the next level.

##### Commands you may need to solve this level

git

```shell 
┌─[charlie@Murkoff]─[~]
└──╼ $

export TERM=xterm

```

### Level 30 > Level 31

There is a git repository at `ssh://bandit30-git@localhost/home/bandit30-git/repo` via the port `2220`. The password for the user `bandit30-git` is the same as for the user `bandit30`.

Clone the repository and find the password for the next level.

##### Commands you may need to solve this level

git

```shell 
┌─[charlie@Murkoff]─[~]
└──╼ $

export TERM=xterm

```

### Level 31 > Level 32

There is a git repository at `ssh://bandit31-git@localhost/home/bandit31-git/repo` via the port `2220`. The password for the user `bandit31-git` is the same as for the user `bandit31`.

Clone the repository and find the password for the next level.

##### Commands you may need to solve this level

git

```shell 
┌─[charlie@Murkoff]─[~]
└──╼ $

export TERM=xterm

```
### Level 32 > Level 33

After all this `git` stuff its time for another escape. Good luck!

##### Commands you may need to solve this level

sh, man

```shell
┌─[charlie@Murkoff]─[~]
└──╼ $

export TERM=xterm

```


