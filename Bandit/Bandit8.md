# Bandit Level 8 → Level 9
## Level Goal

The password for the next level is stored in the file data.txt and is the only line of text that occurs only once
##### Commands you may need to solve this level

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

## Solution
use cat, sort, and uniq to filter through the file and find the unique line
```
cat data.txt | sort | uniq -u
```
