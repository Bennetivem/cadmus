### Basic Arithmatic

Adding two ints x and y: (given that they have already been initialised to a value)

```java
int z = x + y;
```

Subtracting two ints x and y:

```java
int z = x - y;
```

Dividing two ints x and y:

```java
int z = x / y;
```

Beware as x and y are ints z is also an int, and if you remember ints are whole numbers so whatever z comes out to be will be rounded down to the nearest integer.  For example, if `x` were 7, `y` were 5, then `z` were 1.

To avoid this problem you can use a double instead, so if p is a double equal to 7.0 and q is a double 5.0, we could do the following:

```java
double p = 7;
double q = 5;
double r = p / q;
//r would be 1.4
```

If, however, `p` and `q` are integers, `r` will equal `1.0`, because the `/` operator works irresepective of anything other than `p` and `q`, and their datatypes.

To multiply two integers x and y:

```java
int z = x * y;
```

The symbols for addition, subtraction, division and multiplication are `+`, `-`, `/`, `*` respectively.

#### Ex 1 (Physics)
Write a program to work out what the power in watts of a device is if the voltage is 10V and the current is 6A, and print the result.
Hint: Power (W) = Current * Voltage

#### Ex 2 (Physics)
Turn the last exercise into a method that accepts parameters for current and voltage, then returns power in watts.  Then write a program that uses the power method to calculate the energy transferred in kWh, when the current is 5A, the voltage is 14V over the space of 2 hours and print the result.
Hint: Energy transferred (kWh) = Power (kW) × Time (h)


#### Ex 3 (Physics)
Write a program to work out the kinetic energy of an object of mass 500kg that has a velocity of 12 m/s, and print the result
Hint: Kinetic Energy = 0.5 * Mass * (Velocity)^2

#### Ex 4 (Physics)
Write a program to answer the following physics question and print the result.  If a car has a mass of 800 kg and moves with a velocity of 25 m/s, what force is needed to stop the car in 50 metres?
Hint: You may want to turn the previous exercise into a method so you can easily work out   the cars kinetic energy.  You will also need the equation Energy = Force * Distance.

#### Ex 5 (Maths)
Write a program to work out the missing angle of a triangle which has two known angles of 108 degrees and 24 degrees.
Hint: The angles of a triangle must sum up to 180 degrees.

#### Ex 6 (Ecology)
![A quadrat](http://getting-in.com/wp-content/uploads/2012/09/Picture-382-300x223.png)

A standard quadrat used in school is 0.25m<sup>2</sup>. A quadrat is used to sample a random area of a field to estimate the abundance/variety/percentage coverage of a species. For a random sampling to be statistically viable, at least 3% of the area must be sampled. Write a program, given the size of an area, (say 2000m<sup>2</sup>) works out the amount of different samplings that must be done.

### Advanced Arithmatic

#### Powers
To get the value of a number to a given power you can use the `Math.pow()` function, that takes two parameters: a number; and a power; To use, however, you must import the `java.lang.Math` package. A package is essentially a collection of functions. To import `java.lang.Math`, write this at the very top of your code:

```java
import java.lang.Math;
```
Then in your `main` method, you can write:

```java
int number = 2;
int power = 3;
System.out.println(Math.pow(number, power));
// Prints 8
```

#### Square Roots
Another function in that package is the `Math.sqrt()` that returns the square root of a number.

```java
Sysem.out.println(Math.sqrt(25)); // Prints 5
```

#### Remainders
To get the remainder of an int a when divided by another int b we can use % instead of / when dividing, so a%b, where a = 7, b = 5...

```java
int n = 7 % 5;
```
would result in n being 2.

#### Ex 7 (Geometry, Physics, Chemistry, Game Programming)
Write a programs that given four numbers *x<sub>1</sub>*, *y<sub>1</sub>*, *x<sub>2</sub>* and *y<sub>2</sub>*, that are points on a graph, and calculates the distance between them, using the formula:

![Distance Formula](http://www.moomoomath.com/distance.jpg)

This is very useful in collision dectection is scientific models and game programming.
