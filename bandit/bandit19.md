# Bandit Level 19 → 20

## Goal
To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.

## Host information:
- Host: bandit.labs.overthewire.org
- Port: 2220
- Username: bandit19
- Password: cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8
  
## Process
We list it first
```bash
ls
```
There's a setuid binary bandit20-do.
This binary runs as user bandit20.
The bandit20 password is located at:
```bash
/etc/bandit_pass/bandit20
```
But we don't have permission to read that file unless we use the setuid binary. So we can use the setuid binary.
```bash
./bandit20-do cat /etc/bandit_pass/bandit20
```

## Password
```bash
0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO

```
