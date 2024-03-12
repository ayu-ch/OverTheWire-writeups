# **Level 13**
When you login, you can see a sshkey.private file in your current directory.

This is for the next level, you can use the sshkey.private to login to the next level.

We have to use the following command here: `ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220`
This way you can login to level 14. Now we know that the passwd is stored inside /etc/bandit_pass/bandit14 so if we cat it , we get the password for level14.

But the description of level 14 says that we have to send this password to a port 30000 on localhost.
This means that there is a process which is listening at port 30000 on our localhost and we have to send this password.

To connect a remote server, we usually use the `nc` command.

so we can do 
```
cat /etc/bandit_pass/bandit14 | nc localhost 30000
```

We get a password in response!
Exit now and use this password for level 15:)
