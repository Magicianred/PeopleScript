<h1 align="center"><b>PeopleScript</b></h1>
<br>
<br>
<h3 align="center">Documentation for understanding JavaScript meticulously.</h3>
<br>
<br>
<hr>

## `var` Statement Variable Declaration

```javascript
//
//  var-statement.js
//

'use strict';

/* This is a globally-scoped variable declaration. */ 
var beverage = "unsweetened tea";

console.log(beverage); // => unsweetened tea

if (beverage === "unsweetened tea")
{
  /* 
    This is another globally-scoped variable declaration,
    but it will not override the first declaration of 
    the variable "beverage".
  */ 
  var beverage; // !== undefined
  
  console.log(beverage) // => unsweetened tea

  /* 
    This is also another globally-scoped variable 
    declaration, but it overrides the first declaration of
    the variable "beverage" due to the "=" assignment 
    operator.
  */
  var beverage = "water";

  console.log(beverage) // => water
}

function chooseDifferentBeverage() {
  /* 
    This is a function-scoped variable declaration. Therefore,
    this "beverage" variable may only be used within this block
    of the current function.
   */ 
  var beverage = "coffee";
  console.log(beverage); // => coffee;
}

chooseDifferentBeverage();

console.log(beverage); // => water

```