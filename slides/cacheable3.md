You can transform some impure functions into pure ones by **delaying evaluation**:

```
var pureHttpCall = memoize(function(url, params){
  return function() { return $.getJSON(url, params); }
});
```