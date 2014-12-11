# 75 - Golden Ratio Obsession

*Solution by Philip Wang (datforkbomb)*

 
## Problem

Golden Ratio Obsession was a 75 point problem in EasyCTF.

Find the Number of Digits in the 16th Fibonacci Number that Contains 1618 and is Divisible by 1618.

## Hint

Use your knowledge from the previous basic python problems! (You are not, however, limited to python for this problem - you can compute the answer in any language you'd like.)

## Solution

There are only three conditions:  the *16th* Fibonacci number that *Contains 1618*, and *is Divisible by 1618*.  We only need 1 variable, and that's the counter, to indicate that we have reached the 16th Fibonacci number that is divisible by 1618 and contains 1618.

Lets call the counter "i". 

Writing the short but *very* inefficient script: 

    i = 0
    a,b = 0,1
    while i <= 16:
        a,b, = b,a+b
        if "1618" in str(a) and a % 1618 == 0:
            print(i)
            i += 1
        if "1618" in str(a) and a % 1618 == 0 and i == 16:
            print(len(str(a)))


The purpose of this program is simple:  run the Fibonacci sequence while incrementing and outputting the counter every time that the number contains 1618 and is divisible by 1618, and finally stopping when the counter reaches 16 (At 16, the program will print the length of the Fibonacci number, not the counter length.)

     Output:
           1
           2
           3
           4
           5
           6
           7
           8
           9
           10
           11
           12
           13
           14
           15
           7092 #This is the flag.

After waiting a while,  we find that the number of digits in the 16th Fibonacci number that meets all of the problem's requirements (and the flag) to this problem is "7092".


