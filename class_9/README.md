#### Functions

Functions allow us to write code once and call it a number of times throughout our program. This helps us keep code maintainable and also helps to make it dynamic.

```
function sayHello() {
	alert("Hello World!");
}
```

We can also pass in data to perform a dynamic operation:

```
function addTwo(num1, num2) {
	alert(num1 + num2);
}
```

When using JavaScript to perform operations, you may need to `return` the data outside of the function. You can do this like so:

```
function addTwo(num1, num2) {
	return num1 + num2;
}
```

To call a function after it is written, you refer to it by its name:

```
sayHello();

addTwo(1, 2);
```

## JS Loops
- Loops allow you to perform certain operations a set number of times.
- This is common to loop through an array for example and do something with each piece of data.

#### FOR Loop

```
for (var i = 0; i < 20; i++) {
	console.log(i);
}
```
## Homework: Part 1 -- Functions
Your task is to write functions that will make these various calculators work:

- Celcius to fahrenheit: celcius * (9/5) + 32
- Fahrenheit to celcius: (fahrenheit - 32) * 5/9
- Radius to circumference: 2 * Math.PI * radius
- Pythagorean theorem: Math.sqrt((a * a) + (b * b))

You have to use your developer tools to complete this assignment.


When declaring these functions, be sure to include the appropriate parameters. That's what you need to figure out.


Once they return the right number, you'll see that number appear in the console.


## STRETCH Homework: Part 1 -- Loops
- Write a for loop that will iterate from 0 to 20.
- For each iteration, it will check if the current number is even or odd, and report that to the screen (e.g. "2 is even").
- Do this using a `FOR` loop and then try to replicate the same functionality with a `WHILE` loop.
- You will have to look up the syntax for the while loop, and also the modulus (%) operator.
