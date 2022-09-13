## map(), filter(), reduce() in Javascript

What if we want to perform a function on each individual array element ?  
Let us consider a case, where we want to form a new array, from elements of an old array multiplied by 2.  
```
oldArr = [1, 2, 3, 4, 5]
newArr = [2, 4, 6, 8, 10]
```

The basic approach would be -
1. Iterate over array elements through for loop to access each individual elements.
2. Running the function for each element.
3. Passing the result to the new array

```
let oldArr = [1, 2, 3, 4, 5];
let newArr = [];
for(let i=0; i<oldArr.length; i++){
    newArr.push(oldArr[i]*2);
}
console.log(newArr);
// Output- [2, 4, 6, 8, 10]
```

Obviously, this was a small task, so using for loops isn't a big problem. But, when the task is complex, this approach would not be clear. To make task on array elements cleaner and shorter, we can use **map()**, **filter()** & **reduce()** based on when to use each.

### map()
***map()*** transforms each array element in a clean and short way.
1. Create a function that you want to apply.
2. Use this function as a callback in map().  

This way, the function will be applied to each array element.
```
let oldArr = [1, 2, 3, 4, 5]
function doubler(el){
    return el*2;
}
let newArr = oldArr.map(doubler);
console.log(newArr);
// Output- [2, 4, 6, 8, 10]
```

### filter()
***filter()*** filters elements in an array that means creates a new array with elements that are subset of old array. The resulting array only gets the elements that pass the test/condition of a callback function in filter().
```
let oldArr = [1, 2, 3, 4, 5]
function choose(el){
  return el%2===0;
}
let newArr = oldArr.filter(choose);
console.log(newArr);
// Output- [2, 4]
```

### reduce()
***reduce()*** method reduces array elements to a single value. It takes two values i.e, reduce(callback, initial value). Initial value is the first element of the array, if no other initial value is specified.
```
let oldArr = [2, 1, 4, 5, 6, 8, 10, 11]
function doubler(prev, next){
    return prev+next;
}
let newArr = oldArr.reduce(doubler);
console.log(newArr);
// Output- 47
```