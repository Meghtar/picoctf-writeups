# Nice netcat...

Points: 15

## Category

General skills

## Description
>There is a nice program that you can talk to by using this command in a shell: $ nc mercury.picoctf.net xxxx, but it doesn't speak English...

## Solution
After connecting to server using command shown in description, a lot of numbers appear.

>$ nc mercury.picoctf.net xxxx \
112 \
105 \
99 \
111 \
67 \
84 \
70 \
123 \
103 \
48 \
48 \
100 \
95 \
107 \
49 \
116 \
116 \
121 \
33 \
95 \
110 \
49 \
99 \
51 \
95 \
107 \
49 \
116 \
116 \
121 \
33 \
95 \
102 \
50 \
100 \
55 \
99 \
97 \
102 \
97 \
125 \
10 

My first guess was that it was ASCII, so decoding it would need to convert the numbers to text.

And it worked!

It could be done with simple python script, but even easier is using some free online tools like [CyberChef](https://gchq.github.io/CyberChef/).

After choosing 'From Decimal' as Recipe and providing input, the flag comes out.

Flag:
>picoCTF{g00d_k1tty!_n1c3_k1tty!_f2d7cafa}