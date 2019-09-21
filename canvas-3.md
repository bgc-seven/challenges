# We're all Smiles

> **Note:** This challenge assumes you've already done [More Angles in the
> Paint](canvas-2.md).  If you have not, do that challenge first or this will all
get super confusing, fast!

It's all well and good to draw lines, but did you know that you can draw curves
too?!

## Challenge

Include a smiley face in your masterpiece.

1. In your `index.html` file, locate the `<script>` right underneath your
   `<canvas>` element.  Inside there, find the bottom of the code that draws a
   triangle and add the following:

```
...
ctx.fill()     // <== this is the last line of drawing a triangle... find this

// Draw a smiley face
ctx.arc(75, 75, 50, 0, Math.PI * 2, true); // Outer circle
ctx.moveTo(110, 75);
ctx.arc(75, 75, 35, 0, Math.PI, false);  // Mouth (clockwise)
ctx.moveTo(65, 65);
ctx.arc(60, 65, 5, 0, Math.PI * 2, true);  // Left eye
ctx.moveTo(95, 65);
ctx.arc(90, 65, 5, 0, Math.PI * 2, true);  // Right eye
ctx.stroke();
```

