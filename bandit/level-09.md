Bandit Level 9 → Level 10

Objective

Retrieve the password for the next level from the file "data.txt".

The password is stored in one of the human-readable strings, preceded by several "=" characters.

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

2. Initial Search Attempt

Command used

```bash
grep "=" data.txt
```

Result

grep: data.txt: binary file matches

The command detected matching content but identified the file as binary, so it did not display the matching lines normally.

To investigate the file further, I used:

```bash
file ./*
```

The output identified "data.txt" as "data", indicating that its contents were not recognized as a standard file format.

3. Exploring Different Approaches

First approach: Using cat -v

```bash
cat -v data.txt | grep "="
```

The "-v" option makes certain non-printable characters visible in the terminal.

This allowed me to see the matching lines, but the output was still difficult to read.

I then narrowed the search:

```bash
cat -v data.txt | grep "==="
```

This reduced the results to lines containing at least three consecutive "=" characters, but the output was still not ideal.

Second approach: Using grep -a

```bash
grep -a "===" data.txt
```

The "-a" option forces "grep" to process the file as text, even when it contains binary data.

However, the output was still not as clean as expected.

4. Final Solution: Using strings

Command used

```bash
strings data.txt | grep "==="
```

Explanation

- "strings": Extracts sequences of printable characters from a file.
- "|": Passes the output of "strings" to the next command.
- "grep "==="": Searches the extracted strings for three or more consecutive "=" characters.

This approach produced a much cleaner output and allowed me to identify the password required for the next level.

5. Skills Learned

- Searching through files containing binary data.
- Understanding how "grep" handles binary files.
- Using "cat -v" to display non-printable characters.
- Forcing text processing with "grep -a".
- Extracting printable strings using "strings".
- Combining commands with pipes ("|").