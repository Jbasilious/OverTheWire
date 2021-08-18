# Bandit Level 7 → Level 8
## Level Goal

The password for the next level is stored in the file data.txt next to the word millionth
##### Commands you may need to solve this level
grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

## Solution
use grep command to search for the line containing the password
```
grep -G millionth data.text
```
