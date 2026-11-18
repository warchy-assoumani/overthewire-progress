Bandit Level 1 → Level 2

Objective

Retrieve the password for the next level from a file named "-" located in the home directory.

1. Exploring the Directory

Commands used

```bash
pwd
ls
```

Explanation

- "pwd": Displays the current working directory.
- "ls": Lists the contents of the current directory.

The file "-" was identified in the home directory.

2. Reading a File Named "-"

First attempt

```bash
cat -
```

This command did not display the file contents as expected. The "cat" command interprets "-" as a reference to standard input (stdin), rather than as the name of a file.

Solution

```bash
cat ./-
```

Explanation

- "." represents the current directory.
- "/" separates the directory path from the filename.
- "-" is the filename.

Using "./-" explicitly specifies the file path and prevents "cat" from interpreting the filename as standard input.

3. Skills Learned

- Navigating the Linux filesystem.
- Reading files using "cat".
- Understanding relative paths.
- Understanding standard input (stdin).
- Handling filenames that begin with a hyphen.