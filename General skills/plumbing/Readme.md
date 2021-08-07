# plumbing

Points: 200

## Category

General_skills

## Description
>Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to jupiter.challenges.picoctf.org xxxxx.

## Solution
Name of this challenge is `plumbing` which suggests usage of `pipes`. The task is really simple. After connecting to the server, it gives a lot of text as output. Most of the output is useless gibberish.

So the idea is to somehow filter the output. Using grep is great idea here. It's enough to redirect output from the server to grep and search for flag.

>$nc jupiter.challenges.picoctf.org xxxxx | grep pico

returns the flag :)

Flag:
>picoCTF{digital_plumb3r_ea8bfec7}

