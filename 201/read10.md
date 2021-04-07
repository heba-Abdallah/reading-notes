ORDER OF EXECUTION
To find the source of an error, it helps to know how scripts are processed. The order in which statements are executed can be complex; some tasks cannot complete until another statement or function has been run:
 
This script above creates a greeting message, then writes it to an alert box. In order to create that greeting, two functions are used: {greetUser ()} and {getName ()} .
You might think that the order of execution (the order in which statements are processed) would be as numbered: one through to four. However, it is a little more complicated. To complete step one, the interpreter needs the results of the functions in steps two and three (because the message contains values returned by those functions). The order of execution is more like this: 1, 2, 3, 2, 1, and 4.
1. The greeting variable gets its value from the {greetUser()} function. 
2. {greetUser()} creates the message by combining the string 'Hello ' with the result of {getName ()}. 
3. {getName ()} returns the name to {greetUser()}.
 2. {greetUser()} now knows the name, and combines it with the string. It then returns the message to the statement that called it in step 1.
 1. The value of the greeting is stored in memory. 
4. This greeting variable is written to an alert box.

The stack
The JavaScript interpreter one line of code at a time. When a statement needs data from another function, it stacks (or piles) the new function on top of the current task.
When a statement has to call some other code in order to do its job, the new task goes to the top of the pile of things to do.
Once the new task has been performed, the interpreter can go back to the task in hand, each time a new item is added to the stack, it creates a new execution context.
Variables defined in a function (or execution context) are only available in that function. If a function gets called a second time, the variables can have different values.
In the interpreter, each execution context has its own variables object. It holds the variables, functions, and parameters available within it. Each execution context can also access its parent's variables object.

ERROR OBJECTS
Error objects can help you find where your mistakes are and browsers have tools to help you read them.
HOW TO DEAL WITH ERRORS
1: DEBUG THE SCRIPT TO FIX ERRORS: if you come across an error while writing a script (or when someone reports a bug), you will need to debug the code, track down the source of the error, and fix it. You will find that the developer tools available in every major modern browser will help you with this task. 
2: HANDLE ERRORS GRACEFULLY: You can handle errors gracefully using try, catch, throw, and finally statements. Sometimes, an error may occur in the script for a reason beyond your control. For example, you might request data from a third party, and their server may not respond. In such cases, it is particularly important to write error-handling code.

LOGGING DATA TO THE CONSOLE
This example shows several uses of the {console .log ()} method. 
1. The first line is used to indicate the script is running. 
2. Next an event handler waits for the user leaving a text input, and logs the value that they entered into that form field.
When the user submits the form, four values are displayed: 
3. That the user clicked submit
 4. The value in the width input 
5. The value in the height input 
6. The value of the area variable 
They help check that you are getting the values you expect.
The {console. log ()} method can write several values to the console at the same time, each separated by a comma, as shown when displaying the height (5). You should always remove this kind of error handling code from your script before you use it on a live site
 

MORE CONSOLE METHODS
To differentiate between the types of messages you write to the console, you can use three different methods. They use various colors and icons to distinguish them.
1. {console.info ()} can be used for general information.
2. {console.warn ()} can be used for warnings.
3. {console.error ()} can be used to hold errors.
This technique is particularly helpful to show the nature of the information that you are writing to the screen. (In Firefox, make sure you have the logging option selected.)
GROUPING MESSAGES
1. If you want to write a set of related data to the console, you can use the console. {group ()} method to group the messages together. You can then expand and contract the results.
It has one parameter; the name that you want to use for the group of messages. You can then expand and collapse the contents by clicking next to the group's name as shown below.
2. When you have finished writing out the results for the group, to indicate the end of the group the {console.groupEnd ()} method is used.