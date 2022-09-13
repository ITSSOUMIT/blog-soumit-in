## 'this' keyword in Javascript

***this*** keyword works differently in different context of the program. It's value depends on where it is defined or invoked.

The value of ***this*** would be different outside the function and would be different inside it. The same works when you invoke inside a function or inside a method of an object.

> **This** keyword refers to an object that is executing the current piece of code.

Value of ***this*** changes based on the below context -

### Global Context
In global context, ***this*** refers to the global object i.e., window object
```
console.log(this);
// This will return -
// Window {window: Window, self: Window, document: 
// document, name: '', location: Location, ...}
```

Adding any property/method with ***this*** in the global context will add them to global object or simply in window object.

### Function Context
Value of ***this*** in function depends upon where they are defined and invoked.

**Simple invocation -**
```
function writeMessage(){
    if(this===window){
        console.log("true");
    }
} // output- true

/* OR */
"use strict";
function writeMessage(){
    if(this===undefined){
        console.log("true");
    }
} // output- true
```
***this*** in simple invocation of function returns window object in non-strict mode and returns undefined when in strict mode.

**Method invocation -**
```
let car = {
    brand: "suzuki",
    display: function(){
        return this.brand;
    }
};
console.log(car.display());
```
***this*** when invoked in method of an object, refers to the object, the method is defined in.

**Constructor invocation - **
```
function Fruits(breed, model){
    this.breed=breed;
    this.model=model;
}
let fruit1=new Fruits('apple', 1999);
console.log(fruit1);
```
***this*** in constructor function creates an empty object and then refers to this objects.