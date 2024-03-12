# **Level 15**
In this level we have to send the password of our current level to the port 30001 on localhost with SSL encryption.

Study a bit about SSL and how to send data using SSL. You can check it [here](https://gist.github.com/azadkuh/8957116).

We can see that we can use:
```
to send some data:
$> openssl s_client -connect server:portNum
then type in console of client / server.
```
So to send our password we can use `cat /etc/bandit_pass/bandit15 | openssl s_client  -connect localhost:30001 -quiet`

Then we will get our password for the next level:)
