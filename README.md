# Java Script
- [Introduction](#introduction)
- [var let const](#var-let-const)
- [Comparison operator](#Comparison-operator)
- [Truthy and Falsy](#Truthy-and-Falsy)
- [Ternary Operator](#Ternary-Operator)
- [Function and Hoisting](#Function-and-Hoisting)
- [Scope](#Scope)
- [Array](#Array)
- [Functions as Data](#Functions-as-Data)
- [Introduction to Iterators](#Introduction-to-Iterators)
- [The .forEach() Method](#The-.forEach()-Method)









# Introduction

JavaScript (JS) is a lightweight, interpreted, or just-in-time compiled programming language with first-class functions. While it is most well-known as the scripting language for Web pages, many non-browser environments also use it, such as Node.js, Apache CouchDB and Adobe Acrobat. JavaScript is a prototype-based, multi-paradigm, single-threaded, dynamic language, supporting object-oriented, imperative, and declarative (e.g. functional programming) styles.

JavaScript was initially created to “make web pages alive”.

The programs in this language are called scripts. They can be written right in a web page’s HTML and run automatically as the page loads.

Scripts are provided and executed as plain text. They don’t need special preparation or compilation to run.

What makes JavaScript unique?

    Full integration with HTML/CSS.
    
    Simple things are done simply.
    
    Support by all major browsers and enabled by default.
    





# var let const

    var declarations are globally scoped or function scoped while let and const are block scoped.
    
    var variables can be updated and re-declared within its scope; let variables can be updated but not re-declared; const variables can neither be updated nor re-declared.
    
    They are all hoisted to the top of their scope. But while var variables are initialized with undefined, let and const variables are not initialized.
    
    While var and let can be declared without being initialized, const must be initialized during declaration.
    
    Variables that have not been initialized store the primitive data type undefined.
    
    In ES6, template literals use backticks ` and ${} to interpolate values into a string.
    
    
```javascript

     const myPet = 'armadillo';
     console.log(`I own a pet ${myPet}.`);
     // Output: I own a pet  armadillo.
     
```
    
    
    
    
    
    The typeof keyword returns the data type (as a string) of a value.
    
    
    
```javascript
    
    const unknown1 = 'foo';
    console.log(typeof unknown1); // Output: string
 
    const unknown2 = 10;
    console.log(typeof unknown2); // Output: number
 
    const unknown3 = true; 
    console.log(typeof unknown3); // Output: boolean

```
    
 
 # Comparison operator

```javascript

 if (stopLight === 'green' && pedestrians === 0) {
  console.log('Go!');
} else {
  console.log('Stop');
}

```



# Truthy and Falsy

So which values are falsy— or evaluate to false when checked as a condition? The list of falsy values includes:

    0
    
    Empty strings like "" or ''
    
    null which represent when there is no value at all
    
    undefined which represent when a declared variable lacks a value
    
    NaN, or Not a Number
 
```javascript

let numberOfApples = 0;
 
if (numberOfApples){
   console.log('Let us eat apples!');
} else {
   console.log('No apples left!');
}
 
// Prints 'No apples left!'

```

Truthy and falsy evaluations open a world of short-hand possibilities!

Say you have a website and want to take a user’s username to make a personalized greeting. Sometimes, the user does not have an account, making the username variable falsy. The code below checks if username is defined and assigns a default string if it is not:

```javascript

let defaultName;
if (username) {
  defaultName = username;
} else {
  defaultName = 'Stranger';
}

```

If you combine your knowledge of logical operators you can use a short-hand for the code above. In a boolean condition, JavaScript assigns the truthy value to a variable if you use the || operator in your assignment:

```javascript

let defaultName = username || 'Stranger';

```

Because || or statements check the left-hand condition first, the variable defaultName will be assigned the actual value of username if is truthy, and it will be assigned the value of 'Stranger' if username is falsy. This concept is also referred to as **short-circuit evaluation**. 



# Ternary Operator
 
    In the spirit of using short-hand syntax, we can use a ternary operator to simplify an if...else statement.
    
    Comparison operators, including <, >, <=, >=, ===, and !== can compare two values.

    Take a look at the if...else statement example:
```javascript

let isNightTime = true;
 
if (isNightTime) {
  console.log('Turn on the lights!');
} else {
  console.log('Turn off the lights!');
}

```
    
We can use a ternary operator to perform the same functionality:

```javascript

isNightTime ? console.log('Turn on the lights!') : console.log('Turn off the lights!');

```
    
    
 # Function and Hoisting
 
 A function declaration consists of:

    The function keyword.
    
    The name of the function, or its identifier, followed by parentheses.
    
    A function body, or the block of statements required to perform a specific task, enclosed in the function’s curly brackets, { }.
    
```javascript

console.log(greetWorld()); // Output: Hello, World!
 
function greetWorld() {
  console.log('Hello, World!');
}

```

**Hoisting**

Hoisting is a term you will not find used in any normative specification prose prior to ECMAScript® 2015 Language Specification.

One of the advantages of JavaScript putting function declarations into memory before it executes any code segment is that it allows you to use a function before you declare it in your code. For example:

```javascript

function catName(name) {
  console.log("My cat's name is " + name);
}

catName("Tiger");

/*
The result of the code above is: "My cat's name is Tiger"
*/

```

The above code snippet is how you would expect to write the code for it to work. Now, let's see what happens when we call the function before we write it:

```javascript

catName("Chloe");

function catName(name) {
  console.log("My cat's name is " + name);
}
/*
The result of the code above is: "My cat's name is Chloe"
*/

```

Even though we call the function in our code first, before the function is written, the code still works. This is because of how context execution works in JavaScript.

Hoisting works well with other data types and variables. The variables can be initialized and used before they are declared.

JavaScript only hoists declarations, not initializations. If a variable is declared and initialized after using it, the value will be undefined.


# Function Expressions

Another way to define a function is to use a function expression. 

To define a function inside an expression, we can use the function keyword.

In a function expression, the function name is usually omitted. 

A function with no name is called an anonymous function. 

A function expression is often stored in a variable in order to refer to it.

Unlike function declarations, function expressions are not hoisted so they cannot be called before they are defined. 

To declare a function expression:

    Declare a variable to make the variable’s name be the name, or identifier, of your function. Since the release of ES6, it is common practice to use const as the keyword to declare the variable.

    Assign as that variable’s value an anonymous function created by using the function keyword followed by a set of parentheses with possible parameters. Then a set of curly braces that contain the function body.
    
```javascript

const plantNeedsWater = function(day){
  if(day === 'Wednesday')
  return true;
  else
  return false;
}
console.log(plantNeedsWater('Tuesday'));

```

# Arrow Functions

ES6 introduced arrow function syntax, a shorter way to write functions by using the special “fat arrow” () => notation.

Arrow functions remove the need to type out the keyword function every time you need to create a function.

Instead, you first include the parameters inside the ( ) and then add an arrow => that points to the function body surrounded in { } like this:

```javascript

const rectangleArea = (width, height) => {
  let area = width * height;
  return area;
};

```


# Concise Body Arrow Functions 

JavaScript also provides several ways to refactor arrow function syntax. 

The most condensed form of the function is known as concise body. We’ll explore a few of these techniques below:

    Functions that take only a single parameter do not need that parameter to be enclosed in parentheses. However, if a function takes zero or multiple parameters, parentheses are      required.
    
```javascript
    
    ZERO PARAMETERS
    cost fucntionName = () => {};

    ONE PARAMETER
    const functionName = paraOne => {};

    TWO OR MORE PARAMETERS
    const functionName = (paramOne, paramTwo) => {};
    
```


    A function body composed of a single-line block does not need curly braces. Without the curly braces, whatever that line evaluates will be automatically returned. The contents of the block should immediately follow the arrow => and the return keyword can be removed. This is referred to as implicit return.
    
```javascript

SINGLE-LINE BLOCK
const sumNumbers = numsber => number + number;

MULTI-LINE BLOCK
const sumNumbers = number => {
  const sum = number + number;
  return sum;
};

```

# Scope

An important idea in programming is scope. 

Scope defines where variables can be accessed or referenced.

While some variables can be accessed from anywhere within a program, other variables may only be available in a specific context. 


**Scope** is the idea in programming that some variables are accessible/inaccessible from other parts of the program.
    
**Blocks** are statements that exist within curly braces {}.
    
**Global scope** refers to the context within which variables are accessible to every part of the program.
    
**Global variables** are variables that exist within global scope.
    
**Block scope** refers to the context within which variables that are accessible only within the block they are defined.
    
**Local variables** are variables that exist within block scope.
    
**Global namespace** is the space in our code that contains globally scoped information.
    
**Scope pollution** is when too many variables exist in a namespace or variable names are reused.


# Array

Arrays are JavaScript’s way of making lists. Arrays can store any data types (including strings, numbers, and booleans). 

Like lists, arrays are ordered, meaning each item has a numbered position. 

Arrays in JavaScript are zero-indexed, meaning the positions start counting from 0 rather than 1. Therefore, the first item in an array will be at position 0. 

You may recall that you can declare variables with both the let and const keywords. Variables declared with let can be reassigned.

Variables declared with the const keyword cannot be reassigned. 

However, elements in an array declared with const remain mutable. 

Meaning that we can change the contents of a const array, but cannot reassign a new array or a different value. 

One of an array’s built-in properties is length and it returns the number of items in the array. 

We access the .length property just like we do with strings. Check the example below:

```javascript

const newYearsResolutions = ['Keep a journal', 'Take a falconry class'];
 
console.log(newYearsResolutions.length);
// Output: 2

```

We use dot notation, chaining a period with the property name to the array, to access the length property of the newYearsResolutions array. 

One method, **.push()** allows us to add items to the end of an array. Here is an example of how this is used:

```javascript

const itemTracker = ['item 0', 'item 1', 'item 2'];
 
itemTracker.push('item 3', 'item 4');
 
console.log(itemTracker); 
// Output: ['item 0', 'item 1', 'item 2', 'item 3', 'item 4'];

```

Notice that .push() changes, or mutates, itemTracker. You might also see .push() referred to as a destructive array method since it changes the initial array.

If you’re looking for a method that will mutate an array by adding elements to it, then .push() is the method for you! 

Another array method, **.pop()**, removes the last item of an array. 

```javascript

const newItemTracker = ['item 0', 'item 1', 'item 2'];
 
const removed = newItemTracker.pop();
 
console.log(newItemTracker); 
// Output: [ 'item 0', 'item 1' ]
console.log(removed);
// Output: item 2

```

**.pop()** returns the value of the last element. In the example, we store the returned value in a variable removed to be used for later.

**.pop()** is a method that mutates the initial array.

When you need to mutate an array by removing the last element, use **.pop()**. 

Some arrays methods that are available to JavaScript developers include: **.join(), .slice(), .splice(), .shift(), .unshift(), and .concat()**.




# Functions as Data


JavaScript functions behave like any other data type in the language; we can assign functions to variables, and we can reassign them to new variables.


```javascript

const announceThatIAmDoingImportantWork = () => {
    console.log("I’m doing very important work!");
};

const busy = announceThatIAmDoingImportantWork;
 
busy(); // This function call barely takes any space!


```

busy is a variable that holds a reference to our original function. 

If we could look up the address in memory of busy and the address in memory of announceThatIAmDoingImportantWork they would point to the same place. 

Our new busy() function can be invoked with parentheses as if that was the name we originally gave our function. 

Since functions are a type of object, they have properties such as **.length** and .name** and methods such as **.toString()**.

Since functions can behave like any other type of data in JavaScript, it might not surprise you to learn that we can also pass functions (into other functions) as parameters. 

A higher-order function is a function that either accepts functions as parameters, returns a function, or both! 

We call the functions that get passed in as parameters and invoked callback functions because they get called during the execution of the higher-order function.

JavaScript functions are first-class objects, so they have properties and methods like any object

Functions can be passed into other functions as parameters

A higher-order function is a function that either accepts functions as parameters, returns a function, or both


# Introduction to Iterators

The built-in JavaScript array methods that help us iterate are called iteration methods, at times referred to as iterators. 

Iterators are methods called on arrays to manipulate elements and return values.

Notice the different methods being called on the arrays:

    .forEach()
    .map()
    .filter()
    
    
```javascript


const artists = ['Picasso', 'Kahlo', 'Matisse', 'Utamaro'];

artists.forEach(artist => {
  console.log(artist + ' is one of my favorite artists.');
});

const numbers = [1, 2, 3, 4, 5];

const squareNumbers = numbers.map(number => {
  return number * number;
});

console.log(squareNumbers);

const things = ['desk', 'chair', 5, 'backpack', 3.14, 100];

const onlyNumbers = things.filter(thing => {
  return typeof thing === 'number';
});

console.log(onlyNumbers);

```
Output :

```
Picasso is one of my favorite artists.

Kahlo is one of my favorite artists.

Matisse is one of my favorite artists.

Utamaro is one of my favorite artists.

[ 1, 4, 9, 16, 25 ]

[ 5, 3.14, 100 ]

```


# The .forEach() Method

The first iteration method that we’re going to learn is .forEach(). Aptly named, .forEach() will execute the same code for each element of an array.

The code above will log a nicely formatted list of the groceries to the console. Let’s explore the syntax of invoking .forEach(). 

groceries.forEach() calls the forEach method on the groceries array.

.forEach() takes an argument of callback function. Remember, a callback function is a function passed as an argument into another function.

.forEach() loops through the array and executes the callback function for each element. 

During each execution, the current element is passed as an argument to the callback function.
 
The return value for .forEach() will always be undefined.


Another way to pass a callback for .forEach() is to use arrow function syntax. 

```javascript

groceries.forEach(groceryItem => console.log(groceryItem));

```

We can also define a function beforehand to be used as the callback function.

```javascript

function printGrocery(element){
  console.log(element);
}
 
groceries.forEach(printGrocery);

```

All three code snippets do the same thing. In each array iteration method, we can use any of the three examples to supply a callback function as an argument to the iterator.

It’s good to be aware of the different ways to pass in callback functions as arguments in iterators because developers have different stylistic preferences. 

Nonetheless, due to the strong adoption of ES6, we will be using arrow function syntax in the later exercises. 
 
 

 


 



    


















    
    
    
    
    
