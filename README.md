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


