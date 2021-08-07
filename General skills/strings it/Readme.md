# strings it

Points: 100

## Category

General_skills

## Description
>Can you find the flag in file without running it?

## Solution
Just run strings on the file and then *grep* looking for "pico".

>$strings strings | grep pico
picoCTF{5tRIng5_1T_d66c7bb7}

Flag:
>picoCTF{5tRIng5_1T_d66c7bb7}

