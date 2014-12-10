# 75 - Golden Ratio Obsession

Golden Ratio Obsession was a 75 point problem in EasyCTF.
 
## Problem

Find the Number of Digits in the 16th Fibonacci Number that Contains 1618 and is Divisible by 1618.

## Hint

Use your knowledge from the previous basic python problems! (You are not, however, limited to python for this problem - you can compute the answer in any language you'd like.)

## Solution

There are only three conditions:  the *16th* Fibonacci number that *Contains 1618*, and *is Divisible by 1618*.  We only need 1 variable, and that's the counter, to indicate that we have reached the 16th Fibonacci number that is divisible by 1618 and contains 1618.

Lets call the counter "i". 

Writing the simple but *very* inefficient script: 

    i = 0
    a,b = 0,1
    while i <= 16:
        a,b, = b,a+b
        if "1618" in str(a) and a % 1618 == 0:
            print(i)
            i += 1
        if "1618" in str(a) and a % 1618 == 0 and i == 16:
            print(len(str(a)))


The concept of this program is very simple:  run the Fibonacci sequence while incrementing the counter every time that the number contains 1618 and is divisible by 1618, and finally stopping when the counter reaches 16.

Waiting a while,  we find that the flag to this problem is "7092."

        
