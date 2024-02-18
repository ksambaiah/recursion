# Recursion

Recursion is calling itself again and again is called recursive program. It has to stop somewhere otherwise it will be infinite loop, the condition
where it stops at the condition is called base condition.

We will discuss two very basic conditions we encounter in elementary mathematics.
```
n! = n * (n-1)!
0! = 1
```

Let us see how the computation of this goes for 5!

```
5 * 4!
5 * 4 * 3!
5 * 4 * 3 * 2!
5 * 4 * 3 * 2 * 1!
5 * 4 * 3 * 2 * 1 * 0!
5 * 4 * 3 * 2 * 1 * 1     # The expansion part is complete, now we have to do caluclation.
5 * 4 * 3 * 2 * 1
5 * 4 * 3 * 2
5 * 4 * 6
5 * 24
120
```

This is the example of recursion. Another one we encounter during schoold days (among many) is computing GCD of two numbers. 
Let us start with 18 and 28 GCD

```
            18) 28 (1
                18
                --
                10) 18 (1
                    10
                    --
                     8) 10 (1
                         8
                        --
                        2) 8 ( 4
                           8
                          ---
                           0
```

You may be wondering where is recursion used here? GCD of 28 and 18 is same as GCD of 18 and 10 which is 8 and 10 and it is 2 and 8 and 2 and 0. Base condition hit with zero and we stop. GCD is 2.

```
Def  GCD(a, b)
     if b is zero gcd is a
     if not gcd is GCD(b, reminder of b dividing a)
```

Chain ends because each time, reminder of b dividing a is small number than b. 
                    
