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
**java certificate note -2- Exception**

![Alt text](/exceptionHandling.png?raw=true "Optional Title")


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
 
**Casting**

Parent reference type with child object, parent reference type can access only parent method, 
To enable access to child method, we need to use casting. 
```
Parent ptoC = new Child();
ptoC.parentM();
((Child) ptoC).childM();   // casting example
 ```
 
Parent class reference with child class object, to access child methods ( if not overriding ) requires CASTING otherwise compilation error.
 ```
 Child ctoP = (Child) new Parent(); INVALID CASTING
 ```
**Overriding**

The compiler performs the following checks when you override a nonprivate method:

The method from child class must have the same signature as the method in the parent class.

Access Identifier - Equal or Widening - The method from child class must be at least as accessible or more accessible than the method in the parent class.

The method from child class may not throw a checked exception that is new or broader than the class of any exception thrown from the parent class method.

If the method returns a value, it must be the same or a subclass of the method in the parent class.

Ex : parent method --> Object m(){}; Child method --> String m(){}; --> Correct

Java is not possible to override a private method in a parent class since the parent method is not accessible from the child class.

Java can redeclare a new method in the child class with the same or modified signature as the method in the parent class.

This method in the child class is a separate and independent method, unrelated to the parent version's method.

Override --> Final method cannot be overridden.

Override --> Private method cannot be overridden.

Override --> Static method cannot be overridden. Static method looks to overridden but it is hidden.

Override --> If a method cannot be inherited then it cannot be overridden.

*Exam Tip : If parent method is throwing checked exception, child method is runtime or no exception, in case of overriding or dynamic binding, compilation error as parent object at compile time think about parent method which is having checked exception so should be handled.*

 
**Exception with Overriding Rules**
When parent method has :

1) No Exception --> Overriding method can NOT throw checked exception.
2) Unchecked Exception--> Overriding method can Not throw checked exception.
3) Checked Exception --> Overriding method can NOT throw new or  broader checked exception

**Overloading**

Overloading --> In Overloading/polymorphism exception can differ. Access modifier can differ. 
Overloaded methods must have different method parameters from one another.
Overloaded methods may or may not define a different return type. 
Overloaded methods may or may not define different access modifiers. 


Using the same Method name but with different argument is called overloading.

Constructors can also be overloadedOverloaded Methods must have different argument set.

Overloaded Methods may have different return type.

Overloaded Methods may have different access modifier.

Overloaded Methods may throw different exception broader or narrowno restriction.

Methods from super class can also be overloaded in subclass.

Polymorphism applies to overriding not Overloading.

Determining which overloaded Method will be invoked is decided atcompile time on the basis of the reference type.

Overloaded methods can’t be defined by only changing their return type or access modifiers.
*************************************** END **************************************************


