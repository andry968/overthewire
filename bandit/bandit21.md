# Bandit Level 21 → 22

## Goal
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

## Host information:
- Host: bandit.labs.overthewire.org
- Port: 2220
- Username: bandit21
- Password: EeoULMCra2q0dSkYj561DX7s1CpBuOBt
  
## Process
First we ls to specific folder /etc/cron.d/
```bash
ls /etc/cron.d/
```
Output:
```bash
behemoth4_cleanup  cronjob_bandit22  cronjob_bandit24  leviathan5_cleanup    otw-tmp-dir
clean_tmp          cronjob_bandit23  e2scrub_all       manpage3_resetpw_job  sysstat
```
We read the bandit22
```bash
cat /etc/cron.d/cronjob_bandit22
```
Output:
```bash
@reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
* * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
```
So..it mention about /usr/bin/cronjob_bandit.sh , just read it then..
```bash
cat /usr/bin/cronjob_bandit22.sh
```
Output:
```bash
#!/bin/bash
chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
```
Yup..we get the passwords location now.. Just read it
```bash
cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
```

## Explanation
In this level, there is a cron job that runs automatically at specific times as user bandit22. The cron job is defined in a file in /etc/cron.d/. When we open the configuration, we can see what commands are being run and which script is being used. The script appears to be reading bandit22's password from /etc/bandit_pass/bandit22 and saving it to a file in /tmp. Since /tmp is readable by other users, we, as bandit21, can simply read the output file, and its contents become the password for the next level.

## Password
```bash
tRae0UfB9v0UzbCdn9cY0gQnds9GF58Q
```
