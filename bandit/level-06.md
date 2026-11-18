Bandit Level 6 → Level 7

Objective

Retrieve the password for the next level.

The password is stored somewhere on the server and the target file must meet three conditions:

- Owned by user "bandit7".
- Owned by group "bandit6".
- Exactly 33 bytes in size.

1. Exploring the Filesystem

Commands used

```bash
pwd
ls -al
cd ..
ls -al
cd ..
```

Explanation

- "pwd": Displays the current working directory.
- "ls -al": Lists all files and directories, including hidden files, in long format.
- "cd ..": Moves one directory level up.

I started in "/home/bandit6", moved to "/home", and then reached the root directory "/".

Since the target file could be located anywhere on the server, I decided to search from the root directory.

2. Searching for the Target File

First attempt

```bash
find . -user bandit7 -group bandit6 -size 33c
```

Explanation

- "find": Searches for files and directories.
- ".": Starts the search from the current directory.
- "-user bandit7": Selects files owned by user "bandit7".
- "-group bandit6": Selects files belonging to group "bandit6".
- "-size 33c": Selects files exactly 33 bytes in size. The "c" represents bytes.

The search generated numerous "Permission denied" messages because some directories were not accessible to my user.

3. Redirecting Error Messages

Command used

```bash
find . -user bandit7 -group bandit6 -size 33c 2>/dev/null
```
Explanation

The command uses output redirection to suppress permission error messages.

- "2": Refers to standard error ("stderr").
- ">": Redirects the output.
- "/dev/null": A special device that discards any data sent to it.

This allows the search results to be displayed without the permission error messages.

The command returned the following result:

./var/lib/dpkg/info/bandit7.password

4. Reading the File

Command used

```bash
cat ./var/lib/dpkg/info/bandit7.password
```

The file contained the password required for the next level.

5. Skills Learned

- Navigating the Linux filesystem.
- Understanding the root directory ("/").
- Searching recursively with "find".
- Filtering files by owner, group and size.
- Understanding standard error ("stderr").
- Redirecting error messages using "2>/dev/null".
- Reading files using "cat".