# Software Components

A component is a piece of source code[^2] with a specific purpose and an 
interface. All[^1] source code in your SW system should belong to a 
component.

The software components are the basic building blocks of a SW system. If you design good 
software components you will have the following benefits:

* More efficient troubleshooting and maintenance
* Less costly to improve and add functions to your system
* Easier to verify

The separation of software into components is for the benefit of the humans working with it.
The compute executiong the code doesn't care. Thus, to define a software component you
need to understand the limits of your fellow humans cognitive abilities.

The software components should be possible to be seen as a black box, for anyone only using it's 
functionality. That is when using the component you only need to know the purpose and the interface of the component.
Not the implementation. This reduces the cognitive load[^3] required to design and code a software system.

Also, when working with the component you don't need to know how the component is used. You only need to make sure
you fulfill the purpose and respect the interface.

The purpose 

## Purpose

The purpose of a software component *must* be clear. 

[^1] There are some exceptions. Generated code might only exist as 
temporary build files. The architectural framework might or might not
be a SW component of its own. See "bucket". 

[^2] The source code is the text files written by a human, intended 
to be read by a machine (a compiler, preprocessor, code generator etc)

[^3] Cognitive load is a nice expression for the amount of brain power needed for a 
task. See [https://en.wikipedia.org/wiki/Cognitive_load]. When the cognitive load exceeds your limit
things start to get slower in a non-linear way.


