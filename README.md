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


#### THE STACK
Static storage<br>
Object size is known fixed<br>
Ordered<br>
STORES: <br>
Primitive types - number, string, boolean, undefined, null, variables.<br>

#### THE HEAP
Dynamic memory allocation at runtime <br>
UnOrdered<br>
STORES:<br>
Reference types (instances) - Object literals, Arrays, Functions, etc <br>
So it tells JavaScript where to find objects and functions.<br>
        
        const cat = {                            CAT `STORED IN HEAP`
            name: "Jupiter"                      A REFERENCE IS STORED IN STACK AND THE NAME PROPERTY IS `STORED IN STACK`
}

###### ***NOTE*** 
---> VARIABLE NAMES take up memory in the STACK<BR>
---> FUNCITON DEFINITION and OBJECTS have memory in the HEAP.<BR>

#### The Memory Life Cycle
3 parts:<br>

1. Memory Allocation (Values declared and stored then allocated) <br>
           * When function executed memory allocated <br>
           * Function frame added to stack <br> 
           * New objects stored in heap <br>
           * Stack stores reference to new object <br>
           * Function completed then removed from stack <br>
           * Memory is delocated and can be reused. <br>
           * STACK no longer have reference to Object stored in HEAP <br>
           * Objects are passed in a function by reference which can be modified in a function thus modifiying original object <br>
3. Memory in Use (Values read or rewritten) <br>
4. Releasing Memory (Values no longer used are removed from memory). <br>


           let aaliyah = {                                    //object created
                   name: "Aaliyah"                                //Saved into HEAP
           }                                                  //Reference in STACK
                        
           function nameObjectModification(obj, name) {               
                   obj.name = name;                                //Object created and used still references the
                   return obj;                                     //original object aaliyah 
           }
                        
           let sarah = nameObjectModification(aaliyah, "Sarah");      //1st create Sarah object from above fnc
                                                                                   //Referenced to aaliyah object and saved to new variable sarah
                                                                                   // Both variables reference same object                  
           console.log(aaliyah); // { name: 'Sarah' }
           console.log(sarah); // { name: 'Sarah' }

#### Memory in Use

* Variable reassignment <br>
* Using variables <br>
* Passing arguments to functions <br>

#### Garbage Collection

- The process of clearing memory<br>
- JavaScript uses to algorithms for Garbage Collection<br>

                 * REFERENCE COUNTING
                          Eg. Create an object - reference count = 1
                              Create another varaible point to same object - reference count = 2
                              A function uses the object - reference count = 3
                                  Function finished then elements are garbage collected reference = 0
                                          Memory block also = 0 and now utilize it for other storage
                            
                 * MEMORY SWEEPING
                          - Periodically run starting at the root (global object)
                          - Sweeps by marking elements
                          - Unmarked elements are garbage collected




  
