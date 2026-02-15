# Bandit Level 0 

## Goal
The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

## Host information:
- Host: bandit.labs.overthewire.org
- Port: 2220
- Username: bandit1
- Password: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
  
## Process
First i connect via ssh using command
```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
```
and enter the password
```bash
ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
```

After connected, i want to know what files inside, so i type
```bash
ls
```
It show file - so i type:
```bash
cat -
```
But it dont show anything? then i search on google how to read - file and i found that we should use specific path to read it, because without specific path, system will confused. so i type
```bash
cat ./-
```
Well done..it show the password

## Password
```bash
263JGJPfgU6LtdEvgfWU1XP5yac29mFx
```
