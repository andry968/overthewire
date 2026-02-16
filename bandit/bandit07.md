# Bandit Level 7

## Goal
The password for this level is stored in the file data.txt next to the word millionth

## Host information:
- Host: bandit.labs.overthewire.org
- Port: 2220
- Username: bandit7
- Password: morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
  
## Process
After connected, the first thing i do is type
```bash
ls
```
I found data.txt so i just read it
```bash
cat data.txt
```
It show hundred of lines, but remember if the password is next to the word 'millionth' so i type:
```bash
cat data.txt | grep millionth
```

## Password
```bash
dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
```
