# flag_shop

Points: 300

## Category

General_skills

## Description
>There's a flag shop selling stuff, can you buy a flag? Source. Connect with nc jupiter.challenges.picoctf.org xxxxx.

## Solution
After connecting to server, user is given a simple interface which allows to buy flags and check account balance.

User has only 1100 dollars, while proper flag costs 100000 dollars. User can also buy `Defintely not the flag flag` which i will be calling `fakeflag` for 900 dollars each.

My first idea was to buy -1 `fakeflag` and see if my account balance increases to 2000. But it didn't do anything.
As visible in code, there is line
```
if(number_flags > 0)
```
which prevents it from exploiting it this way.

Second idea was to overflow the counter, so the amount of flags would be > 0, while the price would go negative.

In code, price is represented by `int` type, which usual range is from -2,147,483,647 to 2,147,483,647 (of course can vary depending on platform). 

So now i needed to buy amount of `fakeflags` which would exceed upper limit (2,147,483,647).

```
2 147 483 647 / 900 ~ 2 386 092
```

If amount of `flakeflags` exceeds `2 386 092`, then price will go negative and user's balance will grow a lot.

So I tried buying `2 386 095` flags and it worked!

>These knockoff Flags cost 900 each, enter desired quantity\
2386095\
\
The final cost is: -2147481796\
\
Your current balance after transaction: 2147482896

The balance is surely enough to buy challenge flag, so that should be the end :)

```
Your current balance after transaction: 2147482896

Welcome to the flag exchange
We sell flags

1. Check Account Balance

2. Buy Flags

3. Exit

 Enter a menu selection
2
Currently for sale
1. Defintely not the flag Flag
2. 1337 Flag
2
1337 flags cost 100000 dollars, and we only have 1 in stock
Enter 1 to buy one1
YOUR FLAG IS: picoCTF{m0n3y_bag5_68d16363}
```

Flag:
>picoCTF{m0n3y_bag5_68d16363}

