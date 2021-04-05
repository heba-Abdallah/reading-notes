Key Concepts in Positioning Elements
Building Blocks CSS treats each HTML element as if it is in its own box. This box will either be a block-level box or an inline box. Block-level boxes start on a new line and act as the main building blocks of any layout, while inline boxes flow between surrounding texts. You can control how much space each box takes up by setting the width of the boxes (and sometimes the height, too). To separate boxes, you can use borders, margins, padding, and background colors.
Containing Elements
If one block-level element sits inside another block-level element then the outer box is known as the containing or parent element. It is common to group a number of elements together inside a 
(Or other block-level) element. For example, you might group together all of the elements that form the header of a site (such as the logo and the main navigation). The element that contains this group of elements is then referred to as the containing element.

Controlling the Position of Elements

CSS has the following positioning schemes that allow you to control the layout of a page: normal flow, relative positioning, and absolute positioning. You specify the positioning scheme using the position property in CSS. You can also float elements using the float property.
Normal flow: every block-level element appears on a new line, causing each item to appear lower down the page than the previous one. Even if you specify the width of the boxes and there is space for two elements to sit side-by-side, they will not appear next to each other. This is the default behavior (unless you tell the browser to do something else).
Relative Positioning: this moves an element from the position it would be in normal flow, shifting it to the top, right, bottom, or left of where it would have been placed. This does not affect the position of surrounding elements; they stay in the position they would be in in normal flow.
Absolute positioning: this positions the element in relation to its containing element. It is taken out of normal flow, meaning that it does not affect the position of any surrounding elements (as they simply ignore the space it would have taken up). Absolutely positioned elements move as users scroll up and down the page.

To indicate where a box should be positioned, you may also need to use box offset properties to tell the browser how far from the top or bottom and left or right it should be placed.
Fixed positioning: this is a form of absolute positioning that positions the element in relation to the browser window, as opposed to the containing element. Elements with fixed positioning do not affect the position of surrounding elements and they do not move when the user scrolls up or down the page.
Floating Elements: Floating an element allows you to take that element out of normal flow and position it to the far left or right of a containing box. The floated element becomes a block-level element around which other content can flow.

In normal flow, each block-level element sits on top of the next one. Since this is the default way in which browsers treat HTML elements, you do not need a CSS property to indicate that elements should appear in normal flow, but the syntax would be:

Position: static; I have not specified a width property for the heading element, so you can see how it stretches the width of the entire browser window by default. 
Relative positioning moves an element in relation to where it would have been in normal flow, For example, you can move it 10 pixels lower than it would have been in normal flow or 20% to the right. You can indicate that an element should be relatively positioned using the position property with a value of relative. You then use the offset properties (top or bottom and left or right) to indicate how far to move the element from where it would have been in normal flow. To move the box up or down, you can use either the top or bottom properties. To move the box horizontally, you can use either the left or right properties. The values of the box offset properties are usually given in pixels, percentages or ems.

When the position property is given a value of absolute, the box is taken out of normal flow and no longer affects the position of other elements on the page. (They act like it is not there.), the box offset properties (top or bottom and left or right) specify where the element should appear in relation to its containing element. 
Fixed positioning is a type of absolute positioning that requires the position property to have a value of fixed, it positions the element in relation to the browser window. Therefore, when a user scrolls down the page, it stays in the exact same place. It is a good idea to try this example in your browser to see the effect. To control where the fixed position box appears in relation to the browser window, the box offset properties are used.

When you use relative, fixed, or absolute positioning, boxes can overlap. If boxes do overlap, the elements that appear later in the HTML code sit on top of those that are earlier in the page. If you want to control which element sits on top, you can use the z-index property. Its value is a number, and the higher the number the closer that element is to the front. For example, an element with a z-index of 10 will appear over the top of one with a z-index of 5.

Screen Sizes
Different visitors to your site will have different sized screens that show different amounts of information, so your design needs to be able to work on a range of different sized screens.
When designing for print, you always know the size of the piece of paper that your design will be printed on. However, when it comes to designing for the web, you are faced with the unique challenge that different users will have different sized screens, since computers have been sold to the public, the size of screens has been steadily increasing. This means that some people viewing your site might have 13 inch monitors while others may have 27+ inch monitors.
Resolution refers to the number of dots a screen shows per inch. Some devices have a higher resolution than desktop computers and most operating systems allow users to adjust the resolution of their screens.
Fixed Width Layouts
Fixed width layout designs do not change size as the user increases or decreases the size of their browser window. Measurements tend to be given in pixels.

Advantages:
●Pixel values are accurate at controlling size and positioning of elements. 
●The designer has far greater control over the appearance and position of items on the page than with liquid layouts. 
●You can control the lengths of lines of text regardless of the size of the user's window. 
●The size of an image will always remain the same relative to the rest of the page.

Disadvantages:
●You can end up with big gaps around the edge of a page.
 ●If the user's screen is a much higher resolution than the designer's screen, the page can look smaller and text can be harder to read. 
●If a user increases font sizes, text might not fit into the allotted spaces. 
●The design works best on devices that have a site or resolution similar to that of desktop or laptop computers.
 ●The page will often take up more vertical space than a liquid layout with the same content.

Liquid Layouts
Liquid layout designs stretch and contract as the user increases or decreases the size of their browser window. They tend to use percentages.
Advantages:
●Pages expand to fill the entire browser window so there are no spaces around the page on a large screen. 
●If the user has a small window, the page can contract to fit it without the user having to scroll to the side.
 ●The design is tolerant of users setting font sizes larger than the designer intended (because the page can stretch).
Disadvantages:
●If you do not control the width of sections of the page then the design can look very different than you intended, with unexpected gaps around certain elements or items squashed together.
 ●If the user has a wide window, lines of text can become very long, which makes them harder to read. ●If the user has a very narrow window, words may be squashed and you can end up with few words on each line.
 ●If a fixed width item (such as an image) is in a box that is too small to hold it (because the user has made the window smaller) the image can overflow over the text.
