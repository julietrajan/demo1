---
layout: default
title: "video1"
category: "Comic"
sub-category: "Security"
---
{% raw %}
<h1>Drag and Drop Canvas</h1>
<p>Drag the shapes around the canvas!</p>

<canvas id="myCanvas" width="800" height="400" style="border:1px solid #000000;"></canvas>

<script>
    const canvas = document.getElementById('myCanvas');
    const ctx = canvas.getContext('2d');
    let shapes = [
        { x: 50, y: 50, width: 100, height: 100, color: 'red', isDragging: false },
        { x: 200, y: 50, width: 100, height: 100, color: 'green', isDragging: false },
        { x: 350, y: 50, width: 100, height: 100, color: 'blue', isDragging: false }
    ];
    let dragIndex = -1;

    function drawShapes() {
        ctx.clearRect(0, 0, canvas.width, canvas.height);
        shapes.forEach(shape => {
            ctx.fillStyle = shape.color;
            ctx.fillRect(shape.x, shape.y, shape.width, shape.height);
        });
    }

    function getMousePos(canvas, evt) {
        const rect = canvas.getBoundingClientRect();
        return {
            x: evt.clientX - rect.left,
            y: evt.clientY - rect.top
        };
    }

    function isMouseInShape(mouse, shape) {
        return mouse.x > shape.x && mouse.x < shape.x + shape.width &&
               mouse.y > shape.y && mouse.y < shape.y + shape.height;
    }

    canvas.addEventListener('mousedown', (evt) => {
        const mousePos = getMousePos(canvas, evt);
        shapes.forEach((shape, index) => {
            if (isMouseInShape(mousePos, shape)) {
                shape.isDragging = true;
                dragIndex = index;
            }
        });
    });

    canvas.addEventListener('mousemove', (evt) => {
        if (dragIndex !== -1) {
            const mousePos = getMousePos(canvas, evt);
            const shape = shapes[dragIndex];
            shape.x = mousePos.x - shape.width / 2;
            shape.y = mousePos.y - shape.height / 2;
            drawShapes();
        }
    });

    canvas.addEventListener('mouseup', () => {
        if (dragIndex !== -1) {
            shapes[dragIndex].isDragging = false;
            dragIndex = -1;
        }
    });

    canvas.addEventListener('mouseout', () => {
        if (dragIndex !== -1) {
            shapes[dragIndex].isDragging = false;
            dragIndex = -1;
        }
    });

    drawShapes();
</script>

<style>
    canvas {
        display: block;
        margin: 20px auto;
    }
</style>
{% endraw %}
