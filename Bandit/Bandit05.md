
# Bandit Level 5 → Level 6
## Level Goal

The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

    human-readable
    1033 bytes in size
    not executable

##### Commands you may need to solve this level

ls, cd, cat, file, du, find
## Solution
first use cd to enter the inhere directory
```
cd inhere
```

next use the find command to locate a file with a size of 1033 bytes

```
find -size 1033c
```

this reveals the location of the password file, use cat to read it

```
cat ./maybehere07/.file2
```
