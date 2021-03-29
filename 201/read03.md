List

ordered lists is created with the {<ol>} element, each item in the list is placed between an opening [<li>] tag and a closing [</li>] tag.

For unordered list is created with the {<ul>} element, each item in the list is placed between an opening [<li>] tag and a closing [</li>] tag.

The definition list is created with the {<dl>} element and usually consists of a series of terms and their definition, inside the {<dl>} element there is a [<dt>] element it's used to contain the term being defined (the definition term ), and [<dd>] element is used to contain the definition.

The nested list or sub-list it's for putting a second list inside an [<li>] element.

Box dimensions (width, height)

By default a box is sized big enough to hold it's contents. To set your own dimensions for a box you can use the height and width properties. Some page designs expand and shrink to fit size of the user's screen. In such designs, the min-width property specifies the smallest size a box can be displayed at when the browser window is narrow, and the max-width property indicates the maximum width a box can stretch to when the browser window is wide.

In the same way that you might want to limit the width of a box on a page, you may also want to limit the height of it, this is achieved using the min-height and max-height properties.

The over flow property tells the browser what to do if the content contained a box is larger than the box itself. It can have one of two values:

(hidden) this property simply hides any extra content that does not fit in the box, and the (scroll) property adds a scroll bar to the box so that users can scroll to see the missing content.

Every box has three available properties that can be adjusted to control it's appearance 

1- Border: every box has a border(even if it is not visible or is specified to be 0px wide)

2- Margin: sits outside the edge of the border, you can set the width of a margin to create a gap between the borders of two adjacent boxes.

3- Padding: is the space between the border of a box and any content contained within it.

The border-width property is used to control the width of a border. The value of this can either be given in pixels or using (thin, medium, thick) and you can control the individual size of borders using four separate properties. You can control the style of a border sing the border-style property (solid, dotted, dashed, double, groove, ridge, inset, outset)

You can specify the color of a border using either RGB values, hexacodes or CSS color names. It is possible to individually control the colors of the borders on different sides of a box. The border property allows you to specify the width, style and color of a border in one property.

Padding

The padding property allows you to specify how mush space should appear between the content of an element and it's border.

Margin

The margin property controls the gap between boxes. The value is commonly given in pixels, if you want to center a box on the page, you can set the left-margin and right-margin to auto.

In order to center a box on the page, you need to set a width for the box.




Switch statements

A switch statements starts with a variable called the switch value. Each case indicates a possible value for this variable and the code that should run if variable matches that value.

Loops

Loops check a condition, if it returns true, a code block will run. Then the condition will be checked again and if it still returns true, the code block will run again. It repeats until the condition returns false.

There are three common type of loops:

For: if you need to run code a specific number of times use a for loop, the condition on it is usually a counter which is used to tell how many times the loop should run.

While: if you do not know how many times the code should run, you can use a while loop. Here the condition can be something other than a counter, and the code will continue to loop for as long as the condition is true.

Do-While: the do...while loop is very similar to the while loop, but the difference is it will always run the statements inside the curly braces at ;east once, even if the condition evaluates to false.