Bandit Level 10 → Level 11

Objective

Retrieve the password for the next level from the file "data.txt".

The password is encrypted using ROT13, a letter substitution cipher.

1. Exploring the Directory

Command used

```bash
pwd && ls -la
```

Explanation

- "pwd": Displays the current working directory.
- "&&": Executes the second command only if the first command succeeds.
- "ls -la": Lists all files and directories, including hidden files, in long format.

The file "data.txt" was identified in the current directory.

2. Decoding the ROT13 Content

Command used

```bash
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

Explanation

- "cat data.txt": Displays the content of the file.
- "|": Sends the output of the first command to the next command through a pipe.
- "tr": Translates or replaces characters.
- "'A-Za-z'": Defines the uppercase and lowercase English alphabet.
- "'N-ZA-Mn-za-m'": Defines the corresponding ROT13 substitution.

ROT13 shifts each letter by 13 positions in the alphabet. Applying the same transformation again restores the original text.

The decoded output revealed the password required for the next level.

3. Skills Learned

- Understanding the ROT13 substitution cipher.
- Using "tr" to transform characters.
- Combining commands with pipes.
- Processing file contents directly from the terminal.