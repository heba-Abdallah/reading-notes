





Charts are far better for displaying data visually than tables and have the added benefit that no one is ever going to press-gang them into use as a layout tool. They’re easier to look at and convey data quickly, but they’re not always easy to create.

A great way to get started with charts is with Chart.js, a JavaScript plugin that uses HTML5’s canvas element to draw the graph onto the page. It’s a well-documented plugin that makes using all kinds of bar charts, line charts, pie charts and more, incredibly easy.

   

Drawing a line chart

To draw a line chart, the first thing we need to do is create a canvas element in our HTML in which Chart.js can draw our chart. So add this to the body of our HTML page:

   

Next, we need to write a script that will retrieve the context of the canvas, so add this to the foot of your body element:

   

Inside the same script tags we need to create our data, in this instance it’s an object that contains labels for the base of our chart and datasets to describe the values on the chart. Add this immediately above the line that begins ‘var buyers=’:

  

Drawing a pie chart

Our line chart is complete, so let’s move on to our pie chart. First, we need the canvas element:

  

Next, we need to get the context and to instantiate the chart:

  

You’ll notice that this time, we are going to supply some options to the chart.

Next we need to create the data. This data is a little different to the line chart because the pie chart is simpler, we just need to supply a value and a color for each section:

  

Now, immediately after the pieData we’ll add our options:

  

These options do two things, first they remove the stroke from the segments, and then they animate the scale of the pie so that it zooms out from nothing.

 
The grid

Before we can start drawing, we need to talk about the canvas grid or coordinate space. Our HTML skeleton from the previous page had a canvas element 150 pixels wide and 150 pixels high. To the right, you see this canvas with the default grid overlayed. Normally 1 unit in the grid corresponds to 1 pixel on the canvas. The origin of this grid is positioned in the top left corner at coordinate (0, 0). All elements are placed relative to this origin. So the position of the top left corner of the blue square becomes x pixels from the left and y pixels from the top, at coordinate (x, y). Later in this tutorial we'll see how we can translate the origin to a different position, rotate the grid and even scale it, but for now we'll stick to the default.

  

Drawing rectangles

Unlike SVG, <canvas> only supports two primitive shapes: rectangles and paths (lists of points connected by lines). All other shapes must be created by combining one or more paths. Luckily, we have an assortment of path drawing functions which make it possible to compose very complex shapes.

First let's look at the rectangle. There are three functions that draw rectangles on the canvas:

fillRect(x, y, width, height)

Draws a filled rectangle.

strokeRect(x, y, width, height)

Draws a rectangular outline.

clearRect(x, y, width, height)

Clears the specified rectangular area, making it fully transparent.

Each of these three functions takes the same parameters. x and y specify the position on the canvas (relative to the origin) of the top-left corner of the rectangle. width and height provide the rectangle's size.

Applying styles and colors

Colors

Up until now we have only seen methods of the drawing context. If we want to apply colors to a shape, there are two important properties we can use: fillStyle and strokeStyle.

fillStyle = color

Sets the style used when filling shapes.

strokeStyle = color

Sets the style for shapes' outlines.

color is a string representing a CSS <color>, a gradient object, or a pattern object. We'll look at gradient and pattern objects later. By default, the stroke and fill color are set to black (CSS color value #000000).

Note: When you set the strokeStyle and/or fillStyle property, the new value becomes the default for all shapes being drawn from then on. For every shape you want in a different color, you will need to reassign the fillStyle or strokeStyle property.

The valid strings you can enter should, according to the specification, be CSS <color> values. Each of the following examples describe the same color.

// these all set the fillStyle to 'orange' ctx.fillStyle = 'orange';ctx.fillStyle = '#FFA500';ctx.fillStyle = 'rgb(255, 165, 0)';ctx.fillStyle = 'rgba(255, 165, 0, 1)';