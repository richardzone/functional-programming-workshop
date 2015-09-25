### Object-oriented approach

```js
var getIncompleteTaskSummariesForMember_objectOriented = function(memberName) {
   return fetchData()
       .then(function(data) {
           var taskList = new TaskList(data.tasks);
           taskList.chooseByMember(memberName);
           taskList.chooseByCompletion(false);
           var newTaskList = taskList.getSummaries();
           newTaskList.sort(new TaskListSorter("dueDate"));
           return newTaskList.tasks;
       });
};
```