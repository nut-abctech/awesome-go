## Pointers

Pointers provide a way to share data across function boundaries. Having the ability to share and reference data with a pointer provides flexbility. It also helps our programs minimize the amount of memory they need and can add some extra performance.

## Notes

* Use pointers to share data.
* Values in Go are always pass by value.
* "Value of", what's in the box. "Address of" ( **&** ), where is the box.
* The (*) operator declares a pointer variable and the "Value that the pointer points to".

## 1.5 Garbage Collection

![figure1](GC_Algorithm.png)

## Links

### Pointer Mechanics

https://golang.org/doc/effective_go.html#pointers_vs_values

http://www.goinggo.net/2013/07/understanding-pointers-and-memory.html

http://www.goinggo.net/2014/12/using-pointers-in-go.html

### Stacks

[Contiguous Stack Proposal](https://docs.google.com/document/d/1wAaf1rYoM4S4gtnPh0zOlGzWtrZFQ5suE8qr2sD8uWQ/pub)

### Escpae Analysis and Inlining

[Go Escape Analysis Flaws](https://docs.google.com/document/d/1CxgUBPlx9iJzkz9JWkb6tIpTe5q32QDmz8l0BouG0Cw)

https://github.com/golang/go/wiki/CompilerOptimizations

### Garbage Collection

https://en.wikipedia.org/wiki/Tracing_garbage_collection

https://blog.golang.org/go15gc

[Rick Hudson GC Talk](https://www.youtube.com/watch?v=aiv1JOfMjm0&index=16&list=PL2ntRZ1ySWBf-_z-gHCOR2N156Nw930Hm)

### Single Static Assignment Optimizations

[GopherCon 2015: Ben Johnson - Static Code Analysis Using SSA](https://www.youtube.com/watch?v=D2-gaMvWfQY)

https://github.com/golang/go/blob/dev.ssa/src/cmd/compile/internal/ssa/compile.go#L83

https://godoc.org/golang.org/x/tools/go/ssa

## Code Review

[Pass by Value](example1/example1.go) ([Go Playground](https://play.golang.org/p/nNnsK6hWdP))

[Sharing data I](example2/example2.go) ([Go Playground](https://play.golang.org/p/FWmGnVUDoA))

[Sharing data II](example3/example3.go) ([Go Playground](http://play.golang.org/p/VYqb11RiWr))

[Stack vs Heap](example4/example4.go) ([Go Playground](https://play.golang.org/p/3qE0uUOnTv))

## Exercises

### Exercise 1

**Part A** Declare and initialize a variable of type int with the value of 20. Display the _address of_ and _value of_ the variable.

**Part B** Declare and initialize a pointer variable of type int that points to the last variable you just created. Display the _address of_ , _value of_ and the _value that the pointer points to_.

[Template](exercises/template1/template1.go) ([Go Playground](http://play.golang.org/p/asM7GXfJNk)) | 
[Answer](exercises/exercise1/exercise1.go) ([Go Playground](http://play.golang.org/p/pUtHSTN0Ef))

### Exercise 2

Declare a struct type and create a value of this type. Declare a function that can change the value of some field in this struct type. Display the value before and after the call to your function.

[Template](exercises/template2/template2.go) ([Go Playground](http://play.golang.org/p/b6-FNFOToO)) | 
[Answer](exercises/exercise2/exercise2.go) ([Go Playground](http://play.golang.org/p/oEtveMoO1s))
___
All material is licensed under the [Apache License Version 2.0, January 2004](http://www.apache.org/licenses/LICENSE-2.0).