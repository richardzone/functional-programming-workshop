### Compose Functions

```
var compose = function(f,g) {
  return function(x) {
    return f(g(x));
  };
};
```