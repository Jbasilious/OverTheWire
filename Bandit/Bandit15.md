# Bandit Level 15 → Level 16
## Level Goal

The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL encryption.

##### Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…
##### Commands you may need to solve this level

ssh, telnet, nc, openssl, s_client, nmap

## Solution
use openssl and s_client to connect
```
openssl s_client -connect localhost:30001
```
once connected you just paste the previous levels password and you are given the password for the next level
