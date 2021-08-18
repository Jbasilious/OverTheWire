# Bandit Level 12 → Level 13
## Level Goal

The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)
##### Commands you may need to solve this level

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd, mkdir, cp, mv, file

## Solution

Whoever came up with this definitely has a sense of humour, this was the software equivalent to one of the Russian nesting dolls.

because there are limited privileges in the starting directory, I took the questions advice and made a new directory under /tmp called bandit12. Then I copied the data file to the new directory.
```
mkdir /tmp/bandit12
cp data.txt /tmp/bandit12
```
from here the fun began, first step was to use xxd to revert the file from a hex dump to binary
```
xxd -r data.txt temp.txt
```
next I used the file command to determine what type of compression was used on the file

```
file temp.txt
```
this revealed the file was compressed using gzip, I then used then had to rename the file using the mv command so it would have the correct suffix for the gzip command to run
```
mv temp.txt temp.gz
```
now I could use the gzip command to decompress the file, it turns out the file had been compressed 8 times using 3 different formats, gzip, bzip2, and tar. I had to repeat the previous steps from using file to determine the compression type. then one of the following commands to decompress.
```
gzip -d temp.gz
bzip2 -d temp.bz2
tar -xf temp.tar
```

once fully decompressed I could use cat to read the file and reveal the password

```
cat temp.txt
```
