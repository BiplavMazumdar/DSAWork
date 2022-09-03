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






