# Bandit Level 16 → 17

## Goal
The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL/TLS and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

Helpful note: Getting “DONE”, “RENEGOTIATING” or “KEYUPDATE”? Read the “CONNECTED COMMANDS” section in the manpage.

## Host information:
- Host: bandit.labs.overthewire.org
- Port: 2220
- Username: bandit16
- Password: kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx
  
## Process
First, we using nmap to scan open port on localhost in the range 31000 to 32000
```bash
namp -p 31000-32000 localhost
```
Output:
```bash
PORT      STATE SERVICE
31046/tcp open  unknown
31518/tcp open  unknown
31691/tcp open  unknown
31790/tcp open  unknown
31960/tcp open  unknown
```
Then we test it manually using openssl s_client
```bash
openssl s_client -connect localhost:31046
```
Do it to all open port until we get the right one. In this case i find it in port 31790!..Then we close it and copy bandit16 password first.
```bash
cat /etc/bandit_pass/bandit16
```
Output:
```bash
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx
```
Copy the password above and connect again to port 31790
```bash
openssl s_client -connect localhost:31790 -quiet
```
Then paste the password and enter. Now we get private key. So copy the private key and exit bandit16 to local computer and make file private.key , then paste the private key from bandit16. Now we have ssh private key. Next, give the permission and connect it
```bash
chmod 700 private.key
ssh -i private.key bandit17@bandit.labs.overthewire.org -p 2220
```
Boom!! we did it... Now we can just read the password
```bash
cat /etc/bandit_pass/bandit16
```

## Password
```bash
EReVavePLFHtFlFsjn3hyzMlvSuSAcRD
```
