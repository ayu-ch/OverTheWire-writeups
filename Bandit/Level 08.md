# **Level 8**
This level requires you to know the sort and uniq commands. Check out their man pages for more info.

If you try to do ` cat data.txt` , there will be a lot of lines. You have to find a line which is not repeated (or the unique line)

For uniq command, it only recognises a unique line if lines similar lines are next to each other.

For this , we have to use the sort command, which sorts all the lines in an order, so that all the similar ones are next to each other.
> You can check it out using `cat data.txt | sort`
Now that all the similar lines are next to each other, we can finally use the uniq command. We can use this in a number of ways.

One is that you can use uniq -c to see how many times a line is repeated and find the one which has only 1 count (-c stands for count)

The best method is to use the -u flag , which only prints out the uniq one. So the command would be : `cat data.txt| sort | uniq -u`

The output is the passwd for the next level:)
