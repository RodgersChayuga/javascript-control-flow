# Control Flow in JavaScript
>Control flow refers to the order in which statements are executed in a program. In JavaScript, there are several control flow statements that allow you to control the flow of execution in your code.

## 1. Conditional Statements:
### 1.1. If Statement
The `if` statement is used to execute a block of code if a certain condition is true. Here's an example:

```Javascript
let num = 5;

if (num > 0) {
  console.log("The number is positive");
}

//result: The number is positive
```

>In this example, the code inside the `if` statement will only be executed if the `num` variable is greater than 0. If the condition is false, the code inside the `if` statement will be skipped.

### 1.2. If-Else Statement
The `if-else` statement is used to execute one block of code if a condition is true, and another block of code if the condition is false. Here's an example:

```Javascript
let num = -5;

if (num > 0) {
  console.log("The number is positive");
} else {
  console.log("The number is negative");
}

//result: The number is negative
```

>In this example, if the `num` variable is greater than 0, the first message will be printed. If the `num` variable is less than or equal to 0, the second message will be printed.

### 1.3. Else-If Statement
The `else-if` statement is used to test multiple conditions. It's often used in combination with `if` and `else` statements to create more complex logic. Here's an example:

```Javascript
let num = 0;

if (num > 0) {
  console.log("The number is positive");
} else if (num < 0) {
  console.log("The number is negative");
} else {
  console.log("The number is zero");
}

//result: The number is zero
```

>In this example, if the `num` variable is greater than 0, the first message will be printed. If the `num` variable is less than 0, the second message will be printed. If the `num` variable is equal to 0, the third message will be printed.

### 1.4. Ternary Operator
The ternary operator is a shorthand way of writing an `if...else` statement. It takes three operands: a condition, a value to return if the condition is true, and a value to return if the condition is false. Here's an example:

```Javascript
const age = 18;

const message = age >= 18 ? "You can vote" : "You can't vote";
console.log(message);

//result: you can vote.
```

## 2. Loop Statements:

### 2.1. For Loop
The `for` loop is used to execute a block of code a specified number of times. Here's an example:

```Javascript
for (let i = 0; i < 5; i++) {
  console.log(i);
}

//result: 0 1 2 3 4
```

>In this example, we're using a for loop to log the numbers 1 through 10 to the console. The i variable is initialized to 1, and the loop will continue as long as i is less than or equal to 10. On each iteration of the loop, the code inside the curly braces will be executed, which will log the value of i to the console. Finally, the i variable is incremented by 1 at the end of each iteration.

### 2.2. While Loop
The `while` `loop` allows us to execute a block of code as long as a certain condition is true. Here's an example:

```Javascript
let i = 0;
while (i < 5) {
  console.log(i);
  i++;
}

//result: 0 1 2 3 4
```

>At the beginning of the loop, i is initialized to 0. The loop then prints the value of i using console.log(), and increments i by 1 using the i++ statement. This process repeats until the condition i < 5 is false.

>When i is 0, the loop prints 0. Then i is incremented to 1. When i is 1, the loop prints 1, and so on. The loop continues until i is 4, at which point the loop prints 4 and increments i to 5. Since i is no longer less than 5, the loop exits and the program finishes.

>The end result is that the program prints the numbers 0 through 4 to the console, each on its own line.

### 2.3. Do-While Loop
The `do-while` loop is similar to the `while` loop, but it guarantees that the code inside the loop will execute at least once, even if the condition is initially false. Here's an example:

```Javascript
let i = 0;

do {
  console.log(i);
  i++;
} while (i < 5);

//result: 0 1 2 3 4
```

>In this example, the code inside the loop will execute at least once, even though the condition `i < 5` is initially false.

### 2.4. For...in Loop.
The `for...in` loop is used to iterate over the properties of an object. Here's an example:

```Javascript
const obj = { a: 1, b: 2, c: 3 };

for (const prop in obj) {
  console.log(`${prop}: ${obj[prop]}`);
}

//result: a: 1 b: 2 c: 3 
```

