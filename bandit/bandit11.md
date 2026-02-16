# Bandit Level 11

## Goal
The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

## Host information:
- Host: bandit.labs.overthewire.org
- Port: 2220
- Username: bandit11
- Password: dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
  
## Process
After connected, the first thing i do is type
```bash
ls
```
I found data.txt so i just read it
```bash
cat data.txt
```
Its a ROT13. What we gonna do is decrypt it
```bash
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```
- 'A-Za-z' → all uppercase + lowercase
- 'N-ZA-Mn-za-m' → its ROT13 counterpart
- tr will convert letters one by one

## Password
```bash
7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
```
