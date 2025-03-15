
# Software Interfaces

TODO

### Function call interface

Let us start with the most common example: A function call interface provided by a component. Function call interfaces are 
used between components within one executable. (See also [remote procedure calls](rpc.html))

This kind of interface is supported by all common or less common languages for embedded SW
engineering: C, C++, Java, Rust.

In this interface the caller is outside the component, the callee is inside the component and 
the call is the interface. This kind of interface is so natural for most programmers that the
specifics of it is not really considered. So lets write them down:

* Function calls take place in one execution thread, the caller waits until the callee returns.
* It is bidirectional the caller provides data [^4] and the callee can return data [^5].
* Function call interfaces are asymmetric. There is a caller and a called.

### Communication interfaces

TODO

### Shared memory interfaces

TODO



