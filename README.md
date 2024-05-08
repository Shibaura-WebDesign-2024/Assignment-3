# Styling with CSS 

## Styling text

Download menu.html from the material folder. This is an online menu.
I have added some styles in the head section. There are a few styles needed to be added. The final decorated one should look similar to Fig. 1. 

Can you try to fill in the missing styles? 

Hint: all necessary elements are already created; you only need to write the decoration rule. No colors are manipulated in this part.

Notice that we didn’t touch a single character of the document markup (HTML) in the process. That’s the beauty of keeping style separate from structure.

![image](https://github.com/Shibaura-WebDesign-2024/Assignment-3/assets/167287319/eafb9a30-3991-487f-8b6d-7c8af2358127)


## Colors and links 
## 2-A Adding colors and a background image to your page
Now, let’s give your menu a little personality with foreground and background image.
The image file (bgimage.png) should be placed in “image” folder. Be sure to include the pathname relative to the current HTML document.

Hint: you should style h1, h2, header. See Figure 2 for the decorated version. 
Color code: 

![image](https://github.com/Shibaura-WebDesign-2024/Assignment-3/assets/167287319/d2abfc0e-3767-4b10-9125-89639be9b4c7)
![image](https://github.com/Shibaura-WebDesign-2024/Assignment-3/assets/167287319/e36d1773-c965-4c58-b99b-fc682f706717)

## 2-B Decorating Link and its action
I’ve already added a rule that turns underlines off under links (text-decoration:none), so we’ll be relying on color to make the links pop. Please decorate the link as follows
- Write a rule that makes links the same purple as the h1.
- Make visited links a muted purple.
- When the mouse is placed over links, make the text a brighter purple. and add a white background color.
- This will look a little like the links are lighting up when the mouse is pointing at it. Use these same style rules for when the links are in focus.
- As the mouse is being clicked (or tapped on a touch device), add a white background color and make the text turn a vibrant purple. 

Make sure that all of your link pseudo-classes are in the correct order.

## Decorating timetable 
Use your timetable that you created in the previous class. Please add some style to decorate the table. You are free to design. Please try to also play with adding the background image or patterns and manipulate the opacity, position, etc. 


Hints: 
There are plenty of free resource that you can use for decorating your website.  Here are only a few examples.

### Photos 
www.pexel.com 

### Pattern (repeating) 
http://www.colourlovers.com/patterns
http://subtlepatterns.com
https://www.wowpatterns.com/

### Icons 
https://www.flaticon.com/

### Make your own background
http://patternizer.com/izfa

## Flexbox starter


Note: Be sure to use one of the Flexbox-supporting browsers
1. Open bakery-styles.css in a text editor and start by making the ul element in the nav element as neutral as possible:
```
nav ul {
margin: 0;
padding: 0;
list-style-type: none;
}
```
2. Turn that ul element into a flexbox by setting its display to flex. As a result, all of the li elements become flex items. Because we want rows and no wrapping, the default values for flex-direction and flex-wrap are fine, so the properties can be omitted:
```
nav ul {
…
display: flex;
}
```
4. Save the document and look at it in a browser. You should see that the links are lined up tightly in a row, which is an improvement, but we have more work to do.
5. Now we can work on the appearance of the links. Start by making the a elements in the nav list items display as block elements instead of inline. Give them 1px rounded borders, padding within the borders (.5em top and bottom, 1em left and right), and .5em margins to give them space and to open up the brown navigation bar.
```
nav ul li a {
display: block;
border: 1px solid;
border-radius: .5em;
padding: .5em 1em;
margin: .5em;
}
```
7. We want the navigation menu to be centered in the width of the nav section. Add the following declaration for the nav ul element:
```
nav ul {
…
display: flex;
justify-content: center;
}
```

Figure 3 shows the way your navigation menu should look when you are finished.

![image](https://github.com/Shibaura-WebDesign-2024/Assignment-3/assets/167287319/03eaa637-bbec-4443-ac23-7714f8181ab0)


## A Flexible online menu

Open index.html Can you try to make a flexible online menu just like Figure 4?

Hints:
1.	You will need to use flex-wrap property on #menu container, and justify-content property. 
2.	The price buttons have to line up at the bottom of each menu item. This will be possible if each item is also a flex container.
Hint: you will need to turn the element that contain h2 and p into a nested flex container by setting its display to flex and specifying the direction as column so they continue to stack up vertically. 
3.	Instead of having lots of empty space inside the menu container, let’s make the items fill the available space. Because we want the items to be fully flexible, we can use the auto value for flex (the same as flex: 1 1 auto;). 
4.	Make the photos appear at the top of each menu item.  Because each section is a flex container, we can use the order property to move its items around. In this case, select the paragraphs with the “photo” class name and give it a value less than the default 0. This will make the photo display first in the line
```
.photo {
order: -1;
}
```

 ![image](https://github.com/Shibaura-WebDesign-2024/Assignment-3/assets/167287319/3e97c98e-9646-427d-b054-40f0d16a7365)


## Grid starter

Open index.html Figure 5 shows the grid layout of the final version of this page. Can you try to make a flexible online menu just like Figure 6?
1. Start by turning the containing element, the #layout div, into a grid container by setting its display mode to “grid”:
```
#layout {
…
display: grid;
}
```
2. Figure 5 shows the row and column tracks required to accommodate the content in the desired layout. Start by defining the rows as specified in the sketch, using the grid-template-rows property. There should be six values, representing each of the six rows.
```
#layout {
…
display: grid;
grid-template-rows: 3em 20px 150px 300px 5em;
}
```
3. Do the same for the seven columns. Make the column grow and shrink with the available space by specified its width in fractional units (1fr). The remaining columns create 150px-wide cells for three images and 20px of space before them. You can use repeat () function to repeat the spaces and figure columns three times like this:
```
grid-template-columns: 1fr repeat(3, 20px 150px);
```
4. Finally, let’s assign names to the grid lines that border the grid area where the main content element should appear. The names give us some intuitive options for placing that item later. The main area starts at the third row track, so assign the name “mainstart” to the grid line between the second and third row track measurements:
```
grid-template-rows: 3em 20px [main-start] 150px 300px 5em;
```
5. The main area extends into the last row track, so assign the name “main-end” to the last grid line in the grid (after the last row track):
```
grid-template-rows: 3em 20px [main-start] 150px 300px 5em [main-end];
```
6. Do the same for the grid lines that mark the boundaries of the column track where the main content goes:
```
grid-template-columns: [main-start] 1fr [main-end] repeat(3, 20px 150px);
```
7. Now, let’s place the items on the grid. Start by placing the nav element into the first row of the grid, using the four grid line properties:
```
nav {
grid-row-start: 1;
grid-row-end: 2;
grid-column-start: 1;
grid-column-end: 8; /* you could also use -1 */
}
```
8. Place the figures in their positions on the grid. Start by putting the third figure (#figC) in its place in the far-right column by using the shorthand grid-row and grid-column properties. It goes between the 3rd and 4th row grid lines and extends from the 7th to 8th column lines. For columns, instead of 7 and 8, use the negative value for the last line and span it one space to the left to get to the starting point:
```
#figC {
grid-row: 3 / 4;
grid-column: span 1 / -1;
}
```
9. Now position the #figA and #figB elements by using the grid-area property with line values. Remember that the values go in the order top, left, bottom, right (counterclockwise around the area).
```
#figA {
grid-area: 3 / 3 / 4 / 4;
}
#figB {
grid-area: 3 / 5 / 4 / 6;
}
```
10. We gave the grid lines around the main area names, so let’s use them to place the main grid item:
```
main {
grid-row: main-start / main-end;
grid-column: main-start / main-end;
}
```
11. Do you remember that when you name lines around an area *-start and *-end, it creates an implicitly named area *? Because we named the lines according to this syntax, we could also place the main element with grid-area like this:
```
main {
grid-area: main;
}
```
12. Finally, we can put the footer into its place. It starts at the last row grid line and spans back one track. For columns, it starts at the third line and goes to the last. Here is one way to write those instructions. Can you come up with others that achieve the same result?
```
footer {
grid-row: 5 / 6;
grid-column: 3 / -1;
}
```
13. Try opening your finished file in the browser. When the browser is stretched, everything may looks fine. However, when you narrow the browser window, the text in the main element overflows its cell. Can you try to fix this? (Hint: it is something to do with measurement of the row in grid)

![image](https://github.com/Shibaura-WebDesign-2024/Assignment-3/assets/167287319/032f077c-9001-4b76-a176-53adff94619a)

![image](https://github.com/Shibaura-WebDesign-2024/Assignment-3/assets/167287319/0bacb27b-8c98-49f4-9369-e927cfa9dc16)
Figure 6: The finished version of part 6


## A final touch using Grid

Now you can use your new grid skills to give it a two-column layout that would be appropriate for tablets and larger screens for Black goose bakery page (The same files that you used for part 4). Figure 7 shows the finished page. Can you add grid layout to make your finished page look similar to Figure 7?

Hints
1.	Add a div around all of the content elements (from header to footer), and give it the id “container”.

```
<body>
<div id="container">
<header>…</header>
<main>…</main>
<aside>…</aside>
<footer>…</footer>
</div>
</body>
```
Then, add a new style to make the new div display as a grid
```
		#container{
			Display: grid;
		}
```
2.	Here are hints for row height setting
o	First row - It should observe the height settings on the elements within it and automatically accommodate the content. 
o	Second row- Make sure that the track will expand at least as much as necessary to fit the text. 
o	Third row - a height of 5em should be sufficient to fit the few lines of text with a comfortable amount of space
o	There are only two column tracks (main, hours sidebar), make sure that the main content be ensured that the text will never get narrower than 25em but it should be able to expand to fill the available space in the browser. 
o	You can name the areas in your grid to place items in it easily and efficiently.

![image](https://github.com/Shibaura-WebDesign-2024/Assignment-3/assets/167287319/559bb616-fa9b-4d62-8e27-9e0cd25359fc)
Figure 7: The finished version of part 7, black goose bakery page with a two-column grid layout








