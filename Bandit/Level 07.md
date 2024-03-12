# **Level 7**
This level needs the following command: `grep`

**grep** is used to search something in a string/file. It is a very versatile command. You can check its man pages for more details:)

The description says that the password is next to the word 'millionth'.

This challenge also requires you to use pipes(|). Pipes help to execute multiple commands one after another and give the output after the final one.

We can find 'millionth' by using grep like this : `cat data.txt | grep millionth`

The output we get is : `millionth	{passwd}`
