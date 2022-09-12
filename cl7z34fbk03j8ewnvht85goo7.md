## Arrow function in Javascript

**Arrow Functions** are much cleaner and shorter way compared to function expressions.
They are most likely to be used when you want to create an *anonymouus function*.

### Let's see the difference -

**Function Expression -**
```
let x = function(x, y){
    return x * y;
}
``` 
**Arrow Function -**
```
let x = (x, y) => x * y;
```

*Noticed?* our variable is remaining the same, function keyword is omitted with function symbol and the code remains the same for whatever task you are creating it for. Second one is **more clear and short**, right? To call it, use **x();**

*There are certain ways to define arrow function in different situations*

### Function with no arguments
When function doesnot accept argument, then you can use empty parenthesis.
```
let x = () => //code;
```

### Function with arguments
Here you can use arguments inside parenthesis. Works same as regular function but in shorter way.
```
let showText = (text) => console.log(text);
```

### Function as expression
You can easily and effortlessly use arrow function as expression. Here we are using with ternary operators.
```
let num = 0;
let message = (num < 10) ?
    () => console.log('Correct Answer') :
    () => console.log('Try Again');
message();  // output: Correct Answer
```

### Multiline function
In this case, use only curly braces to wrap everything.
```
let result = (a, b) => {
    let sum = a+b;
    return sum;
}
```

*Dont forget to hit the heart, if you found this article, informative!*