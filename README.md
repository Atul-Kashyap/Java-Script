# Java Script
- [Introduction](#introduction)
- [var let const](#var-let-const)












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
    
    
    
    
    
    
    
    
    
    
