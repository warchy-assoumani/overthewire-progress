Bandit Level 8 → Level 9

Objective

Retrieve the password for the next level from the file "data.txt".

The password is the only line that occurs exactly once in the file.

1. Exploring the Directory

Commands used

```bash
pwd && ls -al
```

Explanation

- "pwd": Displays the current working directory.
- "&&": Executes the second command only if the first command succeeds.
- "ls -al": Lists all files and directories, including hidden files, in long format.

The file "data.txt" was identified in the current directory.

2. Finding the Unique Line

Command used

```bash
sort data.txt | uniq -u
```

Explanation

- "sort data.txt": Sorts the lines of the file.
- "|": Redirects the output of the first command to the second command (pipe).
- "uniq -u": Displays only lines that occur exactly once.

Sorting the file first is important because "uniq" only compares consecutive lines.

The command returned the unique line, revealing the password required for the next level.

3. Additional Experiment

After finding the password, I tested whether "uniq" could be used without "sort".

Command tested

```bash
uniq -u data.txt
```

The command did not return the expected result.

This experiment helped me understand that "uniq" only detects consecutive duplicate lines. Sorting the file first groups identical lines together, allowing "uniq -u" to identify the line that appears exactly once.

4. Skills Learned

- Sorting text files using "sort".
- Identifying unique lines using "uniq".
- Combining commands with pipes ("|").
- Understanding the importance of command execution order.
- Using "&&" to chain commands conditionally.