# My Blank Canvas

You knew you can put text and share images on the web...

... but did you know you that you can actually _draw_ on the web?

All you need to get started is a blank canvas!

## Challenge

1. **Add a canvas.** In your `index.html`, find the `<body>` section and add a `canvas` element to
   it:

```
<canvas id="kara-walker" width="400px" height="400px"></canvas>
```
2. **Make it visible.** Find the `<style>` and set the background color of the canvas so that you can
   see it.

```
#kara-walker {
  background-color: #303030;
}
```
3. **Draw on it.**  Let's puts a rectangle on this canvas.  Right underneath the
   `<canvas>` add a `script` section.

```
<script>
  const canvas = document.getElementById('kara-walker')
  const ctx = canvas.getContext('2d')
  ctx.fillStyle = "#f64279"
  ctx.fillRect(150,150,100,100,100,100)
</script>
```


