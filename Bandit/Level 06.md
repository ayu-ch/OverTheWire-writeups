# **Level 6**
Here we have to find a file which satisifes all the following conditions:
```
owned by user bandit7
owned by group bandit6
33 bytes in size
```

Again we can use the `find` command but here we have to search in the whole filesystem.

To put a condition of groups and user, we can use the -group and -user flag respectively.

We use '/' here to start from root.

The whole command will look like this : ` find / -type f -size 33c -group bandit6 -user bandit7`

using this we can find a `bandit7.password` file. You can `cat` the file to get the password for the next level:)
