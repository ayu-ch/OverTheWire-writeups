# **Level 12**
This level was very long, but not to demotivate you, it was fun!

We are given with a data.txt file which is a hexdump.
`xxd` is a command used to create hexdumps and also to revert the hexdumps by using the `-r` flag.

But we dont have permissions to use it in this directory and we are supposed to do it in the directory mentioned in the challenge description, which is /tmp/{anything}

So we create a directory using `mkdir /tmp/{anything}` (mkdir stands for make directory)

Now we copy the contents of data.txt in the current directory to the directory we just made.
We use the command `cp data.txt /tmp/{anything}/data.txt`

Now we can change our working directory to the one we made by using `cd /tmp{anything}`.

Okay so we can run our hexdump revert (xxd -r) here to get the passwd. xxd reverts hex files to binaries.

The method for using it is like this  => xxd -r input output

So we can use the command `xxd -r data.txt output.bin`. This gives us a file called output.bin. We can check the details of the file by using the `file` command.

Wait what? This is a gzip compressed file. It means we have to decompress it. (Learn about gzip by using man gzip)

We can decompress gzip files by using `gzip -d` command but it needs the extension of the file as `.gz`. So now we have to rename our output.bin to output.gz. We can do this by running the command `mv output.bin output.gz'

Now that we have our gzip compressed file with its extension we can run the command : `gzip -d output.gz`. This again gave us an `output` file. We can check it using the file command. It says that it is a bzip2 compressed file.

bzip2 is also a similar command to gzip and we use -d flag to decompress it but the files extension should be .bz2
So we again rename the output file to output.bz2 and then decompress it.

We again get an output file. This is again a gzip compression data file. We repeat the above steps again.

Now we get a output file, but if we check it using the file command we can see that it is a `POSIX tar archive`.
These files should have extension as `.tar` and can be decompressed by the command `tar -xvf filemname`.

These steps are repeated a few times until we reach one moment where the output file is an ASCII text. We can cat the output and get the passwd:)
