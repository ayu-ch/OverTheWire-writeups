# **Level 20**
In this level , we have a setuid binary which listens to a port we give it as an arugment.

So we have to run two different terminals on the same server. I used tmux for this, we can run the command `tmux` and then using `ctrl+b c` creates a new window. To merge them , we can use `ctrl+b %` . We will now have two terminals on the same server next to each other!

So in one terminal i created a directory /tmp/{random} and stored the password of lvl20 in a txt file.

I then sent the password to a port using `nc -lp 5555 < /tmp/{random}/pass.txt

Then i switched my terminal using `ctrl+b ->` and then ran the setuid binary with the portnumber as: `./suconnect 5555`/

Then it gave me the password for the next level!!
