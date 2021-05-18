





Forms

HTML form elements work a little bit differently from other DOM elements in React, because form elements naturally keep some internal state. For example, this form in plain HTML accepts a single name:

  

This form has the default HTML form behavior of browsing to a

new page when the user submits the form. If you want this behavior in React, it just works. But in most cases, it’s convenient to have a JavaScript function that handles the submission of the form and has access to the data that the user entered into the form. The standard way to achieve this is with a technique called “controlled components”.

Controlled Components

In HTML, form elements such as <input>, <textarea>, and <select> typically maintain their own state and update it based on user input. In React, mutable state is typically kept in the state property of components, and only updated with setState().

We can combine the two by making the React state be the “single source of truth”. Then the React component that renders a form also controls what happens in that form on subsequent user input. An input form element whose value is controlled by React in this way is called a “controlled component”.

For example, if we want to make the previous example log the name when it is submitted, we can write the form as a controlled component:

  

Try it on CodePen

Since the value attribute is set on our form element, the

displayed value will always be this.state.value, making the React state the source of truth. Since handleChange runs on every keystroke to update the React state, the displayed value will update as the user types.

With a controlled component, the input’s value is always driven by the React state. While this means you have to type a bit more code, you can now pass the value to other UI elements too, or reset it from other event handlers.

The textarea Tag

In HTML, a <textarea> element defines its text by its children:

  

In React, a <textarea> uses a value attribute instead. This way, a form using a <textarea> can be written very similarly to a form that uses a single-line input:

  

Notice that this.state.value is initialized in the constructor, so that the text area starts off with some text in it.




JavaScript — The Conditional (Ternary) Operator Explained




Starting With the Basics — The if statement

Using a conditional, like an if statement, allows us to specify that a certain block of code should be executed if a certain condition is met.

Consider the following example:

We have a person object that consists of a name, age, and driver property.

  

We want to test if the age of our person is greater than or equal to 16. If this is true, they’re old enough to drive and driver should say 'Yes'. If this is not true, driver should be set to 'No'.

We could use an if statement to accomplish this:

  

But what if I told you we could do the same exact thing in just one line of code? Well, here it is:

  

This shorter code yields us the same result of person.driver = 'Yes';

The Conditional (Ternary) Operator

First, we’ll take a look at the syntax of a typical if statement:

  

Now, the ternary operator:

  

Here’s what you need to know:

The conditionis what you’re actually testing. The result of your condition should be true or false or at least coerce to either boolean value.
A ?separates our conditional from our true Anything between the ? and the : is what is executed if the condition evaluates to true.
Finally a : If your conditionevaluates to false, any code after the colon is executed.

  