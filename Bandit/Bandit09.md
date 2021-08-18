
# Bandit Level 9 → Level 10
## Level Goal

The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.
##### Commands you may need to solve this level

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

## Solution

use cat, sort, strings, and grep to filter through the file  
```
cat data.txt | sort | strings | grep ==.*
```

the above command returns 4 lines, only one resembles the format of other passwords. 
