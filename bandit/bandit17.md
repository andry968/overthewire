# Bandit Level 17 → 18

## Goal
There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new

NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19

## Host information:
- Host: bandit.labs.overthewire.org
- Port: 2220
- Username: bandit17
- Password: EReVavePLFHtFlFsjn3hyzMlvSuSAcRD
  
## Process
First we command
```bash
ls
```
The output is passwords.new and passwords.old, Next we use 'diff' to know the difference
```bash
diff passwords.old passwords.new
```
Output:
```bash
42c42
< pGozC8kOHLkBMOaL0ICPvLV1IjQ5F1VA
---
> x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO
```
The line marked with > is the new password.

## Password
```bash
x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO
```
