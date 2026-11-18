Bandit Level 2 → Level 3

Objective

Retrieve the password for the next level from a file whose name contains spaces.

1. Exploring the Directory

Commands used

```bash
pwd
ls
ls -l
```

Explanation

- "pwd": Displays the current working directory.
- "ls": Lists the contents of the current directory.
- "ls -l": Displays directory contents in long format, including file permissions, ownership, size and modification date.

The file "--spaces in this filename--" was identified in the home directory.

2. Reading a Filename Containing Spaces

First attempt

```bash
cat ./--spaces in this filename--
```

This command returned a "No such file or directory" error.

The shell interpreted the spaces as argument separators, splitting the filename into several arguments.

Solution

```bash
cat "./--spaces in this filename--"
```

Explanation

Double quotes ("" "") tell the shell to treat the enclosed text as a single argument.

This allows "cat" to correctly interpret the entire path, including its spaces, as one filename.

3. Skills Learned

- Navigating the Linux filesystem.
- Using "ls" and its options.
- Understanding shell argument parsing.
- Handling filenames containing spaces.
- Using quotation marks to preserve a filename as a single argument.