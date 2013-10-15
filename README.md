infiniteLoop
============

infinite loop in nodejs

## easy to use:

```javascript
var InfiniteLoop = require('infinite-loop');
  
var il = new InfiniteLoop();
  
//task you want to run infinitely
function addOne(n) {
  n ++;
  console.log(n);
}

//use add to add a task
//first argument should be a function, the rest should be the functions' argument
il.add(addOne, 26);

//use run to invoke the task
il.run();

//the api is chainable
il.add(addOne, 26).run();
```