# Bandit Level 18 → 19

## Goal
The password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.

## Host information:
- Host: bandit.labs.overthewire.org
- Port: 2220
- Username: bandit18
- Password: x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO
  
## Process
First thing i do is connect via SSH like usual, but .bashrc is modified → every time you log in to SSH it automatically logs out (Byebye!). So we cant login?? I was think so until i know that we can use SSH to execute commands directly, and not an interactive shell. We know that the password for the next level is stored in a file readme so i command:
```bash
ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme 
```

## Password
```bash
cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8
```
