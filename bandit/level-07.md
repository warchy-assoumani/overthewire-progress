Bandit Level 7 → Level 8

Objective

Retrieve the password for the next level from the file "data.txt".

The password is located on the same line as the word "millionth".

1. Exploring the Directory

Commands used

```bash
pwd
ls -al
```

Explanation

- "pwd": Displays the current working directory.
- "ls -al": Lists all files and directories, including hidden files, in long format.

The file "data.txt" was identified in the current directory.

2. Inspecting the File

First attempt

```bash
cat data.txt
```

This command displayed a very large amount of text, making it difficult to locate the required information manually.

3. Searching for a Specific Word

Command used

```bash
grep "millionth" data.txt
```

Explanation

- "grep": Searches for a specific text pattern in a file.
- ""millionth"": Specifies the word to search for.
- "data.txt": Specifies the file to search.

The command displayed the line containing "millionth", revealing the password required for the next level.

4. Skills Learned

- Inspecting files from the terminal.
- Understanding the limitations of displaying large files with "cat".
- Searching for specific text using "grep".
- Extracting relevant information from large text files.