# JS Fresher
# 1. What are the different data types present in javascript?

# They are of 2 Types 

1. Primitive types
2. Non-primitive types

# In Premitive type

# String, Number,BigInt,Boolean,Undefined,Null,Symbol

BigInt - This data type is used to store numbers which are above the limitation of the Number data type. It can store large integers and is represented by adding “n” to an integer literal.

var bigInteger =  234567890123456789012345678901234567890;

Undefined - When a variable is declared but not assigned, it has the value of undefined and it’s type is also undefined.

var x; // value of x is undefined
var y = undefined; // we can also set the value of a variable as undefined

Null - It represents a non-existent or a invalid value.
var z = null;

Symbol - It is a new data type introduced in the ES6 version of javascript. It is used to store an anonymous and unique value.
var symbol1 = Symbol('symbol');
data type whose instances are unique and immutable

# 2. Non-primitive types

Primitive data types can store only a single value. 
# To store multiple and complex values, non-primitive data types are used.
# Object - Used to store collection of data.
object,Array


# Q2 Explain Hoisting in javascript.

Hoisting is the default behaviour of javascript where all the variable and function declarations are moved on top.

Check with file


//Hoisting is the default behaviour of javascript where all the variable and function declarations are moved on top.


//This means that irrespective of where the variables and functions are declared, 
//they are moved on top of the scope. The scope can be both local and global.
//Example 1
hoistedVariable = 3;
console.log(hoistedVariable);
var hoistedVariable;

// * It is only work with var 
// not with const and let


// in const and let throw an error  can not 'hoistedVariable' before initialization


//Example 2:

m1();
function m1(){
    console.log("hello world");
}
// even when the function is declared after calling


// Example 3
 
function m2(){
    x = 23;
    console.log(x);
    var x; //Hoisting takes place in the local scope as well
}

m2();

// Hoisting takes place in the local scope as well

var v;
console.log(v); // Outputs "undefined" since the initialization of "x" is not hoisted
v = 98;

// Note - To avoid hoisting, you can run javascript in strict mode by using “use strict” on top of the code:

"use strict";
z = 93; // Gives an error since 'z' is not declared
console.log(z);
var z;
# // important concept 

var foo = 1;
console.log(foo); // here we will get 1;

console.log(fooo); // here we will get undefine;   because value decleration after console in hoisting initialisation will work
                   // but in case of decleration we have to declare first then call
var fooo = 1

# 3. Why do we use the word “debugger” in javascript?

The debugger for the browser must be activated in order to debug the code. 
Built-in debuggers may be switched on and off, requiring the user to report faults.
The remaining section of the code should stop execution before moving on to the next line while debugging.

# 4. Difference between “ == “ and “ === “ operators.
Both are comparison operators. The difference between both the operators is that “==” is used to compare values whereas, “ === “ is used to compare both values and types.

# 5. Difference between var and let keyword in javascript.

Some differences are 

* From the very beginning, the 'var' keyword was used in JavaScript programming whereas the keyword 'let' was just added in 2015.

* The keyword 'Var' has a function scope. Anywhere in the function, the variable specified using var is accessible but in ‘let’ the scope of a variable declared with the 'let' keyword is limited to the block in which it is declared. Let's start with a Block Scope.

* In ECMAScript 2015, let and const are hoisted but not initialized. Referencing the variable in the block before the variable declaration results in a ReferenceError because the variable is in a "temporal dead zone" from the start of the block until the declaration is processed.

# Temporal Dead Zone is the period of time during which the let and const declarations cannot be accessed. Temporal Dead Zone starts when the code execution enters the block which contains the let or const declaration and continues until the declaration has executed.

