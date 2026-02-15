# Bandit Level 3

## Goal
The password for thisl evel is stored in a hidden file in the inhere directory.

## Host information:
- Host: bandit.labs.overthewire.org
- Port: 2220
- Username: bandit3
- Password: MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
  
## Process
After connected, the first thing i do is type
```bash
ls
```
It show directory inhere so i change the directory and list
```bash
cd inhere
ls
```
After the directory changed and i list it, but it dont show anything so i type
```bash
ls -a
```
a = all, so it show hidden file, in this case it show ...Hiding-From-You, so i just read it
```bash
cat ...Hiding-From-You
```
Done easily

## Password
```bash
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
```
