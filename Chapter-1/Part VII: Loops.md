Loops
===

Loops are very important to programmers as they allow us to do complicated, long winded calculations in a short amount of time.

There a four main loops in Java, the **for loop**, **while loop**, **do loop**, and **array loop**.  With each loop you have an initial condition, a final condition, and a set of instructions.  The set of instructions will continue to run until the final condition is met.

### For loop

For loops are mostly used for counting up or down in steps, usually in steps of one.  The initial condition is an int which you can initialise to a value of your choice (most of the time we use 0 if counting up to a certain value), then we have a final condition so the value you want to count up or down to.  We also have a function to increase the number of steps , for increasing by one we will use ++ (as described previously), and for decreasing by one we will use --.  So now you know how a for loop works it is time to show you what one looks like.  Below is a for loop which starts at 0, counts up by 1 each step, and prints out the number of each step, until 10 steps have been reached.  (Notice the parameters of the method countTen says void, this is because the method does not require any parameters, and putting void is more clear than simply leaving the parameters blank)

```java
public void countTen(void) {
	for(int n = 0; n <= 10 ; n++) {
		System.out.println(n) ;
	}
}
```

So in the brackets of the for loop we initialise a variable called n to 0, and we use n++ to increase n by 1 each step, and we continue to do this for when n is less than or equal to 10.  So as the loop is first run the program checks to see whether the value of n meets the final condition (n<=10), since 0 is less than 10, n meets the condition, the piece of code within the {} is run once, and then n is increased by one, then the program checks to see whether the new value of n meets the final condition, since 1 is still less than 10 the code inside of the {} of the for loop is run once again, and this process continues until n is no longer less than or equal to 10, so this will happen when n is 11.  Once this occurs the for loop finishes and the code inside of the loop is no longer run.  Once you understand how a for loop works, the rest of the loops are fairly easy to pick up!

So onto the while loop.  The while loop has only one condition and if the condition is met then the code is run, otherwise the loop finishes.  Below is an example of a while loop. (With while loops, variables must be initialised before the loop starts)

#### Ex 1 (Maths)
Use a loop of your choice to print out all the multiples of 9 within the range 0-108.
 
#### Ex 2 (Maths)
Write a function, that when given a number, calculates whether it is a prime number.

#### Ex 3 (Maths)
Write a function, that when given a number, prints an array of all its factors.

#### Ex 4 (Music)
Write a function, that prints the lyics of [99 Bottles of Beer](http://99-bottles-of-beer.net/lyrics.html), with a loop.
Extension: Add a variable to change the number of bottles.

### While loop
 
```java
public void countTenWithWhileLoop(void) {
	int n = 0;
	while (n<=10) {
		System.out.println(n);
	}
}
```

Do you see any problems with this loop?  This is an example of an infinite loop, which is a loop that never ends; as n stays the same.  In order for the loop to finish, we need to include a piece of code to change the value of n.  Hopefully you would notice that we could use n++ to do this.  So the correct loop would look like this

```java
public void countTenWithWhileLoop(void) {
	int n = 0;
	while (n <= 10) {
		System.out.println(n);
		n++;
	}
}
```

The best way of having an infinite loop is to use a while loop and set the condition to true. This way the condition is always true and so the code always gets executed.  It would look like this:

```java
while(true) {
	// code to execute
}
```

#### Ex 5 (Maths)
Write a function, that prints all the multiples of a given number, while they are under a hundred.

#### Ex 6 (Maths)
The sequence of triangle numbers is generated by adding the natural numbers. So the 7th triangle number would be 1 + 2 + 3 + 4 + 5 + 6 + 7 = 28. The first ten terms would be:

1, 3, 6, 10, 15, 21, 28, 36, 45, 55, ...

Use your function from Ex 3 plus a while loop, to create a function that returns the first triangular number with more than 20 factors.

### Do loop

Now onto the do loop.  This loop is nearly exactly the same as the while loop.  However the piece of code within the loop is run before checking to see if the condition is met.  This guarantees that the do loop is always run at least once.  Here is an example of the do loop.

```java
public void countTenWithDoLoop(void) {
	int n=0 ;
	do {
		System.out.println(n);
		n++;
	} while (n<=9);
}
```

Notice here we must change 10 to 9, as if we keep it as 10, once n becomes 11 the piece of code will be run and then the program will check to see if the condition is met.

#### Ex 7 (Computer Science)
Write a program, that uses a do loop to prompt the user for a number, checks whether it's a number, and repeats until it is actually a number.

### Array loop

Finally the array loop.  This is just a more succinct way of loop through an array. It is constructed like a `for` loop, but inside the parentheses, you write: a variable instantiation of type of a given item of the array; a comma; and the name of the array.

```java
public void printIntArray(void) {
	for(int n : nameOfArray) {
		System.out.println(n);
	}
}
```

Now that you have covered all of the different types of loops I will give you an example of a more complicated loop which will sum the numbers from 0 to 20

```java
public void sumFirstFifteenNumbers(void) {
	int sum = 0;
	// we must initialise sum outside the loop, otherwise it would keep getting initialised to 0 each time the loop runs
	for (int n = 0; n <= 20; n++) {
		sum = sum + n;
	}
	System.out.println(sum); // this prints out the final sum
}
```