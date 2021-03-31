Image

A picture can say a thousand words, and great images help make the difference between an average-looking site and a really engaging one.

Images can be used to set the tone for a site in less time than it takes to read a description, and if you are building a site from scratch, it is good practice to create a folder for all of the images the site uses.

Adding Images

{<img>}

To add an image into the page you need to use an {<img>} element. This is an empty element (which means there is no closing tag). It must carry the following two attributes:

src :This tells the browser where it can find the image file. This will usually be a relative URL pointing to an image on your own site

alt :This provides a text description of the image which describes the image if you cannot see it.

Title: You can also use the title attribute with {<img>} element to provide additional information about the image.

And we can defined the specifies height and width of the image in pixels, it’s a good idea to specify the size of the image so that the browser can render the rest of the text on the page while leaving the right amount of space for the image that is still loading.

Where an image is placed in the code will affect how it is displayed. There are three examples of image placement that produce different results:

 1: before a paragraph: The paragraph starts on a new line after the image.

2: inside the start of a paragraph: The first row of text aligns with the bottom of the image.

 3: in the middle of a paragraph: The image is placed between the words of the paragraph that it appears in




Color

The color property allows you to specify the color of text inside an element. You can specify any color in CSS in one of three ways:

rgb values: These express colors in terms of how much red, green and blue are used to make it up. For example: rgb(100,100,90)

hex codes: These are six-digit codes that represent the amount of red, green and blue in a color, preceded by a pound or hash # sign. For example: #ee3e80

 color names: There are 147 predefined color names that are recognized by browsers. For example: DarkCyan

CSS treats each HTML element as if it appears in a box, and the background-color property sets the color of the background for that box. You can specify your choice of background color in the same three ways you can specify foreground colors: RGB values, hex codes, and color.

Every color on a computer screen is created by mixing amounts of red, green, and blue, Computer monitors are made up of thousands of tiny squares called pixels. When the screen is not turned on, it's black because it's not emitting any light. When it's on, each pixel can be a different color, creating a picture, the color of every pixel on the screen is expressed in terms of a mix of red, green, and blue — just like on a television screen.




RGB Values > Values for red, green, and blue are expressed as numbers between 0 and 255.

  

Hex Codes > Hex values represent values for red, green, and blue in hexadecimal code.

  

Color Names > Colors are represented by predefined names. However, they are very limited in number.

  

Hue > Hue is near to the colloquial idea of color. Technically speaking however, a color can also have saturation and brightness as well as hue.

Saturation > Saturation refers to the amount of gray in a color. At maximum saturation, there would be no gray in the color. At minimum saturation, the color would be mostly gray

Brightness > Brightness (or "value") refers to how much black is in a color. At maximum brightness, there would be no black in the color. At minimum brightness, the color would be very dark.

The CSS3 rgba property allows you to specify a color, just like you would with an RGB value, but adds a fourth value to indicate opacity. This value is known as an alpha value and is a number between 0.0 and 1.0 (so a value of 0.5 is 50% opacity and 0.15 is 15% opacity). The rgba value will only affect the element on which it is applied (not child elements).

CSS3 introduces an entirely new and intuitive way to specify colors using hue, saturation, and lightness values.

Hue: Hue is the colloquial idea of color. In HSL colors, hue is often represented as a color circle where the angle represents the color, although it may also be shown as a slider with values from 0 to 360.

Saturation: Saturation is the amount of gray in a color. Saturation is represented as a percentage. 100% is full saturation and 0% is a shade of gray.

Lightness: Lightness is the amount of white (lightness) or black (darkness) in a color. Lightness is represented as a percentage. 0% lightness is black, 100% lightness is white, and 50% lightness is normal. Lightness is sometimes referred to as luminosity


Text

Font-size

The font-size property enables you to specify a size for the font. There are several ways to specify the size of a font. The most common are:

Pixels > Pixels are commonly used because they allow web designers very precise control over how much space their text takes up. The number of pixels is followed by the letters px.

Percentages > the default size of text in browsers is 16px. So a size of 75% would be the equivalent of 12px, and 200% would be 32px.

You may have noticed that programs such as Word, Photoshop and InDesign offer the same sizes of text, the default size of text in a browser is 16 pixels. So if you use percentages or ems, you calculate the size of text you want based on the default size of the text used in browsers. For example, you could scale down to 12 pixels for body copy and scale up to 24 pixels for headings