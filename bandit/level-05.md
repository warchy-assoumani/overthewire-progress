Bandit Level 5 → Level 6

Objective

Retrieve the password for the next level from a file located somewhere inside the "inhere" directory.

The target file must meet three conditions:

- 1033 bytes in size.
- Not executable.
- Human-readable.

1. Exploring the Directory

Commands used

```bash
pwd
ls
cd inhere
ls -al
```

Explanation

- "pwd": Displays the current working directory.
- "ls": Lists the contents of the current directory.
- "cd inhere": Changes the current directory to "inhere".
- "ls -al": Displays all files and directories, including hidden files, in long format.

The directory contained numerous subdirectories named "maybehere", each containing several files.

Instead of inspecting every file manually, I looked for a way to filter files using specific criteria.

2. Searching by File Size

Command used

```bash
find . -type f -size 1033c
```

Explanation

- "find": Searches for files and directories.
- ".": Starts the search from the current directory, including its subdirectories.
- "-type f": Restricts the search to regular files.
- "-size 1033c": Searches for files exactly 1033 bytes in size. The "c" represents bytes.

The command returned a single result:

./maybehere07/.file2

3. Reading the File

Command used

```bash
cat ./maybehere07/.file2
```

The file contained the password required for the next level.

4. Skills Learned

- Searching recursively through directories.
- Using "find" to filter files by specific criteria.
- Filtering files by exact size.
- Understanding file paths.
- Reading files using "cat".