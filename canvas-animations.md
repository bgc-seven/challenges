Ok let's start by getting the starter code below.

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
	</script>
</body>
</html>
```


Ok this time we're going to do a small animation


Let's create the following function inside of our script tags.

```
function draw() {
  ctx.drawImage(hero, 0, 0, 16,16, 100,100,32,32) // ctx.drawImage(image, sourceX, sourceY, sourceWidth, sourceHeight, destinationX, destinationY, destinationWidth, destinationHeight)
}
```

Our program doesn't know what hero is so let's create that. Under the  `const ctx = canvas.getContext('2d')`
Let's add 

``` 
const hero = new Image()
hero.src = 'hero.png'
```

Alright I wonder what that will do. Let's open our webpage and open our browser console.

Ok next lets change our draw function

```
function draw() {
			ctx.drawImage(hero, 0, 0, 16,16, 100,100,32,32) // left

			ctx.translate(canvas.width, 0);
			ctx.scale(-1, 1);
			ctx.drawImage(hero, 0, 0, 16,16, 100,100,32,32) // right
			ctx.scale(1,-1)
			ctx.drawImage(hero, 0, 32, 16,16, 140,140,32,32) // down

			ctx.drawImage(hero, 0, 16, 16,16, 30,30,32,32) //up
		}
    ```
