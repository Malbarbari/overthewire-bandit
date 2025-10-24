# OverTheWire - Bandit



hello, i`m Mohammad ali albarbari, i hope you found these writeups are helpful.



---
## Level 0
### THE GOAL
The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 page to find out how to beat Level 1.
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```
username:bandit0 && password:bandit0
```bash
bandit0@bandit:~$ ls
readme
bandit0@bandit:~$ cat readme
```
level1 password:  ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5I
---
## Level 1-2
## THE GOAL
The password for the next level is stored in a file called - located in the home directory

```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
password: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
```
### solution:
The file’s name is -, but commands think - means “read from stdin” or an option.
So when you type cat -, it waits for input instead of opening the file.
```bash 
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat ./-
263JGJPfgU6LtdEvgfWU1XP5yac29mFx
```
---
## Level 2-3
The password for the next level is stored in a file called --spaces in this filename-- located in the home directory
### THE GOAL
The password for the next level is stored in a file called --spaces in this filename-- located in the home directory
```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
password:263JGJPfgU6LtdEvgfWU1XP5yac29mFx
```
### solution 
```bash
bandit2@bandit:~$ ls
--spaces in this filename--
bandit2@bandit:~$ cat -- "--spaces in this filename--"
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
```
---
## Level 3-4
### THE GOAL
The password for the next level is stored in a hidden file in the inhere directory.
```bash
ssh bandit3@bandit.labs.overthewire.org -p 2220
```
### solution
```bash
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere/
bandit3@bandit:~/inhere$ ls
bandit3@bandit:~/inhere$ ls -a
.  ..  ...Hiding-From-You
bandit3@bandit:~/inhere$ cat ./...Hiding-From-You 
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
```
---
## Level 4-5 
### THE GOAL
The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.
### solution
```bash
ssh bandit4@bandit.labs.overthewire.org -p 2220
the password we got from the previous level
bandit4@bandit:~/inhere$ ls
-file00  -file02  -file04  -file06  -file08
-file01  -file03  -file05  -file07  -file09
bandit4@bandit:~/inhere$ file ./*
./-file00: data
./-file01: OpenPGP Public Key
./-file02: OpenPGP Public Key
./-file03: data
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: data
bandit4@bandit:~/inhere$ cat ./-file07
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
```
---
## Level 5-6
### THE GOAL
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

    human-readable
    1033 bytes in size
    not executable
### solution
```bash
ssh bandit5@bandit.labs.overthewire.org -p 2220
bandit5@bandit:~$ cd inhere/
bandit5@bandit:~/inhere$ ls
maybehere00  maybehere05  maybehere10  maybehere15
maybehere01  maybehere06  maybehere11  maybehere16
maybehere02  maybehere07  maybehere12  maybehere17
maybehere03  maybehere08  maybehere13  maybehere18
maybehere04  maybehere09  maybehere14  maybehere19
bandit5@bandit:~/inhere$ find . -type f -size 1033c
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
```
---

















