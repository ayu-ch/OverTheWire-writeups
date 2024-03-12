# **Level 18**
If we try to connect using ssh , it says `byebye` and the connection **closes**.

So i thought that since we are getting connecting for a moment and then the connection is getting closed, we can use `scp` command instead and get all the files which is present in the directory just after connecting to the server.

I used the command `scp -P2220 bandit18@bandit.labs.overthewire.org:* .`

This gave me a readme file which had password for the next level in it:))
