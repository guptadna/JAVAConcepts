Java Concepts
=====

*************************************** START **************************************************

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

*************************************** END **************************************************

*************************************** START **************************************************
**java certificate note -3- Inheritance/ polymorphism / overloading/ overriding / interface / class - Completed**

**Inheritance**
```

1) method dynamic binding(runtime) works (if same name methods are defined in parent and child class)

2) dynamic binding does not work with static as static methods are tied to class.

3) static variables are copied from parent to child class so static variables declared in parent class can be accessed using child class name.

4) static methods are NOT copied from parent to child class so static methods declared in parent class can NOT be accessed using child class name. 

5) variable binding will be at compile time.6) final class cannot be extended 
```


**Static Variable in Inheritance**

**Static variable and method declared in Parent class can be accessed:**

```
staticVar;
Parent.staticVar;
Child.staticVar;
new Parent().staticVar;
new Child().staticVar;
```
**Instance variable and method declared in Parent class can be accessed:**
```
instanceVar;
new Parent().instanceVar;
new Child().instanceVar;
```

**Dynamic Binding**

When parent and child class have same method name and overriding exist - Dynamic biding happens and parent reference type has object of child class will access child method.

If parent method is throwing checked exception, child method is runtime or no exception, in case of overriding or dynamic binding, compilation error as parent object at compile time think about parent method which is having checked exception so should be handled.
```
 Parent ptoC = new Child();
 ptoC.commonM(); //dynamic binding concept - access child method
 ```
*************************************** END **************************************************