>In this example, the loop will iterate over each property of the obj object and log its key-value pair to the console.

### 2.5. For...of Loop.
The `for...of` loop is used to iterate over the values of an iterable object, such as an array. Here's an example:

```Javascript
const arr = [1, 2, 3];

for (const value of arr) {
  console.log(value);
}

//result: 1 2 3
```

>In this example, the loop will iterate over each value in the arr array and log it to the console.

## 3. Control Statements:

### 3.1. Switch Statement
The `switch` statement is used to execute different actions based on different conditions. Here's an example:

```Javascript
let day = "Monday";

switch (day) {
  case "Monday":
    console.log("Today is Monday");
    break;
  case "Tuesday":
    console.log("Today is Tuesday");
    break;
  case "Wednesday":
    console.log("Today is Wednesday");
    break;
  default:
    console.log("Today is a different day");
}

//result: Today is Monday
```

>In this example, the code will check the value of the `day` variable and execute the corresponding code block. If the `day` variable is "Monday", the first message will be printed. If it's "Tuesday", the second message will be printed, and so on. If none of the conditions match, the `default` block will be executed.

### 3.2. Continue Statement
The `continue` statement is used to skip over an iteration of a loop. It's often used in combination with `if` statements to create more complex logic. Here's an example:

```Javascript
for (let i = 0; i < 5; i++) {
  if (i === 3) {
    continue;
  }
  console.log(i);
}

//result: 0 1 2 4
```

>In this example, the loop will skip over the iteration when `i` is equal to 3, because the `continue` statement is executed.

### 3.3. Break Statement
The `break` statement is used to exit a loop early. It's often used in combination with if statements to create more complex logic. Here's an example:

```Javascript
for (let i = 0; i < 5; i++) {
  if (i === 3) {
    break;
  }
  console.log(i);
}

//result: 0 1 2
```

>In this example, the loop will exit early when `i` is equal to 3, because the `break` statement is executed.

### 3.4. Return Statement
The `return` statement is used to return a value from a function. Here's an example:

```Javascript
function add(a, b) {
  return a + b;
}

const result = add(2, 3);
console.log(result);

//result: 5
```

>In this example, the `add` function takes two parameters, adds them together, and returns the result. The result is then assigned to the `result` variable and logged to the console.

## 4. Exception Handling Statements:

### 4.1. Try-Catch Statement
The `try-catch` statement is used to handle errors in JavaScript. The `try` block contains the code that might throw an error, and the `catch` block contains the code that will handle the error if it occurs. Here's an example:

```Javascript
try {
  let x = y / 0;
} catch (err) {
  console.log(err.message);
}
```

>In this example, the code inside the `try` block will throw an error because we're trying to divide by zero. The `catch` block will catch the error and log its message to the console.

### 4.2. Label Statement
The `label` statement is used to create a label that can be used with the `break` and `continue` statements. Here's an example:

```Javascript
outerLoop:
for (let i = 0; i < 5; i++) {
  innerLoop:
  for (let j = 0; j < 5; j++) {
    if (i === 3 && j === 3) {
      break outerLoop;
    }
    console.log(i, j);
  }
}
```

>In this example, the `outerLoop` label is created and used with the `break` statement. The `break outerLoop` statement exits both the `innerLoop` and the `outerLoop` when  `i` is 3 and `j` is 3.

### 4.3. Break Statement with Label
The `break` statement can also be used with a label to exit a loop early. Here's an example:

```Javascript
outerLoop:
for (let i = 0; i < 5; i++) {
  innerLoop:
  for (let j = 0; j < 5; j++) {
    if (i === 3 && j === 3) {
      break outerLoop;
    }
    console.log(i, j);
  }
}
```

>In this example, we have two nested loops. The outer loop iterates over the numbers 0 to 4, and the inner loop also iterates over the numbers 0 to 4. When `i` is 2 and `j` is 3, the `break` statement with the `outerLoop` label is executed, which exits the outer loop entirely.

>Notice that the inner loop continues to execute until the `break` statement is encountered, and only then does the outer loop exit entirely.
