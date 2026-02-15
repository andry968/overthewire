# Bandit Level 5

## Goal
The password for the level is stored in a file somewhere under the inhere directory and has all of the following properties:

    human-readable
    1033 bytes in size
    not executable


## Host information:
- Host: bandit.labs.overthewire.org
- Port: 2220
- Username: bandit5
- Password: 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
  
## Process
After connected, the first thing i do is type
```bash
ls
```
It show directory inhere so i change the directory and list it
```bash
cd inhere
ls
```
The output is maybehere00 to maybehere17 folder!. We dont have the time, didnt we? so i take a look of the hint
```bash
human-readable
1033 bytes in size
not executable
```
We can use 'find' with filter based on size, in this case 1033c. so i type
```bash
find . -type f -size 1033c
```
The output say ./maybehere07/.file2. Then we could just read it
```bash
cat ./maybehere07/.file2
```

## Password
```bash
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
```
