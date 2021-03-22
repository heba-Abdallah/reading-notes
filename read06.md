When you are writing JavaScript, do not expect to write it perfectly the first time, programming is like problem solving.

The JavaScript interpreter uses the concept of three execution context,

1. Global context: code that is in the script, but not in a function. there is only one global context in any page.

2. Function context: code that is being run within a function. Each function has it's own function context.

3. Eval context(Not Shown): text is executed like code in an internal function called eval().

Each correspond to variable new execution context, they correspond to variable scope, the first two execution contexts correspond with the notion of scope,

1) Global scope: is a variable is declared outside a function, it can be used any where because it has global scope.

2)Function-level scope: when a variable is declared within a function, it can only be used within that function.

Each time a script enters a new execution context, there are two phases of activity,

* Prepare:

- The new scope is created.

- Variables, functions, and arguments are created.

- The value of the [this] keyword is determined.

* Execute:

- Now it can assign values to variables.

- Reference functions and run their code.

- Execute statement.