# Tab, Tab, Attack

Points: 20

## Category

General_skills

## Description
>Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: Addadshashanammu.zip

## Solution
Task is really similar to previous one. At first i unzipped the file, then ran *strings* on unzipped file and grepped the result looking for "pico".

So, used commands were:
>$unzip Addadshashanammu.zip

>$strings Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet | grep pico

The only 'difficulty' in this task was that there were long names of directories, so using tab instead of writing them manually speeded up the process.

Flag:
>picoCTF{l3v3l_up!_t4k3_4_r35t!_6f332f10}