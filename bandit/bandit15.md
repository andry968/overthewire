# Bandit Level 15 → 16

## Goal
The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL/TLS encryption.

Helpful note: Getting “DONE”, “RENEGOTIATING” or “KEYUPDATE”? Read the “CONNECTED COMMANDS” section in the manpage.

## Host information:
- Host: bandit.labs.overthewire.org
- Port: 2220
- Username: bandit15
- Password: 8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
  
## Process
Like the level before. First we read the bandit15 password
```bash
cat /etc/bandit_pass/bandit15
```
Output:
```bash
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
```
Dont forget to copy the password and now we use openssl. But what is openssl s_client for?

openssl s_client = manual TLS/SSL client
Meaning:
- You connect to the server using encryption
- You can send encrypted data
- You can view the raw TLS process
This is OpenSSL's debugging and testing tool.

So we type:
```bash
openssl s_client -connect localhost:30001
```
After connected, we paste the password we copied before
```bash
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
```
Doneee

## Password
```bash
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx
```
