# Bandit Level 8

## Goal
The password for this level is stored in the file data.txt and is the only line of text that occurs only once

## Host information:
- Host: bandit.labs.overthewire.org
- Port: 2220
- Username: bandit8
- Password: dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
  
## Process
After connected, the first thing i do is type
```bash
ls
```
I found data.txt so i just read it
```bash
cat data.txt
```
It show hundred of lines, and the password its only show once so i using 'sort' combine with 'uniq -u'
```bash
sort data.txt | uniq -u
```
- sort = Sorts all rows so that identical rows are grouped together
- uniq -u = unique only, only displays rows that appear once

## Password
```bash
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
```