# टेम्पोरल डेड ज़ोन उस समय की अवधि है जिसके दौरान लेट और कॉन्स्ट घोषणाओं तक पहुँचा नहीं जा सकता है। टेम्पोरल डेड ज़ोन तब शुरू होता है जब कोड निष्पादन उस ब्लॉक में प्रवेश करता है जिसमें लेट या कॉन्स्ट डिक्लेरेशन होता है और तब तक जारी रहता है जब तक कि डिक्लेरेशन निष्पादित नहीं हो जाता।

console.log(foo); // undefined
var foo = 123;

console.log(foo); // Error
let foo = 123;

# This might lead you to think that hoisting doesn’t apply to let and const; that is an incorrect assumption.

This might come as a surprise, but similar to var, variables declared with let and constants declared using const are also hoisted; it is just that how they are hoisted is different from how var variables are hoisted.

 # Let’s look at an example of code that proves that variables declared using let are also hoisted.
 
 let age = 50;

function printAge() {
  console.log(age);
  let age = 30;
}

printAge(); // Error

Running the code snippet above throws an error even though the variable age is declared in the global scope. This is because the console.log statement inside the printAge function doesn’t have access to that outer age variable, since another age variable is declared within the printAge function.


function print() {
  function log() {
    console.log(age);
  }

  const age = 20;
  log();
}

print(); // 20


How are we able to access age before its declaration?

Actually, age is accessed after the declaration of age variable because the console.log is inside another function that is called after the declaration of the age variable. By the time the age variable is accessed inside the log function, the age variable’s declaration has already been executed.

This means that it’s not about where, but about when the let variable or const constant is accessed. Temporal Dead Zone relates to time, not the space above the declaration of let or const.


# 6 Explain Implicit Type Coercion in javascript.

Implicit type coercion in javascript is the automatic conversion of value from one data type to another. It takes place when the operands of an expression are of different data types.

* String coercion

String coercion takes place while using the ‘ + ‘ operator. When a number is added to a string, the number type is always converted to the string type.

Ex 1 :- var x = 3;
var y = "3";
    
x + y // Returns "33" 

Example 2:

var x = 24;
var y = "Hello";
x + y   // Returns "24Hello"; 

Note - ‘ + ‘ operator when used to add two numbers, outputs a number. The same ‘ + ‘ operator when used to add two strings, outputs the concatenated string:

var name = "Vivek";
var surname = " Bisht";
name + surname     // Returns "Vivek Bisht" 

When JavaScript sees that the operands of the expression x + y are of different types ( one being a number type and the other being a string type ), it converts the number type to the string type and then performs the operation. Since after conversion, both the variables are of string type, the ‘ + ‘ operator outputs the concatenated string “33” in the first example and “24Hello” in the second example.

Note - Type coercion also takes place when using the ‘ - ‘ operator, but the difference while using ‘ - ‘ operator is that, a string is converted to a number and then subtraction takes place.

var x = 3;
Var y = "3";
x - y    //Returns 0 since the variable y (string type) is converted to a number type

Boolean Coercion
Boolean coercion takes place when using logical operators, ternary operators, if statements, and loop checks. To understand boolean coercion in if statements and operators, we need to understand truthy and falsy values.

Logical operators:
Logical operators in javascript, unlike operators in other programming languages, do not return true or false. They always return one of the operands.

OR ( | | ) operator - If the first value is truthy, then the first value is returned. Otherwise, always the second value gets returned.

AND ( && ) operator - If both the values are truthy, always the second value is returned. If the first value is falsy then the first value is returned or if the second value is falsy then the second value is returned.

Equality Coercion
Equality coercion takes place when using ‘ == ‘ operator. As we have stated before

# 7. Is javascript a statically typed or a dynamically typed language?

JavaScript is a dynamically typed language. In a dynamically typed language, the type of a variable is checked during run-time in contrast to a statically typed language, where the type of a variable is checked during compile-time.

Since javascript is a loosely(dynamically) typed language, variables in JS are not associated with any type. A variable can hold the value of any data type.

For example, a variable that is assigned a number type can be converted to a string type:

var a = 23;
var a = "Hello World!";


