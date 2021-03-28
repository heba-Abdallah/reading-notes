Headings 

<h1><h2><h3><h4><h5><h6>

<h1> used for main headings

<h2> used for subheadings, if there are further sections under the subheading then the <h3> element is used, and so on ....

  

paragraphs <p> to create a paragraph, surround the words that make up the paragraph with an opening <p> tag and closing </p> tag.

and by enclosing words in the tags <b> and </b> we can make characters appear bold, also by enclosing words in the tags <i> and </i> we can make characters appear italic.

    

line breaks by <br /> if you wanted to add a line break inside the middle of a paragraph you can use the line break tag and you can add horizontal rules between sections using the <hr /> tag.

the uses of the <strong> element indicate that its content has strong importance, by default browsers will show the contents of a <strong> element in bold, but the <em> element indicates emphasis that subtly changes the meaning of a sentence, by default browsers will show the contents of an <em> element in italic.

for quotations there are two elements commonly used: <blockquote> is used for longer quotes that take up an entire paragraph, the <q> element is used for shorter quotes that sit within a paragraph.

CSS

CSS allows you to create rules that control the way that each individual box is presented.

CSS works by associating rules with HTML elements. These rules govern how the content of specified elements should be displayed. A CSS rule contains two parts: a selector and a declaration

Selectors indicate which element the rule applies to. The same rule can apply to more than one element if you separate the element names with commas

Declarations indicate how the elements referred to in the selector should be styled. Declarations are split into two parts (a property and a value), and are separated by a colon.

  




CSS declarations sit inside curly brackets and each is made up of two parts: a property and a value, separated by a colon. You can specify several properties in one declaration, each separated by a semi-colon.

  

Properties indicate the aspects of the element you want to change. For example, color, font, width, height and border and the Values specify the settings you want to use for the chosen properties. For example, if you want to specify a color property then the value is the color you want the text in these elements to be.




Using External CSS

<link>

The <link> element can be used in an HTML document to tell the browser where to find the CSS file used to style the page. It is an empty element (meaning its self-closing tag), and it lives inside the <head> element. It should use three attributes:

  




Href: specifies the path to the CSS file (which is often placed in a folder called css or styles), type: specifies the type of document being linked to. The value should be text/css and rel: specifies the relationship between the HTML page and the file it is linked to. The value should be stylesheet when linking to a CSS file.

Using Internal CSS

<style>

You can also include CSS rules within an HTML page by placing them inside a <style> element which usually sits inside the <head> element of the page.

the <style> element should use the type attribute to indicate that the styles are specified in CSS. The value should be text/ css.

  




JavaScript

A script is a series of instructions that a computer can follow one-by-one. Each individual instruction or step is known as a statement. Statements should end with a semicolon.

  







You should write comments to explain what your code does. They help make your code easier to read and understand. This can help you and others who read your code.

  




A script will have to temporarily store the bits of information it needs to do its job. It can store this data in variables. When you write JavaScript, you have to tell the interpreter every individual step that you want it to perform. This sometimes involves more detail than you might expect.

Before you can use a variable, you need to announce that you want to use it. This involves creating the variable and giving it a name.

  

Once you have created a variable, you can tell it what information you would like it to store for you.

  




JavaScript distinguishes between numbers, strings, and true or false values known as Booleans.

The numeric data type handles numbers, the strings data type consists of letters and other characters and Boolean data types can have one of two values: true or false.




Decision Making

There are often several places in a script where decisions are made that determine which lines of code should be run next.


There are two components to a decision:

An expression is evaluated, which returns a value.
A conditional statement says what to do in a given situation.  


You can evaluate a situation by comparing one value in the script to what you expect it might be. The result will be a Boolean: true or false.


In any condition, there is usually one operator and two operands. The operands are placed on each side of the operator. They can be values or variables, you often see expressions enclosed in brackets.

  

The if statement evaluates a condition. If the condition evaluates to true, any statements in the subsequent code block are executed.

The if …. else statement checks a condition. If it resolves to true the first code block is executed, if the condition resolve to false the second code block is run instead.