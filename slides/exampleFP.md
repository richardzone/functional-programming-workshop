### Functional approach

```
var getIncompleteTaskSummariesForMemberFunctional = function(memberName) {
    return fetchData()
        .then(get('tasks'))
        .then(filter(propEq('member', memberName)))
        .then(reject(propEq('complete', true)))
        .then(map(pick(['id', 'dueDate', 'title', 'priority'])))
        .then(sortBy(get('dueDate')));
};
```