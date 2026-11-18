Bandit Level 3 → Level 4

Objective

Retrieve the password for the next level from a hidden file located inside the "inhere" directory.

1. Navigating to the Target Directory

Commands used

```bash
pwd
ls
cd inhere
```

Explanation

- "pwd": Displays the current working directory.
- "ls": Lists the contents of the current directory.
- "cd inhere": Changes the current directory to "inhere".

2. Finding the Hidden File

Command used

```bash
ls -al
```
Explanation

- "-a": Displays all files, including hidden files.
- "-l": Displays directory contents in long format, including permissions, ownership, size and modification date.

The command revealed a hidden file named "..Hiding-From-You".

3. Reading the File

Command used

```bash
cat ..Hiding-From-You
```
The command displays the contents of the file, revealing the password required for the next level.

4. Skills Learned

- Navigating directories using "cd".
- Understanding hidden files in Linux.
- Using combined options with "ls".
- Listing files in long format.
- Reading files using "cat".