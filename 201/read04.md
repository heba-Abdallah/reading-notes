Writing Links
Links are created using the {<a>} element. Users can click on anything between the opening tag {>a>} and the closing tag {</a>}. You specify which page you want to link to using the [href] attribute.
 
The text between the opening <a> tag and closing </a> tag is known as link text. Where possible, your link text should explain where visitors will be taken if they click on it

When you are linking to other pages within the same site, you do not need to specify the domain name in the URL. You can use a shorthand known as a relative URL.

It’s a good idea to organize your code by placing the pages for each different section of the site into a new folder. Folders on a website are sometimes referred to as directories.

 

Every page and every image on a website has a URL (or Uniform Resource Locator). The URL is made up of the domain name followed by the path to that page or image.
Relative URLs can be used when linking to pages within your own website. They provide a shorthand way of telling the browser where to find your files, when you are linking to a page on your own website, you do not need to specify the domain name. You can use relative URLs which are a shorthand way to tell the browser where a page is in relation to the current page.
If your site is organized into separate folders (or directories), you need to tell the browser how to get from the page it is currently on to the page that you are linking to. 
To create a link that starts up the user's email program and addresses an email to a specified email address, you use the {<a>} element. However, this time the value of the {href} attribute starts with {mailto :} and is followed by the email address you want the email to be sent to.
If you want a link to open in a new window, you can use the {target} attribute on the opening {<a>} tag. The value of this attribute should be {_blank}.

Building Blocks
CSS treats each HTML element as if it is in its own box. This box will either be a block-level box or an inline box. Block-level boxes start on a new line and act as the main building blocks of any layout, while inline boxes flow between surrounding texts. You can control how much space each box takes up by setting the width of the boxes (and sometimes the height, too). To separate boxes, you can use borders, margins, padding, and background colors. Block-level boxes start on a new line and act as.
If one block-level element sits inside another block-level element then the outer box is known as the containing or parent element.
It is common to group a number of elements together inside a {<div>} (or other block-level) element. For example, you might group together all of the elements that form the header of a site (such as the logo and the main navigation). The <div> element that contains this group of elements is then referred to as the containing element.
CSS has the following positioning schemes that allow you to control the layout of a page: normal flow, relative positioning, and absolute positioning. You specify the positioning scheme using the position property in CSS. You can also float elements using the float property.
Normal flow
Every block-level element appears on a new line, causing each item to appear lower down the page than the previous one. Even if you specify the width of the boxes and there is space for two elements to sit side-by side, they will not appear next to each other. This is the default behavior (unless you tell the browser to do something else).
Relative Positioning
This moves an element from the position it would be in normal flow, shifting it to the top, right, bottom, or left of where it would have been placed. This does not affect the position of surrounding elements; they stay in the position they would be in in normal flow.
Ab solute positioning
This positions the element in relation to its containing element. It is taken out of normal flow, meaning that it does not affect the position of any surrounding elements (as they simply ignore the space it would have taken up). Absolutely positioned elements move as users scroll up and down the page.

In normal flow, each block-level element sits on top of the next one. Since this is the default way in which browsers treat HTML elements, you do not need a CSS property to indicate that elements should appear in normal flow, but the syntax would be:

position: static;

Relative positioning moves an element in relation to where it would have been in normal flow. For example, you can move it 10 pixels lower than it would have been in normal flow or 20% to the right. You can indicate that an element should be relatively positioned using the position property with a value of relative.
When the position property is given a value of absolute, the box is taken out of normal flow and no longer affects the position of other elements on the page. (They act like it is not there.)
The box offset properties (top or bottom and left or right) specify where the element should appear in relation to its containing element.
Fixed positioning is a type of absolute positioning that requires the position property to have a value of fixed.
The float property allows you to take an element in normal flow and place it as far to the left or right of the containing element as possible. Anything else that sits inside the containing element will flow around the element that is floated.
A lot of layouts place boxes next to each other. The float property is commonly used to achieve this. When elements are floated, the height of the boxes can affect where the following elements sit.

Different visitors to your site will have different sized screens that show different amounts of information, so your design needs to be able to work on a range of different sized screens.
When designing for print, you always know the size of the piece of paper that your design will be printed on. However, when it comes to designing for the web, you are faced with the unique challenge that different users will have different sized screens.
Resolution refers to the number of dots a screen shows per inch. Some devices have a higher resolution than desktop computers and most operating systems allow users to adjust the resolution of their screens.
Because screen sizes and display resolutions vary so much, web designers often try to create pages of around 960-1000 pixels wide (since most users will be able to see designs this wide on their screens).

To create a fixed width layout, the width of the main boxes on a page will usually be specified in pixels (and sometimes their height, too).
The liquid layout uses percentages to specify the width of each box so that the design will stretch to fit the size of the screen.
CSS frameworks aim to make your life easier by providing the code for common tasks, such as creating layout grids, styling forms, creating printer-friendly versions of pages and so on. You can include the CSS framework code in your projects rather than writing the CSS from scratch.

Functions let you group a series of statements together to perform a specific task. If different parts of a script repeat the same task, you can reuse the function (rather than repeating the same set of statements).
To create a function, you give it a name and then write the statements needed to achieve its task inside the curly braces.
This is known as a function declaration.
 

Having declared the function, you can then execute all of the statements between its curly braces with just one line of code.
This is known as calling the function.
Sometimes a function needs specific information to perform its task. In such cases, when you declare the function you give it parameters. Inside the function, the parameters act like variables.
When you call a function that has parameters, you specify the values it should use in the parentheses that follow its name. The value are called argument, and they can be provided as values or as variables.
