### Joseph Huang

### Part 1
### == vs. === in Javascript

Double equals is officially known as the abstract equality comparison operator while triple equals is termed the strict equality comparison operator. The difference between them is as follows: Abstract equality will attempt to resolve the data types via type coercion before making a comparison. Strict equality will return false if the types are different.

```
// abstract equality
console.log(3 == "3"); // true
 
// strict equality 
console.log(3 === "3"); // false
```
Example 1

Using two equal signs returns true because the string “3” is converted to the number 3 before the comparison is made. Three equal signs sees that the types are different and returns false. 


### String literals are different from string objects
```
console.log("This is a string." == new String("This is a string.")); // true
 
console.log("This is a string." === new String("This is a string.")); // false
```
Example 2

Why did the strict equality in example 2 returned false?
```
console.log(typeof "This is a string."); // string
 
console.log(typeof new String("This is a string.")); //object
```
Example 3

### When comparing reference types both abstract and strict comparisons will return false unless both operands refer to the exact same object.

```
var a = []; 
var b = [];
var c = a;
 
console.log(a == b); // false
console.log(a === b); // false
 
console.log(a == c); // true 
console.log(a === c); // true
```
Example 4

## What should I use?
Using the strict equality operator to increase the clarity of your code and prevent any false positives caused by abstract equality comparison. 

### Part 2
### return in js

When a return statement is called in a function, the execution of this function is stopped. If specified, a given value is returned to the function caller. JavaScript functions require an explicit return statement for returning the result of an expression (the value) from a function. If the expression is omitted, undefined is returned instead. 

```
function counter() {
  for (var count = 1; ; count++) {  // infinite loop
    console.log(count + 'A'); // until 5
      if (count === 5) {          
        return;
      }
      console.log(count + 'B');  // until 4
    }
  console.log(count + 'C');  // never appears
}

counter();

// Output:
// 1A
// 1B
// 2A
// 2B
// 3A
// 3B
// 4A
// 4B
// 5A
```