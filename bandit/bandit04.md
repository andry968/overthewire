# Bandit Level 4

## Goal
The password for thisl evel is stored in a hidden file in the inhere directory.

## Host information:
- Host: bandit.labs.overthewire.org
- Port: 2220
- Username: bandit4
- Password: 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
  
## Process
After connected, the first thing i do is type
```bash
ls
```
It show directory inhere so i change the directory and list it
```bash
cd inhere
ls
```
The output is -file00 to -file09. We could read them one by one to get the password, but we can use 'file' to find out which ones are readable instead. So I type
```bash
file ./*
```
Few of them are data and OpenPGP Public key but file07 its the only ASCII text!. so i read it
```bash
cat ./-file07
```
And we did it

## Password
```bash
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
```
