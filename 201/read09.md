Forms
How Forms Work
A user fills in a form and then presses a button to submit the information to the server. The name of each form control is sent to the server along with the value the user enters or selects. The server processes the information using a programming language such as PHP, C#, VB.net, or Java. It may also store the information in a database. The server creates a new page to send back to the browser based on the information received.
A form may have several form controls, each gathering different information. The server needs to know which piece of inputted data corresponds with which form element.
Form Structure
{<form>} controls live inside an element. This element should always carry the action attribute and will usually have a method and id attribute too.
Action: every element requires an action attribute. Its value is the URL for the page on the server that will receive the information in the form when it is submitted.
Method: Forms can be sent using one of two methods: get or post.
With the get method, the values from the form are added to the end of the URL specified in the action attribute. The get method is ideal for: 
●Short forms (such as search boxes) 
●When you are just retrieving data from the web server (not sending information that should be added to or deleted from a database)

With the post method the values are sent in what are known as HTTP headers. As a rule of thumb you should use the post method if your form: 
● allows users to upload a file
● is very long 
● contains sensitive data (e.g. passwords) 
● adds information to, or deletes information from, a database
If the method attribute is not used, the form data will be sent using the get method.

Text Input
The {<input>} element is used to create several different form controls. The value of the type attribute determines what kind of input they will be creating.
{type="text"}: When the type attribute has a value of text, it creates a single-line text input.
Name: When users enter information into a form, the server needs to know which form control each piece of data was entered into. (For example, in a login form, the server needs to know what has been entered as the username and what has been given as the password.) Therefore, each form control requires a name attribute. The value of this attribute identifies the form control and is sent along with the information they enter to the server.
Size: The size attribute should not be used on new forms. It was used in older forms to indicate the width of the text input (measured by the number of characters that would be seen)
Maxlength: You can use the maxlength attribute to limit the number of characters a user may enter into the text field. Its value is the number of characters they may enter. For example, if you were asking for a year, the maxlength attribute could have a value of 4.
Password Input
{<input>}
{type="password"}: When the type attribute has a value of password it creates a text box that acts just like a single-line text input, except the characters are blocked out. They are hidden in this way so that if someone is looking over the user's shoulder, they cannot see sensitive data such as passwords.
Name: The name attribute indicates the name of the password input, which is sent to the server with the password the user enters.
Size, maxlength: It can also carry the size and maxlength attributes like the single-line text input.

Text Area
The {<textarea>}: element is used to create a multi-line text input. Unlike other input elements this is not an empty element. It should therefore have an opening and a closing tag.
Any text that appears between the opening {<textarea>} and closing {</textarea>} tags will appear in the text box when the page loads, If the user does not delete any text between these tags, this message will get sent to the server along with whatever the user has typed.
 
Lists, Tables and Forms
The list-style-type property allows you to control the shape or style of a bullet point (also known as a marker), It can be used on rules that apply to the {<ol>}, and {<li>} elements
Unordered Lists: For an unordered list you can use the following values: none, disc, circle, square.
Ordered Lists: For an ordered (numbered) list you can use the following values: 
•	Decimal:   (1 2 3)
•	Decimal-leading-zero: (01 02 03)
•	Lower-alpha: (a b c) 
•	Upper-alpha: (A B C)
•	Lower-roman: (i. ii. Iii.)
•	Upper-roman: (I II III)
You can specify an image to act as a bullet point using the list-style-image property, the value starts with the letters url and is followed by a pair of parentheses. Inside the parentheses, the path to the image is given inside double quotes. This property can be used on rules that apply to the {<ul>} and {<li>} elements.


HOW EVENTS TRIGGER JAVASCRIPT CODE
When the user interacts with the HTML on a web page, there are three steps involved in getting it to trigger some JavaScript code. Together these steps are known as event handling.
1.	Select the element node(s) you want the script to respond to. For example, if you want to trigger a function when a user clicks on a specific link, you need to get the DOM node for that link element.
2.	Indicate which event on the selected node(s) will trigger the response. Programmers call this binding an event to a DOM node. 
3.	State the code you want to run when the event occurs. When the event occurs, on a specified element, it will trigger a function. This may be a named or an anonymous function.
Event flow
Html elements nest inside other element, if you hover or click on a link, you will also be hovering or clicking on its parent elements.
Imagine a list item contains a link. When you hover over the link or click on it, JavaScript can trigger events on the {<a>} element, and also any elements the {<a>} element sites inside.
Event handlers/listeners can be bound to the containing {<li>}, {<ul>}, {<body>}, and {<html>} elements, plus the document object, and the window object. The order in which the events fire as known as event flow, and events flow in two directions.
Event bubbling: the event starts at the most specific node and flows outwards to the least specific one. This is the default type of event flow with very wide browser support.
Event capturing: the event starts at the least specific node and flows inwards to the most specific one. This is not supported in internet Explorer 8 and earlier.
Why flow matters
The flow events only really matters when your code has events handlers on an element and one of its ancestor or descendant elements.