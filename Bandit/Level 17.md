# **Level 17**
We first save the sshkey given in the previous level and use it for logging to this level by this command: `ssh -i {sshkey file} bandit17@bandit.labs.overthewire.org -p 2220`

We are asked to find the uniq line in passwords.new which isnt in passwords.old file.

We can easily do this with the `diff` command.
`diff` is used to find the difference between two files.

We can use the command `diff passwords.new passwords.old`.

It will give two lines which is line unique to passwords.new and passwords.old respectively.

So the first string is our password for the next level
