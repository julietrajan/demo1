---
layout: default
title: "video1"
category: "Comic"
sub-category: "Security"
---



## Drag and Drop Canvas with Icons
{% raw %}
<p>Drag the icons from the left and drop them onto the canvas on the right!</p>

<div style="display: flex;">
    <div id="iconContainer" style="width: 200px; border: 1px solid #000; padding: 10px;">
        <img src="images/icon1.png" id="icon1" class="draggable-icon" width="100" height="100">
        <img src="images/icon2.png" id="icon2" class="draggable-icon" width="100" height="100">
        <img src="images/icon3.png" id="icon3" class="draggable-icon" width="100" height="100">
    </div>
    <canvas id="myCanvas" width="600" height="400" style="border:1px solid #000000; margin-left: 20px;"></canvas>
</div>

<script>
    const canvas = document.getElementById('myCanvas');
    const ctx = canvas.getContext('2d');
    let images = [];
    let dragIndex = -1;
    let offsetX, offsetY;

    document.querySelectorAll('.draggable-icon').forEach((img, index) => {
        img.addEventListener('dragstart', (e) => {
            dragIndex = index;
            offsetX = e.offsetX;
            offsetY = e.offsetY;
        });
    });

    canvas.addEventListener('dragover', (e) => {
        e.preventDefault();
    });

    canvas.addEventListener('drop', (e) => {
        e.preventDefault();
        const mousePos = getMousePos(canvas, e);
        const img = document.querySelectorAll('.draggable-icon')[dragIndex];
        images.push({
            img: img,
            x: mousePos.x - offsetX,
            y: mousePos.y - offsetY,
            width: img.width,
            height: img.height
        });
        drawImages();
    });

    function drawImages() {
        ctx.clearRect(0, 0, canvas.width, canvas.height);
        images.forEach(image => {
            ctx.drawImage(image.img, image.x, image.y, image.width, image.height);
        });
    }

    function getMousePos(canvas, evt) {
        const rect = canvas.getBoundingClientRect();
        return {
            x: evt.clientX - rect.left,
            y: evt.clientY - rect.top
        };
    }
</script>

<style>
    .draggable-icon {
        margin: 10px 0;
        cursor: grab;
    }
    .draggable-icon:active {
        cursor: grabbing;
    }
    #iconContainer {
        display: flex;
        flex-direction: column;
        align-items: center;
    }
</style>
{% endraw %}
