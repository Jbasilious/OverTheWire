
# Bandit Level 6 → Level 7
## Level Goal

The password for the next level is stored somewhere on the server and has all of the following properties:

    owned by user bandit7
    owned by group bandit6
    33 bytes in size

##### Commands you may need to solve this level

ls, cd, cat, file, du, find, grep
## Solution
use ls command to show all directories including hidden ones
```
ls -a
```

This didn't reveal anything useful so moved to the parent directory revealing directories named bandit0 through 33

```
cd ..
```
After searching around here for a while I didn't come across anything so I used cd to go back to root and searched from there.

the following command searches for the criteria specified. the last section "2>/dev/null" redirects all errors to null so they don't print out. making sure we only see the file we're looking for
```
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
```

This worked and the password file was located at
 ```
/var/lib/dpkg/info/bandit7.password
```
