
# Bandit Level 4 → Level 5
## Level Goal

The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.
##### Commands you may need to solve this level

ls, cd, cat, file, du, find

## Solution
enter the file directory
```
cd inhere
```
shows the file type for all files in the directory, reveals -file07 is the only ASCII text file.
```
file ./-file*
```
displays file -file07 revealing the password for the next level
```
cat ./-file07
```
