Bandit Level 0 → Level 1

Objective

Connect to the Bandit server using SSH and retrieve the password for the next level.

The password for the initial connection is provided by OverTheWire.

1. SSH Connection

Command used:

ssh bandit0@bandit.labs.overthewire.org -p 2220

Explanation

- "ssh": Establishes a secure remote connection.
- "bandit0": Username used for authentication.
- "bandit.labs.overthewire.org": Remote server hostname.
- "-p 2220": Specifies the SSH server port.

Technical note: SSH uses TCP port 22 by default. In this challenge, the server listens on port 2220.

2. Locating and Reading the File

Objective

The password for Level 1 is stored in a file named "readme", located in the home directory.

Commands used

pwd
ls
cat readme

Explanation

- "pwd": Displays the current working directory. Used to verify that I was in the home directory.
- "ls": Lists the contents of the current directory. Used to locate the "readme" file.
- "cat readme": Displays the contents of the "readme" file directly in the terminal.

The file contains the password required to authenticate as "bandit1".

3. Skills Learned

- Establishing remote SSH connections.
- Understanding SSH authentication.
- Specifying a custom SSH port.
- Navigating the Linux filesystem.
- Reading files from the command line.