# Chapter 1.3: Basic Control Flow

In this chapter, we will explore basic control flow structures in programming.
Control flow structures allow you to control the execution of your code based on certain conditions or perform repetitive tasks using loops.
Understanding control flow is crucial for building more complex and interactive programs.

## Conditional Statements

Conditional statements are used to perform different actions based on different conditions.
The most common conditional statement is the `if` statement.

The syntax of the `if` statement is as follows:

```javascript
if (condition) {
  // code to execute if the condition is true
} else {
  // code to execute if the condition is false
}
```

The condition is an expression that evaluates to either `true` or `false`.
If the condition is `true`, the code block inside the `if` statement is executed.
Otherwise, if the condition is `false`, the code block inside the `else` statement (if present) is executed.

Here's an example:

```javascript
let age = 18;

if (age >= 18) {
  console.log("You are an adult.");
} else {
  console.log("You are a minor.");
}
```

In this example, if the `age` variable is greater than or equal to 18, the message "You are an adult." will be printed.
Otherwise, the message "You are a minor." will be printed.

You can also use multiple `if` statements together with `else if` statements to handle multiple conditions.
Here's an example:

```javascript
let num = 10;

if (num > 0) {
  console.log("Positive number");
} else if (num < 0) {
  console.log("Negative number");
} else {
  console.log("Zero");
}
```

In this example, different messages will be printed based on the value of the `num` variable.

### Switch Statement

Another way to handle multiple conditions is by using a switch statement.
The switch statement evaluates an expression and matches its value to various cases.
It then executes the code block associated with the matching case.

Here's the syntax of a switch statement:

```javascript
switch (expression) {
  case value1:
    // code to execute when expression matches value1
    break;
  case value2:
    // code to execute when expression matches value2
    break;
  // more cases...
  default:
  // code to execute when expression doesn't match any case
}
```

The switch statement starts by evaluating the expression.
It then compares the value of the expression with each case value.
When a match is found, the code block associated with that case is executed.
The `break` keyword is used to exit the switch statement after the matching case is executed.

Here's an example of a switch statement that checks the day of the week and logs a message accordingly:

```javascript
let day = "Monday";

switch (day) {
  case "Monday":
    console.log("It's the beginning of the week.");
    break;
  case "Friday":
    console.log("It's the end of the week.");
    break;
  default:
    console.log("It's another day of the week.");
}
```

In this example, if the `day` variable is "Monday", it will log the message "It's the beginning of the week." If the `day` variable is "Friday", it will log the message "It's the end of the week." For any other day, it will log the message "It's another day of the week."

If a 'break' keyword is not used, the execution will continue flowing into the next case.
An example of when this might be useful is the following:

```javascript
let month = "March";

switch (month) {
    case "January":
    case "March":
    case "May":
    case "July":
    case "August":
    case "October":
    case "December":
        console.log("This month has 31 days");
        break;
    case "April":
    case "June":
    case "September":
    case "November":
        console.log("This month has 30 days");
        break;
    case "February":
        console.log("This month has 28 days");
        break;
    default:
        throw;
};
```

Here, we group the months of the year based on how many days are in their room.
This allows us to only write the `console.log` statement once.

Switch statements are useful when you have multiple conditions to check against a single expression value.
They provide a concise and readable way to handle such cases.

## Loops

Loops are used to repeat a block of code multiple times.
They are useful for performing repetitive tasks or iterating over collections of data.

There are different types of loops available in JavaScript:

- The `for` loop: It allows you to execute a block of code for a specified number of times.
- The `while` loop: It repeats a block of code as long as a given condition is true.
- The `do-while` loop: It is similar to the `while` loop, but it always executes the block of code at least once before checking the condition.

Here's an example of a `for` loop that prints the numbers from 1 to 5:

```javascript
for (let i = 1; i <= 5; i++) {
  console.log(i);
}
```

This will output:

```bash
1
2
3
4
5
```

The loop starts with an initial value of `i = 1`.
It executes the code block inside the loop as long as the condition `i <= 5` is true.
After each iteration, the value of `i` is incremented by 1 using the `i++` expression.

### Summary

In this chapter, we explored basic control flow structures in programming.
We learned about conditional statements like the `if` statement, which allows us to execute code based on different conditions.
We also covered loops, such as the `for` loop, to repeat code for a specified number of times.

Additionally, we introduced the switch statement, which is useful for handling multiple conditions based on a single expression value.

In the [next chapter](./4-Assignment-1-Adventure-Game.md), we will dive into arrays and objects, which are essential data structures for organizing and manipulating data.
Understanding these data structures will expand your ability to work with more complex programs.

Keep practicing with control flow structures, as they are fundamental concepts in programming.
