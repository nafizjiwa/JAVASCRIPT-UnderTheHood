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
|Data structures for memory| The Heap|
|| The Call Stack |

The Event Loop can be summarized as: when code is executed, it is handled by the heap and call stack, which interact with Node and Web APIs. <br> 
Those APIs enable concurrency and pass asynchronous messages back to the stack via an event queue. <br>
The event queue’s interaction with the call stack is managed by an event loop.<br>

##### THE STACK
Static storage<br>
Object size is known fixed<br>
Ordered<br>
Stores Primitive values <br>

##### THE HEAP
Dynamic memory allocation at runtime <br>
UnOrdered<br>
Stores Reference (instances) values.<br>
So it tells JavaScript where to find objects and functions.<br>
        
        const cat = {                            CAT `STORED IN HEAP`
            name: "Jupiter"                      A REFERENCE IS STORED IN STACK AND THE NAME PROPERTY IS `STORED IN STACK`
}

Primitive types - number, string, boolean, undefined, null.<br>
Reference types - Object literals, Arrays, Functions, etc <br>

##### The Memory Life Cycle
3 parts:<br>
1. Memory Allocation (Values declared and stored)
2. Memory in Use (Values read or rewritten)
3. Releasing Memory (Values no longer used are removed from memory)

