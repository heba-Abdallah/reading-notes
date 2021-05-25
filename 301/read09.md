What is functional programming?

Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data

The first fundamental concept we learn when we want to understand functional programming is pure functions. But what does that really mean? What makes a function pure?

So how do we know if a function is pure or not? Here is a very strict definition of purity:

It returns the same result if given the same arguments (it is also referred as deterministic)
It does not cause any observable side effects
It returns the same result if given the same arguments

Imagine we want to implement a function that calculates the area of a circle. An impure function would receive radius as the parameter, and then calculate radius * radius * PI:

  




Now imagine some mathematicians argue that the PI value is actually 42and change the value of the global object.

Our impure function will now result in 10 * 10 * 42 = 4200. For the same parameter (radius = 10), we have a different result. Let's fix it!

    

Now we’ll always pass thePI value as a parameter to the function. So now we are just accessing parameters passed to the function. No external object.

For the parameters radius = 10& PI = 3.14, we will always have the same the result: 0
For the parameters radius = 10& PI = 42, we will always have the same the result: 4200
Reading Files

If our function reads external files, it’s not a pure function — the file’s contents can change.

  

Random number generation

Any function that relies on a random number generator cannot be pure.




  

It does not cause any observable side effects

Examples of observable side effects include modifying a global object or a parameter passed by reference.

Now we want to implement a function to receive an integer value and return the value increased by 1.

  