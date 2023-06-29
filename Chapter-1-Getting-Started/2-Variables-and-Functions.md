# Chapter 1.2: Variables and Functions

In this chapter, we will explore variables and functions, which are fundamental concepts in programming.
Variables allow us to store and manipulate data, while functions enable us to organize our code into reusable blocks.
By the end of this chapter, you will have a solid understanding of how to work with variables and functions in programming.

## Variables

Variables are used to store and manipulate data in programming.
They provide a way to give names to values, making it easier to work with and modify data throughout your program.

To declare a variable in JavaScript, use the `let` or `const` keyword followed by the variable name.
For example:

```javascript
let message = "Hello, world!";
const pi = 3.14;
```

In the example above, `message` is a variable that stores a string, and `pi` is a variable that stores a number.
Note that `let` is used for variables that can be reassigned, while `const` is used for variables that are meant to be constant and cannot be changed once assigned.

You can also initialize a variable without assigning a value to it.
In that case, the variable will have the value `undefined`.
For example:

```javascript
let greeting;
console.log(greeting); // Output: undefined
```

Variables can hold various types of data, including numbers, strings, booleans, objects, and more.
We'll explore these data types in more detail in later chapters.

## Functions

Functions are blocks of code that perform a specific task or set of tasks.
They allow us to break down our code into reusable and modular parts, making our programs more organized and easier to manage.
In fact, you have already called a function - `console.log()` is an in-built function of JavaScript.

To define a function in JavaScript, you can use the `function` keyword followed by the function name, a set of parentheses for parameters (if any), and curly braces to enclose the function body.
For example:

```javascript
function sayHello() {
  console.log("Hello, world!");
}
```

In the example above, `sayHello` is the name of the function.
The function body is enclosed in curly braces `{}`, and it contains the code that will be executed when the function is called.

You can also define functions with parameters, which are placeholders for values that can be passed into the function.
For example:

```javascript
function greet(name) {
  console.log("Hello, " + name + "!");
}
```

In this case, `name` is a parameter of the `greet` function.
When the function is called with an argument, the value of the argument will be assigned to the `name` parameter within the function.

To call or invoke a function, simply write its name followed by parentheses.
For example:

```javascript
sayHello(); // Output: Hello, world!
greet("John"); // Output: Hello, John!
```

Calling a function executes the code within the function body, allowing you to perform specific actions or calculations.

### Alternative Declaration

There is another way to declare a function you may see when searching for solutions online, which is the following:

```javascript
const greet = (name) => {
  console.log("Hello, " + name + "!");
};
```

This declaration is equivalent to the `greet` declaration above, just in another format.
When I write code, I usually prefer this format, but either one is fine.

## Summary

In this chapter, we explored variables and functions, which are essential concepts in programming.
Variables allow us to store and manipulate data, while functions provide a way to organize and reuse code.
You learned how to declare variables using `let` and `const`, and how to define and call functions in JavaScript.

In the [next chapter](./Chapter-1-Getting-Started/Conditional-Statements-and-Loops.md), we will delve into conditional statements and loops, which will expand your ability to control the flow of your programs.
Keep practicing with variables and functions, as they are building blocks for more complex programming concepts.
