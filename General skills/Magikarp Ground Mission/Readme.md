# Magikarp Ground Mission

Points: 30

## Category

General_skills

## Description
>Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin. Login via `ssh` as `ctf-player` with the password, `********`

## Solution
After launching challenge instance i connected via ssh using credentials from description.

First thing to do was to run *ls*.
>$ ls \
1of3.flag.txt  instructions-to-2of3.txt

So the flag is divided into 3 parts and there are instructions how to get to next part.

Cating 1st part of flag:
>$ cat 1of3.flag.txt\
picoCTF{xxsh_

Instruction said:
>$ cat instructions-to-2of3.txt\
Next, go to the root of all things, more succinctly `/`

So

>$ cd / && ls\
2of3.flag.txt  bin  boot  dev  etc  home  instructions-to-3of3.txt  lib  lib64  media  mnt  opt  proc  root  run  sbin srv  sys  tmp  usr  var

And here was 2nd part of flag and further instructions.

>$ cat 2of3.flag.txt\
0ut_0f_\\/\\/4t3r_

>$ cat instructions-to-3of3.txt\
Lastly, ctf-player, go home... more succinctly `~`

So last part would be going to `~` which can be done by just 
>$ cd

Then
>$ ls\
3of3.flag.txt  drop-in

Displaying content of 3rd part of flag:
>$ cat 3of3.flag.txt\
3ca613a1}

And now i just had to connecty those 3 parts of flag.

Flag:
>picoCTF{xxsh_0ut_0f_\\/\\/4t3r_3ca613a1}

