



The JavaScript Call Stack - What It Is and Why It's Necessary

The JavaScript engine (which is found in a hosting environment like the browser), is a single-threaded interpreter comprising of a heap and a single call stack. The browser provides web APIs like the DOM, AJAX, and Timers.

The call stack is primarily used for function invocation (call). Since the call stack is single, function(s) execution, is done, one at a time, from top to bottom. It means the call stack is synchronous.

The understanding of the call stack is vital to Asynchronous programming (which we will look at in a later article).

In Asynchronous JavaScript, we have a callback function, an event loop, and a task queue. The callback function is acted upon by the call stack during execution after the call back function has been pushed to the stack by the event loop.

At the most basic level, a call stack is a data structure that uses the Last In, First Out (LIFO) principle to temporarily store and manage function invocation (call).

Let’s break down our definition:

LIFO: When we say that the call stack, operates by the data structure principle of Last In, First Out, it means that the last function that gets pushed into the stack is the first to be pop out, when the function returns.

Let us take a look at a code sample to demonstrate LIFO by printing a stack trace error to the console.

  

When the code is run, we get an error. A stack is printed showing how the functions are stack on top each other. Take a look at the diagram.

  

You will notice that the arrangement of the functions as a stack begins with the firstFunction() (which is the last function that got into the stack, and is popped out to throw the error), followed by the secondFunction(), and then the thirdFunction() (which is the first function that gets pushed into the stack when the code is executed).

Temporarily store: When a function is invoked (called), the function, its parameters, and variables are pushed into the call stack to form a stack frame. This stack frame is a memory location in the stack. The memory is cleared when the function returns as it is pop out of the stack.

  

Manage function invocation (call): The call stack maintains a record of the position of each stack frame. It knows the next function to be executed (and will remove it after execution). This is what makes code execution in JavaScript synchronous.

Think of yourself standing on a queue, in a grocery store cash point. You can only be attended to after the person in front of you have been attended to. That’s synchronous.

This is what we mean by “manage function invocation”.

How does the call stack handle function calls?

We will answer this question by looking at a sample code of a function that calls another function. Here is the example code:

    




This is what happens when the code is run:

When secondFunction()gets executed, an empty stack frame is created. It is the main (anonymous) entry point of the program.
2. secondFunction()then calls firstFunction()which is pushed into the stack.
3. firstFunction() returns and prints “Hello from firstFunction” to the console.
4. firstFunction() is pop off the stack.
5. The execution order then move to secondFunction().
6. secondFunction() returns and print “The end from secondFunction” to the console.
7. secondFunction() is pop off the stack, clearing the memory.







JavaScript error messages && debugging

Most of your time as a developer is spent reading code followed by debugging that same code, most likely to be able to read it or solve an “unexpected feature” (which, joking aside, is more correctly known as a “bug”).

  

This is a sample of an error, the green is the overall error message, the light blue is to note if the error was properly handled, the brownish (dark yellow) is the type of error and the red is the call stack

The code that was run was the following (this is code for example purposes):




(function testing(){
  var obj = {
    add
  }  function add(a, b) {
    var result = a + b
    return result.split('')
  }  var stringResult = obj.add("1", "2")
  var result = obj.add(1, 2)
})()




I will come back to this code in the call stack section, let us first see what the types of error can be.

Types of error messages

The first thing that indicates you that something is wrong with your code is the (in)famous error message that the one we saw just moments ago, it usually appears on your console (being developer tools of the browser, terminal or whatever else you are using).

For those already used to programming, reading an error message is like second nature, for everybody else, is something you learn either you like it or not so might as well talk a bit about each of them.

Reference errors

This is as simple as when you try to use a variable that is not yet declared you get this type os errors.

console.log(foo) // Uncaught ReferenceError: foo is not defined

This is also a common thing when using const and let, they are hoisted like var and function but there is a time between the hoisting and being declared so when you try to access them a reference error occurs, the fact that this happens to let and const is called Temporal Dead Zone (TDZ).

foo = 'Hello' // Uncaught ReferenceError: foo is not defined
let foo

Whatever you are using (var, let or const) the fix is as simple has declaring the variable before any declaration is made.

let foo;
foo = 'Hello'

Syntax errors

I know it’s in the name of the errors, but like it says itself, this occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.

JSON.parse( {'foo': 'bar'} ) // Uncaught SyntaxError: Unexpected token o in JSON at position 1

This can be solved by just fixing the syntax, in this case the object should be a JSON.

JSON.parse('{"foo":"bar"}')

Some syntax errors like sending a trailing comma when calling a function are handled without error by most recent browsers, but older ones you have to be careful.

Range errors

Try to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.

var foo= []
foo.length = foo.length -1 // Uncaught RangeError: Invalid array length

An array for instance cannot have a negative length, why would you mess with the array length? Some people use it to set an array to empty, something of the likes of:

var foo = [0, 0]
foo.length = foo.length - 2 // (or foo.length - foo.length)
foo // would log [] instead of [0, 0]

I prefer not to mutate my variables whenever possible (making them constants and not variables) but this is a method that is available and now you know it.

Type errors

Like the name indicates, this types of errors show up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.

var foo = {}
foo.bar // undefined
foo.bar.baz // Uncaught TypeError: Cannot read property 'baz' of undefined

This is probably the most frequent error in JS, trying to access a property/method thinking that bar is of the type object when in reality, since it hasn’t been declared yet, it’s undefined which doesn’t have any baz available.

The fix is simple, just make sure that bar exists before trying to access it, either by creating bar or by checking for undefined.

var foo = { bar: {} }
foo.bar.baz // undefined but you avoid the error

or

var foo = {}
if (typeof foo.bar !== 'undefined') {
  foo.bar.baz // this will never be executed while bar does not exist
}

There are also warnings, for instance telling you about a deprecated method, which can be found more frequently in firefox developer tools.