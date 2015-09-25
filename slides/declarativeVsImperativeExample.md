### One more example

Imperative style:
```
var sumOfSquares = function(list) {
    var result = 0;
    for (var i = 0; i < list.length; i++) {
        result += square(list[i]);
    }
    return result;
};

console.log(sumOfSquares([2, 3, 5]));
```

Declarative style:
```
var sumOfSquares = pipe(map(square), reduce(add, 0));

console.log(sumOfSquares([2, 3, 5]));
```
