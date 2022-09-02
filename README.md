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
