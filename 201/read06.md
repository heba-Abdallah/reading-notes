Object
Objects group together a set of variables and functions to create a model of a something you would recognize from the real world. In an object, variables and functions take on new names.
If a variable is part of an object, it is called a property. Properties tell us about the object, such as the name of a hotel or the number of rooms it has. Each individual hotel might have a different name and a different number of rooms and if a function is part of an object, it is called a method. Methods represent tasks that are associated with the object. For example, you can check how many rooms are available by subtracting the number of booked rooms from the total number of rooms.
Creating an Object
Literal notation is the easiest and most popular way to create objects.
The object is the curly braces and their contents, the object is stored in a variable called hotel so you would refer to it as the {hotel} object.
Separate each key from its value using a colon, also each property and method with a comma.
   
In the {checkAvailability()} method, the [this] keyword is used to indicate that it is using the [rooms] and [booked] properties of [this] object.
You access the properties or methods of an object using dot notation, you can also access properties using square brackets
To access a property or method of an object you use the name of the object, followed by a period, then the name of the property or method you want to access.
The period is known as the member operator. The property or method on its right is a member of the object on its left.
You can also access the properties of an object (but not its methods) using square bracket syntax, this time the object name is followed by square brackets and property name is inside them.
 
The Document Object Model DOM
The document object model specifies how w browsers should create a model of an HTML page and how JavaScript can access and update the contents of a web page while it is in the browser window.
The DOM is neither part of HTML, nor part of JavaScript; it is a separate set of rules. It is implemented by all major browser makers, and covers two primary areas:
1-MAKING a MODEL OF THE HTM L PAGE
 When the browser loads a web page, it creates a model of the page in memory. The DOM specifies the way in which the browser should structure this model using a DOM tree
ACCESSING AND CHANGING THE HTML PAGE
 The DOM also defines methods and properties to access and update each object in this model, which in turn updates what the user sees in the browser
Methods that find elements in the DOM tree are called DOM queries. When you need to work with an element more than once, you should use a variable to store the result of this query.
When a script selects an element to access or update, the interpreter must find the element(s) in the DOM tree.
   
When people talk about storing elements in variables, they are really storing the location of the element within the DOM tree in a variable. The properties and methods of that element node work on the variable.
If your script needs to use the same element more than once, you can store the location of the element in a variable. This saves the browser looking through the DOM tree to find the same element again it is known as caching the selection
   
{getElementById()} and {querySelector()} can both search an entire document and return individual elements.
getElementById() is the quickest and most efficient way to access an element because no two elements can share the same value for their id attribute.
Document refers to the document object. You always have to access individual elements via the document object.
   
The getElementById() method indicates that you want to find an element based upon the value of its id attribute
querySelector() is a more recent addition to the DOM, so it is not supported in order browsers. But it is very flexible because its parameters is a CSS selector, which means it can used to accurately target many more elements.
{getElementById ()} allows you to select a single element node by specifying the value of its id attribute. This method has one parameter: the value of the id attribute on the element you want to select. This value is placed inside quote marks because it is a string. The quotes can be single or double quotes, but they must match.
There are two ways to select an element from a NodeList:
The item() method and array syntax. Both require the index number of the element you want
The item() Method
NodeLists have a method called item() which will return an individual node from the NodeList. You specify the index number of the element you want as a parameter of the method (inside the parentheses)
Executing code when there are no elements to work with wastes resources. So programmers often check that there is at least one item in the NodeList befor running any code. To do this use the length property of the NodeList – it tells you how many items the NodeList contains.
Array syntax is preferred over the item() method because it is faster. Before selecting a node from a NodeList, chech that it contain nodes, if you repeatedly use the NodeList, store it in a variable.
You can access individual nodes using a square bracket syntax similar to that used to access individual items from an array, you specify the index number of the element you want inside square bracket that follow the NodeList.
The {getElementsByClassName()} method allows you to select elements whose class attribute contains a specific value. The method has one parameter: the class name which is given in quotes within the parentheses after the method name, because several elements can have the same value for their cl ass attribute, this method always returns a Nodelist.
The {getElementsByTagName ()} method allows you to select elements using their tag name. The element name is specified as a parameter, so it is placed inside the parentheses and is contained by quote marks.
{querySelector()} returns the first element node that matches the CSS-style selector. querySelectorA11 () returns a Nodelist of all of the matches. Both methods take a CSS selector as their only parameter. The CSS selector syntax offers more flexibility and accuracy when selecting an element than just specifying a class name or a tag name, and should also be familiar to front-end web developers who are used to targeting elements using CSS.

