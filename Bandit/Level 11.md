# **Level 11**

Here we get to know about a cipher called as `ROT 13`

This cipher translates/rotates all the letters by 13 characters, eg: A will be replaced by N , B will be replaced by O ..... Z will be replaced by N.

Here we have to use the `tr` command. This is used to translate letters. For example, if i use ` tr 'a' 'z'` all the a's in my input will be changed to z.

With this we can build a ROT13 cipher, we can have the first argument as '[A-Za-z]' ,bash recognises the '-' and understands it as A to Z and a to z.

The second argument must be what the first argument must be replaced by. So have to replace A by N and Z by M , but we cannot do N-M directly here. We have to write it as N-ZA-M which means N to Z and A to M.

So the second argument will be '[N-ZA-Mn-za-m]`

Now the whole command looks like this: `cat data.txt | tr '[A-Za-z]' '[N-ZA-Mn-za-m]'`
