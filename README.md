=======
timed
=====

Simplifies high resolution timing for profiling

Usage exampe:

```javascript
t = require('timed');

//Start the timer
t.reset();

setTimeout(function() {
  //should be about 1000 ms
  console.log('Elapsed: ' + t.since() + ' ms');  

  t.reset();  //timer starts again now from 0
  setTimeout(function() {
    //This one should be about 1500 ms
    console.log('Elapsed: ' + t.since() + 'ms');
  }, 1500);
  

}, 1000);

```
