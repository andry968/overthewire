# Bandit Level 2

## Goal
The password is stored in a file called --spaces in this filename-- located in the home directory.

## Host information:
- Host: bandit.labs.overthewire.org
- Port: 2220
- Username: bandit2
- Password: 263JGJPfgU6LtdEvgfWU1XP5yac29mFx
  
## Process
First i connect via ssh using command
```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
```
And enter the password
```bash
263JGJPfgU6LtdEvgfWU1XP5yac29mFx
```
After connected, the first thing i do is type
```bash
ls
```
It show file --spaces in this filename-- so i type cat using \ like this
```bash
cat --spaces\ in\ this\ filename--
```
But the output is unreconigzed option? then i remember this isn't just because of the spaces, but because the file name begins with --.
In Linux, -- is the prefix option, so cat expects that argument, not the file name.
The solution is use -- to stop option parsing, so i command
```bash
cat -- "--spaces in this filename--"
```
And the password show up!

## Password
```bash
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
```
