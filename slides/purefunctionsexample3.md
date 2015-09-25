```
// impure
var minimum = 21;

var checkAge = function(age) {
  return age >= minimum;
};

// pure
var checkAge = function(age) {
  var minimum = 21;
  return age >= minimum;
};
```

Note:
In the impure portion, checkAge depends on the mutable variable minimum to determine the result. In other words, it depends on system state which is disappointing because it increases the cognitive load by introducing an external environment.

It might not seem like a lot in this example, but this reliance upon state is one of the largest contributors to system complexity