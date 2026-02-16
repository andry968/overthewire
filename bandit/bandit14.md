# Bandit Level 14 → 15

## Goal
The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

## Host information:
- Host: bandit.labs.overthewire.org
- Port: 2220
- Username: bandit14
- Password: MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
  
## Process
After connected, the first thing i do is type
```bash
ls
```
Oops..we have nothing here.. Take a look of the hint and we must submitting the password of the current level to port 30000 on localhost. So first we type
```bash
cat /etc/bandit14_pass/bandit14
```
Ouput:
```bash
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
```
Then copy the password and type
```bash
echo "MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS" | nc localhost 30000
```
Well well well..done

## Password
```bash
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
```
