# Bandit Level 10

## Goal
The password for the next level is stored in the file data.txt, which contains base64 encoded data

## Host information:
- Host: bandit.labs.overthewire.org
- Port: 2220
- Username: bandit10
- Password: FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
  
## Process
After connected, the first thing i do is type
```bash
ls
```
I found data.txt so i just read it
```bash
cat data.txt
```
And we get base64. so we just decode it!
```bash
cat data.txt | base64 -d
```

## Password
```bash
dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
```
