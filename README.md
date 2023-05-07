Download Link: https://assignmentchef.com/product/solved-lab2
<br>
INSTRUCTIONS

————

Compile this code. You should see 3 rectangles, one of which you can move

with the ‘w’, ‘a’, ‘s’, and ‘d’ keys.

Read through this code! Try to understand it before starting the assignment.

Comment confusing lines with what you think code is doing, and experiment

with existing code to test your understanding.

Once you feel comfortable with this code, accomplish each of the following,

and make sure your code compiles and runs after each step is completed.

1) Get and set functions

<ol>

 <li>a) In Rect, create a get and set methods for “min” and “max”. Use the</li>

</ol>

signature “void setMin(Vec2 const &amp; min)” and

“void setMax(Vec2 const &amp; max)”. Use the “this” pointer to disambiguate

“min” and “max”.

1) Refactor userRect to be dynamic

<ol>

 <li>a) Make userRect a dynamic object. That means it should be declared as</li>

</ol>

“Rect * userRect” instead of “Rect userRect”. Use new to dynamically

allocate.

<ol>

 <li>b) the member operator ‘.’ will need to be replaced with the</li>

</ol>

pointer-to-member operator ‘-&gt;’

<ol>

 <li>c) Don’t forget to delete userRect at the end of the program!</li>

</ol>

2) Operator Overloading

<ol>

 <li>a) Overload the += operator for Vec2, and have it do exactly what</li>

</ol>

Vec2::add does.

<ol>

 <li>b) Replace uses of Vec2::add with the += operator. For example, instead of</li>

</ol>

“min.add(delta);”, use “min += delta;”.

3) Random rectangles, by reference and by pointer

<ol>

 <li>a) create a method with the method signature “void setRandom(Rect &amp; r)”.</li>

</ol>

This function will give the passed-in Rect object a random location.

The random x should be between 0 and 50 x. The random y should be

between 0 and 20. Limit the possible width and height to a minimum of 2

and a maximum of 10.

<ol>

 <li>b) test “void setRandom(Rect &amp; r)” on the local Rect object “rect0”.</li>

 <li>c) create a method with the method signature</li>

</ol>

“void setRandomByPointer(Rect * r)”, which functions the same as

“void setRandom(Rect &amp; r)”, except that the argument is

passed-by-pointer.

<ol>

 <li>d) test “void setRandomByPointer(Rect * r)” on the local Rect object</li>

</ol>

“rect1”.

4) Test and show overlap

<ol>

 <li>a) Using the existing function “isOverlapping(Rect const &amp;)”, test to see</li>

</ol>

if userRect collides with any other Rect objects. If userRect is

overlapping, draw it with ‘+’ instead ‘#’.

<ol>

 <li>b) Create a Rect * pointer that points to the address if the Rect object</li>

</ol>

that userRect collides with. It should point at NULL if userRect is

colliding with no other Rect objects.

<ol>

 <li>c) Print to the screen the width and height of a Rect object that userRect</li>

</ol>

collides with. If no collision is happening, print “no collision”

instead.

5) Array of objects

<ol>

 <li>a) Replace the Rect objects rect0 and rect1 with an array of 2 Rect</li>

</ol>

objects, “rect[2]”.

<ol>

 <li>b) Make sure you replace every remaining “rect0” with “rect[0]”, and every</li>

</ol>

“rect1” with “rect[1]”.

<ol start="5">

 <li>c) Increase the size of the “rect” array to 5. Make sure all 5 Rect</li>

</ol>

objects are randomized, drawn to the screen, and tested for collision.

<ol>

 <li>d) If you have not already done so, replace</li>

</ol>

duplicate-code-using-array-elements with a for-loop. For example:

If you have:

rect[0].draw(‘0’);

rect[1].draw(‘1’);

rect[2].draw(‘2’);

rect[3].draw(‘3’);

rect[4].draw(‘4’);

Replace it with:

for(int i = 0; i &lt; NUMBER_OF_RECTS; i++)

{

rect[i].draw(‘0’+i);

}

Do this where objects are randomized, drawn, and tested for collision




Achievements: (if you finished, and would like a challenge, try these)




[Union Job] When the userRect collides with another rectangle, instead of

drawing the entire userRect with ‘+’ signs, draw only over the

intersecting area.

[Dat Rectangle] Implement an interface that allows the user to select the

moving rectangle, cycling through all possible rectangles with the tab

key, indicating the selected rectangle by drawing it with ‘#’.

[One Size Fits All] Implement an interface that allows the user to increase

or decrease the size of the selected rectangle. For example, if ‘w’,

‘a’, ‘s’, and ‘d’ is used to move the rectangle, ‘W’, ‘A’, ‘S’, and ‘D’

could move the Rect’s max location up, left, down, and right.

[Add Another] When the user presses space, dynamically resize the rect array

to hold an additional random rectangle.

[One Too Many] When the user presses backspace, dynamically resize the rect

array to hold one less rectangle, removing the last one in the list.

When finished:

1) Make sure your name is at the top of this source file

2) Submit this project online

<ol>

 <li>a) Right-click on the .cpp file’s name within visual studio, and select</li>

</ol>

“Open Containing Folder”

<ol>

 <li>b) Close Visual Studio (you may re-open this .cpp file by right-clicking</li>

</ol>

on it in the file system, and slecting edit)

<ol>

 <li>c) Make sure the following files are DELETED from the project’s file</li>

</ol>

structure:

* Any file with the extension: “.ncb”, “.sdf”

* Any folder named: “Debug” or “ipch”

* If Visual Studio is open, you will not be able to delete some files

* If you do not see file extensions, press Alt in the file explorer,

select “Tools”-&gt;”Folder options…”-&gt;”View”, and uncheck

“Hide extensions for known file types”.

<ol>

 <li>d) zip the file structure (the project), which is now missing the</li>

</ol>

temporary files

* Select all of the files in the project folder

* If the resulting zip file is more than 1mb, you have included

temporary files mentioned above. Delete temporary files (that don’t

have a .cpp or .h extension) and try again.


