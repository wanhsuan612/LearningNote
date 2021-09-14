## Sum of values in an object array
----------------------
Sum the x value: 
```
let initialValue = 0
let sum = [{x: 1}, {x: 2}, {x: 3}].reduce( (previousValue, currentValue) => previousValue + currentValue.x, initialValue)

console.log(sum) // logs 6
```

ref: [Array.propotype.reduce()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce)