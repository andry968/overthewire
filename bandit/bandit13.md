# Bandit Level 13

## Goal
The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Look at the commands that logged you into previous bandit levels, and find out how to use the key for this level.

## Host information:
- Host: bandit.labs.overthewire.org
- Port: 2220
- Username: bandit13
- Password: FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
  
## Process
After connected, the first thing i do is type
```bash
ls
```
And the output is we have sshkey.private, first i run
```bash
ssh -i sshkey.private bandit14@localhost -p 2220
```
But the connection was lost... so I copied sshkey.private to my local computer. Now that I'm on my local computer... I created a file named private.key and pasted the text from sshkey.private, and we also granted permissions.
```bash
chmod 700 private.key
ssh bandit14@bandit.labs.overthewire.org -p 2220 -i private.key
```
And BOOM!! we can access bandit 14. Next we read the password
```bash
cat /etc/bandit_pass/bandit14
```

## Password
```bash
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
```
