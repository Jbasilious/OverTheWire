# Bandit Level 14 → Level 15
## Level Goal

The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.
##### Commands you may need to solve this level

ssh, telnet, nc, openssl, s_client, nmap

## Solution
 use the nc command to write data across a network connect ie to the required port on localhost
```
nc localhost 30000
4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e
```
this printed out the password for the next level 
