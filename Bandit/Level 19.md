# **Level 19**
This is a simple challenge which uses a setuid binary.

If we try running the binary using `./bandit20-do` , it says :
```
Run a command as another user.
  Example: ./bandit20-do id
```
On running `./bandit20-do id` , it gives the following output
```
uid=11019(bandit19) gid=11019(bandit19) euid=11020(bandit20) groups=11019(bandit19)
```
whereas if we just run id , we get :
```
uid=11019(bandit19) gid=11019(bandit19) groups=11019(bandit19)
```
so we can get access of anything which has requires the permission of bandit20. Our interest lies in getting the password for the next level.

Hence we execute the following command : `./bandit20-do cat /etc/bandit_pass/bandit20` and we get the passwd
