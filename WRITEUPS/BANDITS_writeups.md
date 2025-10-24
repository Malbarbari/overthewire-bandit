# OverTheWire - Bandit
hello, i`m Mohammad ali albarbari, i hope you found these writeups are helpful.
---
## level 0
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
## level1-2
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
## level 2-3
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
##  level 3-4
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











