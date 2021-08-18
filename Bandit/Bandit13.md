# Bandit Level 13 → Level 14
## Level Goal

The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Note: localhost is a hostname that refers to the machine you are working on
##### Commands you may need to solve this level

ssh, telnet, nc, openssl, s_client, nmap

## Solution
in the starting directory there is a file called sshkey.private i used this file as the key to ssh into the user bandit14
```
ssh -i sshkey.private bandit14@localhost
```
once connected I could read the password in  /etc/bandit_pass/bandit14 directory and read the password
```
cat /etc/bandit_pass/bandit14
```
