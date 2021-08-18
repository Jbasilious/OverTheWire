# Bandit Level 16 → Level 17
## Level Goal

The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.
##### Commands you may need to solve this level

ssh, telnet, nc, openssl, s_client, nmap

## Solution
I used the nmap command to scan ports 31000-32000
```
nmap -p 31000-32000 localhost
```

this revealed 5 open ports in the range, however there services were "unknown" so a trial and error approach had to be taken to determine which was the correct port.


### entering this here to save my progress

correct port is 31790
