# Bandit Level 20 → 21

## Goal
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

NOTE: Try connecting to your own network daemon to see if it works as you think

## Host information:
- Host: bandit.labs.overthewire.org
- Port: 2220
- Username: bandit20
- Password: 0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO
  
## Process
First we list it
```bash
ls
```
Here we have suconnect. Then we run it
```bash
./suconnect
```
Output:
```bash
Usage: ./suconnect <portnumber>
This program will connect to the given port on localhost using TCP. If it receives the correct password from the other side, the next password is transmitted back.
```
So we must use 2 terminal and connect it in the same port. First we copy first the password of bandit20
```bash
0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO
```
In the first terminal we run
```bash
mc -l 12345
```
And paste the password of bandit20

In the seccond terminal, we connect it first into bandit20@bandit.labs.overthewire.org via SSH like usual, then we run
```bash
./suconnect 12345
```
Output:
```bash
Read: 0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO
Password matches, sending next password
```
We go back to the first terminal and Boom! we get the passwords!

## Explanation
The suconnect program runs with bandit21 privileges, even though you're still running bandit20. It connects to localhost on the port you specified and then waits for a line of text from the connection. If the text it receives matches bandit20's password, the program assumes "okay, valid," and since it has bandit21 privileges, it immediately retrieves the bandit21 password and sends it back to the connection.

The trick: you create your own server using nc. So when suconnect connects, you only send it the bandit20 password. The program trusts that input, passes the check, and finally gives you the bandit21 password.

## Password
```bash
EeoULMCra2q0dSkYj561DX7s1CpBuOBt
```
