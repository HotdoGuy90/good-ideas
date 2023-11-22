# The Green Scale Algothrithm (or Green Scale Noise)

Invented by me, i have made a pretty cool algorithm. It requires a seed, x value (point), and y value (point). the algorithm goes as follows: `seed * x * y * e * π` (*e* being the 2.71 number in math) It is then further calculated to become a number from -1 to 1 (kinda like perlin or simplex noise) you can further use this output into a color value by going `(value + 1) / 2 * 255` and then make it a color value by saying `rgb(value - 23, value + 69, value)` and then set the color (or height) for the x and y points that you used before. An example with html is:

**html:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <style>
        body {
            padding: 0;
            margin: 0;
        }
    </style>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Green Scale!</title>
</head>
<body>
    <canvas id="algorithnContainer"></canvas>
    <script src="./main.js"></script>
</body>
</html>
```

**javascript:**
```javascript
function greenScale(seed, x, y) {
    const combinedValue = seed * x * y * Math.PI * Math.E;
    const scaledValue = combinedValue % 3 - 1;
    return scaledValue;
}

const canvas = document.getElementById("algorithmContainer");
const ctx = canvas.getContext('2d');

canvas.width = window.innerWidth;
canvas.height = window.innerHeight;

const seed = Math.floor(Math.random() * 1234567890);
for (var x=0;x<canvas.width;x++) {
    for (var y=0;y<canvas.height;y++) {
        var hue = greenScale(seed, x, y);
        var h = (hue + 1) / 2 * 255;
        
        ctx.strokeStyle = `rgb(${h - 23}, ${h + 69}, ${h})`;
        ctx.beginPath();
        ctx.moveTo(x, y);
        ctx.lineTo(x+1, y+1);
        ctx.stroke();

        
    }
}

ctx.font = "20px Times New Roman";
ctx.fillText("Seed: " + seed, 10, canvas.height - 20)
```

And you can make things like:
