# Static ain't always noise

Points: 20

## Category

General skills

## Description
>Can you look at the data in this binary: static? This BASH script might help!

## Solution
We get binary file 'static'.

There is also bash script but it's not really needed for solving this challenge.

It's enough to run *strings* on the binary and then *grep* for "pico" as it's known than flag format is "picoCTF{flag}".

So only command that needs to be ran is:
>$strings static | grep pico

And there is single line output which is the flag.

Flag:
>picoCTF{d15a5m_t34s3r_f5aeda17}