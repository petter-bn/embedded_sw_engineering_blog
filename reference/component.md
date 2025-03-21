# Software Components

A component is a piece of source code[^2] with a specific purpose and an 
interface. All[^1] source code in your SW system should belong to a 
component.

The software components are the basic building blocks of a SW system. 

![Component](pictures/component01.svg)

## Benefits

If you design good 
software components you will have the following benefits:

* More efficient troubleshooting and maintenance
* Less costly to improve and add functions to your system
* Easier to verify

The separation of software into components is for the benefit of the humans working with it.
The compute executiong the code doesn't care. Thus, to define a software component you
need to understand the limits of your fellow humans cognitive abilities.

The software components should be possible to be seen as a black box, for anyone only using it's 
functionality. That is when using the component you only need to know the purpose and the interface of the component.
Not the implementation. This reduces the cognitive load[^3] required to design and code a software system. Components are the smallest elements in an embedded architecture. Read more about modularity, and why it is beneficial [here](modularity.html).

Also, when working with the component you don't need to know how the component is used. You only need to make sure
you fulfill the purpose and respect the interface.

## Component Examples

In an embedded system, typical purposes of a components are:

* Controlling a device
* Handling input
* Handling a [MMI](glossary.hmtl)
* Processing information

Or a component could provide services to other components.

For example:

* Logging
* Handling configuration parameters
* Scheduling
* Communication
* PID regulation
* Encryption

A [camera-equipped lawnmower robot](example/CELR/index.html) for example could have components where the purposes are:

* Drive motor control
* Cutting motor control
* Map handling
* Trajectory planning

## Properties of a good component

### Purpose

The purpose of a software component *must* be clear.

It the purpose is not clear the component will be hard to use and hard to maintain. If it is hard to describe the purpose of the component, or the purpose consists of several not-very-related parts, the component might lack [cohesion](glossary.hmtl#cohesion) or [integrity](glossary.hmtl#integrity) and thus not provide [modularity](glossary.html).

If you can not describe the purpose of a component in one or two sentences, this a sign that your component might not be well defined.

See also [component integrity in layer architectures](layer_architecture.html).


### Interface

The component [interface](interface.html) provides the way to communicate with the comp0onent. They are the *only* the component communicates with the surrounding system. 

There are many different types of interfaces. Most common:

* Function call interface
* Communication interface
* Shared memory interface

### Thread safety

Many or most embedded systems of today use several processor cores, or multithreaded operating systems or both. It is likely or at least very possible that during the [development lifecycle](glossary.html#development_life_cycle) of a component it will be deployed in a multithreaded system.

Thread safety can be achieved in many ways. (See also [concurrent embedded programming](concurrent_embedded_programming.html))
programming

The strategy for concurrency should be decided in the [architectural design](architecture.html).

### Robustness

TODO

## What to do

If you are writing a new SW product, make sure your components are well defined:

* Decide the purpose of the component
* Design the interface  [interface](interface.html)
* Design the level of thread safety
* Design robustness

##

------

[^1] There are some exceptions. Generated code might only exist as 
temporary build files. The architectural framework might or might not
be a SW component of its own. See "bucket". 

[^2] The source code is the text files written by a human, intended 
to be read by a machine (a compiler, preprocessor, code generator etc)

[^3] Cognitive load is a nice expression for the amount of brain power needed for a 
task. See [https://en.wikipedia.org/wiki/Cognitive_load]. When the cognitive load exceeds your limit
things start to get slower in a non-linear way.

[^4] Even if the caller does not explicitly provides data as parameters to the call, it provides
the call adress, which indicates what is expected to be done.



