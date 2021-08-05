# Based

Points: 200

## Category

General_skills

## Description
>To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with nc jupiter.challenges.picoctf.org xxxxx.

## Solution
This task is all about converting 3 ascii interpretations into text. After connecting via netcat* there appears a prompt:
>Please give the 01110100 01100001 01100010 01101100 01100101 as a word.\
...\
you have 45 seconds.....\
\
Input:

I used simple online tool to convert binary to text. In this case it was `table`.

Next was:
>Please give me the  146 141 154 143 157 156 as a word.\
Input:

This time it was about converting from oct to text and the text was `falcon`.

Last one was:
>Please give me the 6e75727365 as a word.\
Input:

And this was obviously hex to text, so text was `nurse`.

After that system showed the flag.

Flag:
>picoCTF{learning_about_converting_values_02167de8}

