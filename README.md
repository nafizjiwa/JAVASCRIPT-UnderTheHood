# JAVASCRIPT-UnderTheHood

|Javascript| Description |
|-----|-----|
|Javascript| is a single-threaded language |
| Means |can’t executed 2 statements simultaneously|
| Must run one code then run another code| Results: Blocking code |
|Currying||
|Hoisting| By allocating memory to save the names of declared variables and functions (hoisted 1st) |
|| and then hoisting/'raising' them to the top of their current scope prior to execution |
|Hoisting order| function delcaration -> function expression -> variables |
|Concurrency Model||
|Event Loop| helps run non blocking code|
| Result:| event loop helps emulate concurrency in javascript to manage code execution |
| Event Loop Parts: | Memory Heap, Call Stack, Event Queue, Event Loop and Node or Web APIs|
|Their Funciton: | Maintain the order of code execution when we run asynchronous functions |


|Memory Management ||
|-----|-----|
|Memory Heap| Unordered storage of objects and variables|
|Call Stack | tracks the currently running function|
|Event Queue| holds messages of functions waiting processing and added back to stack|
|Event Loop|Adds messages from the Event Queue to the Call Stack|
|Node or Web APIs||

The Event Loop can be summarized as: when code is executed, it is handled by the heap and call stack, which interact with Node and Web APIs. Those APIs enable concurrency and pass asynchronous messages back to the stack via an event queue. The event queue’s interaction with the call stack is managed by an event loop.
