The source code is the fundament of all 
SW engineering.* So why don't I start with writing about source code
instead of components? This is a good question. However, so many good
coding practices are best understood in the context of components. Doing
good unit testing, defensive programming or concurrent programming is
harder (and maybe futile) if you don't have a component structure.


You could argue that the binary executable code is the fundament of all SW
engineering, as this is the code that is actually executed and provides 
the value for the user. But in practice the binary is predictably and
repeatably generated from the source code. And the binary is seldom
something a SW engineer directly works with. In fact, if you need to
work manually with the binary, or it is not directly and predictably
derived from the source code, then your project has problems.


```mermaid
  info
```