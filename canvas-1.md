# Drawing on the Web

Did you know that you can actually _draw_ on the web?

1. Copy this to your website:

```

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="utf-8">
	<title>HTML5 boilerplate – all you really need…</title>
	<style>
		body{
			text-align: center;
			display: flex;
			justify-content: center;
			align-items: center;
		}
		
		#canvas {
			position: relative;
			display: block;
			width: 600px;
			height: 400px;
			margin: 0px;
			background-color: lightblue;
		}
	</style>
</head>
<body>
	<canvas id="canvas" width="400" height="400 "></canvas>
	<script>
		const canvas = document.getElementById('canvas')
		const ctx = canvas.getContext('2d')
		console.log('canvas: ', ctx)
		ctx.fillStyle = 'green'
		ctx.fillRect(150,150,100,100,100,100)
	</script>
</body>
</html>


```


2. Okay we've seen hown to draw a rectangle but how but something else. Lets draw a triangle.

Before we used fillRect but now we will actually code each line ourselves. Place the following code under neath your fillRect command.

```
		ctx.beginPath()
		ctx.moveTo(75, 50)
		ctx.lineTo(100, 75)
		ctx.lineTo(100, 25)
		ctx.fill()
		ctx.endPath()
```

As you can see we have a nice triangle. now above the ctx.beginPath let's add 2 lines of code.

```
ctx.strokeStyle = 'yellow'
ctx.fillStyle = 'lightblue;
```
3. Alright one last thing. above the ```ctx.endPath()``` let's add the following code

```
ctx.moveTo(75,75)
ctx.arc(75, 75, 50, 0, Math.PI * 2, true); // Outer circle
ctx.moveTo(110, 75);
ctx.arc(75, 75, 35, 0, Math.PI, false);  // Mouth (clockwise)
ctx.moveTo(65, 65);
ctx.arc(60, 65, 5, 0, Math.PI * 2, true);  // Left eye
ctx.moveTo(95, 65);
ctx.arc(90, 65, 5, 0, Math.PI * 2, true);  // Right eye
ctx.stroke();
```
