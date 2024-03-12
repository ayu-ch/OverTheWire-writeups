# **Level  16**

In this level, we have to check which ports are open in the range of 31000 to 32000.

There is a command called as `nmap`, which is used to scan for ports which are open.

We can use the following command to get the details of which ports are open in the range: `nmap -p31000-32000 localhost -sV`. We get the following output:
```
Starting Nmap 7.80 ( https://nmap.org ) at 2024-03-12 10:10 UTC
Nmap scan report for localhost (127.0.0.1)
Host is up (0.00010s latency).
Not shown: 996 closed ports
PORT      STATE SERVICE     VERSION
31046/tcp open  echo
31518/tcp open  ssl/echo
31691/tcp open  echo
31790/tcp open  ssl/unknown
31960/tcp open  echo

```

We can see that two ports are open for SSL, we can try both , but we get the desired output from 31790.

We do the same thing we did in the previous challenge.
```
cat /etc/bandit_pass/bandit16 | openssl s_client -connect localhost:31790 -quiet
```
We now get an SSH private key
