# Python Wrangling

Points: 10

## Category

General skills

## Description
>Python scripts are invoked kind of like programs in the Terminal... Can you run this Python script using this password to get the flag?

## Solution
Task is simple. At first I simply ran the python script:

>$python ende.py \
Usage: ende.py (-e/-d) [file]

On screen appeared information on how to properly use the script. User has to provide option (-e probably for encryption or -d probably for decription) and file to encrypt/decrypt.

So I provided that data.
>$python ende.py -d flag.txt.en

Then I got prompt to enter the password. The password is inside pw.txt, so it's enough to paste it after getting the prompt like below:

>$python ende.py -d flag.txt.en \
Please enter the password:192ee2db192ee2db192ee2db192ee2db

Other method can be 'automating it' by simply putting everything to one line:
>$python ende.py -d flag.txt.en < pw.txt

Flag:

>picoCTF{4p0110_1n_7h3_h0us3_192ee2db}