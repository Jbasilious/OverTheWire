# Bandit Level 11 → Level 12
## Level Goal

The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions
##### Commands you may need to solve this level

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd


## Solution
we use the tr command to translate all letters by 13
```
cat data.txt | tr [:alpha:] 'N-ZA-Mn-za-m'
```
