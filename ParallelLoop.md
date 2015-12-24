# Introduction #

Parallel looping constructs are important for high performance in numerical apps.
However Python has no parallel looping construct and due to GIL no real concurrency can be had. Thus I propose to add a parallel loop.

# Details #

Since unPython always aims to be compatible with Python syntax, the idea is to introduce a new iterator called "prange" similar to "range" and "xrange". However whenever the compiler sees prange, it will understand that the loop is parallel. On the interpreter we will just define prange=xrange thus having a serial implementation.

The parallel loop will describe a loop where each iteration is totally independant of other iterations and can be executed in any order. Internally, the loop will be converted into OpenMP loop. However note that if you invoke a method on an object or access an attribute, then the generated code may need to access the interpreter and thus cannot be compiled into a parallel loop.

The parallel loop functionality will be included by end of July 2008.