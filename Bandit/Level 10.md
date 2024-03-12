# **Level 10**

The description says that the password is base64 encoded inside data.txt file.

If we try to do `cat data.txt` , you will get a base64 encoded.

There is a command called as `base64` , you can check out its man page.

The command `base64` alone is used to encode strings into base64. But the command `base64 -d` is used to decode base64 string.

Here we can use the following command to get our passwd : `cat data.txt | base64 -d`
