Bandit Level 4 → Level 5

Objective

Retrieve the password for the next level from the only human-readable file located in the "inhere" directory.

1. Navigating to the Target Directory

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
- "ls -al": Displays all files, including hidden files, in long format.

The directory contained several files named "-file00", "-file01", and so on.

2. Identifying the Correct File

Commands used

```bash
cat ./-file00
cat ./-file01
cat ./-file02
cat ./-file03
cat ./-file04
cat ./-file05
cat ./-file06
cat ./-file07
```

Explanation

Each file was opened individually using "cat".

Most files displayed unreadable characters, making it difficult to identify the correct one.

The password was eventually found in "-file07".

3. Alternative Approach: Identifying File Types

The "file" command can identify the type of content stored in a file without displaying its contents.

For example:

```bash
file ./*
```
This command examines all files in the current directory.

The output would identify the files as follows:

- "-file00" to "-file06": "data", indicating that their contents were not recognized as a standard file format.
- "-file07": "ASCII text", indicating that it contained human-readable text using the ASCII character encoding.

This would have made it possible to identify the correct file without opening each one individually.

4. Skills Learned

- Navigating Linux directories.
- Inspecting directory contents.
- Reading files using "cat".
- Distinguishing human-readable text from binary data.
- Identifying file types using the "file" command.