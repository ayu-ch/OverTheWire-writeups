# **Level 5**
Again we see an inhere directory, we change our directory to it using `cd inhere`

We now can see multiple directories in this directory and each directory has multiple files.

It will take a long time to use file now.

Here comes a command called as `find` . This is used to find any type of file anywhere, along with conditions of the file.

First we can use the following command: `find . -type f`. The '.' stands for the current working directory. This find us files inside the current directory. We will get a big output but we will sort it out.

There is a condition for size which says that the file should be of 1033 bytes or characters.
There is a `-size` flag in find command for this purpose.

We can use the following command : `find . -type f -size 1033c`. This find us a file with a size of 1033 characters/bytes. 

Surprisngly, this alone gives us a single file, we dont have to check for other conditions.

But just for knowledge, we can check if a file is exectuable  or not by using the -executable flag , if we have to check if its not executable then we can do `find . -type f -size 1033c ! -executable`.

We will get the respective file and we can print it to get the passwd.
