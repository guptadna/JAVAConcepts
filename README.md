Java Concepts
=====

********************************************************** START **************************************************

**java certificate note -1- Operator & Precedence**

![Alt text](/operatorPrecedence.png?raw=true "Optional Title")

```
& and | do not short circuit the expression but && and || do.

Bitwise operator 
Bitwise and (&) --> all bits are set, result is set
Bitwise or(|) --> any bit is set, result is set
Bitwise xor(^) --> one or more bit but not all bits is/are set, result will be set
Bitwise one Complement (~) -->
Bitwise left Shift (>>) -->  all the bits will be pushed to left, that removes left side bits and adds 0 at the right side
Bitwise Right Shift (<<) ( shows bigger number) -->  all the bits will be pushed to LEFT, that removes LEFT MOST bits and adds 0 at the RIGHT side

```
**Difference between Logical And ( && ) and Bitwise And (&)**

&& compares boolean only
```
int x = -10 --> (-) is unary operator
int x = 11-10 --> (-) is Arithmetic operator


int x = (-10)%(-3);  --> x is -1, not 1 --> % goes by numerator sign.
int x = (-10)%(3);  --> x is -1, not 1 --> % goes by numerator sign.
int x = (10)%(-3);  --> x is 1,  % goes by numerator sign.

```

Integer i ; i++ --> throws runtime exception as NullPointerException;
Integer i=10; i++ --> 11; */

*************************************************** START **********************************************************
