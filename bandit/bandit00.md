# Bandit Level 0 

## Goal
The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 page to find out how to beat Level 1.

## Host information:
- Host: bandit.labs.overthewire.org
- Port: 2220
- Username: bandit0
- Password: bandit0
  
## Process
First i just connect via ssh using command
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

Then i type 'ls' and found readme, so i type:

```bash
cat readme
```
It show the password

## Password
```bash
ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
```
