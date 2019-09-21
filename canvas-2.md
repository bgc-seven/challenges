# More Angles in the Paint

> **Note:** This challenge assumes you've already done [My Blank
Canvas](canvas-1.md).  If you have not, do that challenge first or this will all
get super confusing, fast!


Okay we've seen hown to draw a rectangle but how but something else. Lets draw a triangle.

Before we used fillRect but now we will actually code each line ourselves.

## Challenge

1. **Draw a line.** In your `index.html` page, find your `<script>` right underneath your
   `<canvas>` element.  Somewhere after the line that contains `const ctx =
   ...`, place the following code:

```
ctx.strokeStyle = 'yellow'
ctx.beginPath()
ctx.moveTo(75, 50)
ctx.lineTo(100, 75)
ctx.closePath()
ctx.stroke()
```

2. **Complete the triangle.** Now that we've got a single line going, let's draw
   the other two.  Edit your script to include:

```
...
ctx.lineTo(100, 25)   // <== add this line
ctx.closePath()
ctx.stroke()
...
```

3. **Fill it in.** Sweet!  But wouldn't it be better filled in?
   instead of `stroke()`, we'll call `fill()`:

```
...
ctx.lineTo(100, 25)
ctx.closePath()
ctx.fill()        // <== replace "stroke()" with this
...
```
