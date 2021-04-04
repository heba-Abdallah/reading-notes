Table

A table represents information in a grid format.

Basic Table Structure:

The {<table>} element is used to create a table. The contents of the table are written out row by row.

You indicate the start of each row using the opening {<tr>} tag, the tr stands for table row), it’s followed by one or more {<td>} elements (one for each cell in that row). At the end of the row use a closing {</tr>} tag.

Each cell of a table is represented using a {<td>} element. (The td stands for table data.), at the end of each cell you use a closing {</td>}.

The {<th>} element is used just like the {<td>} element but its purpose is to represent the heading for either a column or a row. (The th stands for table heading.) Even if a cell has no content, you should still use a {<td>} or {<th>} element to represent the presence of an empty cell otherwise the table will not render correctly, using {<th>} elements for headings helps people who use screen readers, improves the ability for search engines to index your pages, and also enables you to control the appearance of tables better when you start to use CSS.




Object

Creating an Object: Constructor Notation

The new keyword and the object constructor create a blank object, you can then add properties and methods to the object.

First, you create a new object using a combination of the new keyword and the object () constructor function. (This function is part of the JavaScript language and is used to create objects.)

Next, having create the blank object, you can add properties and methods to it using dot notation. Each statement that adds a property or method should end with a semicolon.

  

To update the value of properties, use dot notation or square brackets. They work on objects created using literal or constructor notation, to delete a property use the delete keyword.

Sometimes you will want several object to represent similar things. Object constructors can use a function as template for creating objects.

First, create the template with the object’s properties and methods.

A function called hotel will be used as a template for creating new objects that represent hotels. Like all functions, it contains statements. In this case, they add properties or methods to the object.

The function has three parameters. Each one sets the value of a property in the object. The methods will be the same for each object created using this function.

  

The this keyword is used instead of the object name to indicate that the property or method belongs to the object that this function creates, each statement that creates a new property or method for this object ends in a semicolon (not a comma, which is used in the literal syntax)

The name of a constructor function usually begins with a capital letter (unlike other functions, which tend to begin with a lowercase character), the uppercase letter is supposed to help remind developers to use the new keyword when they create an object using that function.

You create instances of the object using the constructor function. The new keyword followed by a cell to the function create a new object, the properties of each object are given as arguments to the function.

Here, two objects are used to represent two hotels, so each object needs a different name. When the new keyword calls the constructor function it create a new object, each time it is called, the arguments are different because they are the value for the properties of each hotel. Both objects automatically get the same method defined in the constructor function.  

  

The first object is called quayHotel. Its name is “Quay” and it has 40 rooms, 25 of which are books

The second object is called parkHotel. Its name is “park” and it has 120 rooms, 77 of which are booked.

Arrays are actually a special type of object. They hold a related set of key/value pairs (like all objects), bit the key value is its index number.

You can combine arrays and objects to create complex data structures:

Arrays can store a series of objects (and remember their order).

Objects can also hold arrays (as values of their properties).

Browsers come with a set of built-in objects that represent things like the browser window and the current web page shown in that window. These built-in objects act like a toolkit for creating interactive web pages.

Three groups of built-in objects

Using built-in objects: the three sets of built-in objects each offer a different range of tools that help write scripts for web pages.

Browser object model: creates a model of the browser tab or window, the topmost object is the window object, which represents current browser window or tab. Its child objects represent other browser features.

Document object model (DOM): creates a model of the current web page, the topmost object is the document object, which represents the page as a whole. Its child objects represent other items on the page.