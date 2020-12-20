# Java Script
- [Introduction](#introduction)
- [var let const](#var-let-const)
- [Comparison operator](#Comparison-operator)
- [Truthy and Falsy](#Truthy-and-Falsy)
- [Ternary Operator](#Ternary-Operator)










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
     // Output: I own a pet armadillo.
     
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
    
    
    
    
    
    
    
    
