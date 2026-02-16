# Bandit Level 9

## Goal
The password for this level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

## Host information:
- Host: bandit.labs.overthewire.org
- Port: 2220
- Username: bandit9
- Password: 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
  
## Process
After connected, the first thing i do is type
```bash
ls
```
I found data.txt so i just read it
```bash
cat data.txt
```
Its not human readable so i use strings instead. to specificly, i combine it with grep
```bash
strings data.txt | grep "="
```

## Password
```bash
FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
```
