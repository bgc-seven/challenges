# Drawing on the Web

Did you know that you can actually _draw_ on the web?

Your challenge is to draw a line on a web page.

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
			background-color: black;
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
		ctx.arc(60, 65, 5, 0, Math.PI * 2, true)
	</script>
</body>
</html>

```
