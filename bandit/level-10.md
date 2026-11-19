Bandit Level 9 → Level 10

Objective

Retrieve the password for the next level from the file "data.txt".

The password is stored in a Base64-encoded format.

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

2. Decoding the Base64 Content

Command used

```bash
base64 -d data.txt
```

Explanation

- "base64": Encodes or decodes data using Base64.
- "-d": Decodes the input instead of encoding it.
- "data.txt": Specifies the file containing the encoded content.

The command decoded the Base64 content and displayed the password required for the next level.

3. Skills Learned

- Exploring the Linux filesystem.
- Understanding Base64 encoding.
- Decoding data using the "base64" command.
- Using command-line tools to retrieve encoded information.