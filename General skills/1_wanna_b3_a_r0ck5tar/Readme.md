# 1_wanna_b3_a_r0ck5tar

Points: 350

## Category

General_skills

## Description
>I wrote you another song. Put the flag in the picoCTF{} flag format

## Solution
This seemed like another challenge with rockstar language.

So i started with running the program, but the output was empty.

Then i decided to use some script to translate rockstar code to code in some other language. On rockstar [github page](https://github.com/RockstarLang/rockstar) there is a plenty of transpilers. I chose python as destination language and used [rockstar-py](https://github.com/yyyyyyyan/rockstar-py).

After translating code into more readable form it was easy.

There 2 ifs in code:
 - first checks if first provided input is equal to a_guitar variable (which is `10`)
 - second checks if second provided input - Music(which is at that moment equal to `170`) variable is False/0, so in other words -- if given input is `170`

So the solution to this task is to run the program and provide input:
>10\
170

After running program with that input, the output is:
>Keep on rocking!\
66\
79\
78\
74\
79\
86\
73

Numbers are likely to be ASCII codes and indeed they were.

The text appeared to be: `BONJOVI`.

After putting mentioned text into picoCTF{} tags, the challenge was solved.

Flag:
>picoCTF{BONJOVI}

