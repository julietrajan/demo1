---
layout: default
title: "video1"
category: "Comic"
sub-category: "Security"
---
## Line of business extension

{% raw %}
<p>Line of business extension!</p>

<canvas id="myCanvas" width="1000" height="830" style="border:1px solid #000000;"></canvas>

The data flows through the solution as follows:

<br> 1. Supplier data stored in Common Data Services (CDS) is moved to SQL via Data Factory.
<br> 2. Purchase order (PO) data stored in ERP system is sent to Azure SQL database.
<br> 3. Azure API Management is used to expose an Azure function to the Power Platform.
<br> 4. Power Apps retrieves data from Azure SQL Database through the Azure Function being exposed by Azure API Management.
<br> 5. User reviews and updates POs in Power Apps and sends this data to suppliers through CSV exports.
<br> 6. Power BI reports trends in supplier status.

<script>
    const canvas = document.getElementById('myCanvas');
    const ctx = canvas.getContext('2d');
    const images = [
        { src: 'adf.png', x: 50, y: 10, width: 50, height: 50, isDragging: false, name: 'Azure Data Factory' },
        { src: 'func1.png', x: 200, y: 10, width: 50, height: 50, isDragging: false, name: 'Azure Function' },
        { src: 'pbi.png', x: 350, y: 10, width: 50, height: 50, isDragging: false, name: 'Power BI' },
        { src: 'apim.png', x: 500, y: 10, width: 50, height: 50, isDragging: false, name: 'API Management' }
    ];
    let dragIndex = -1;

    function loadImages(callback) {
        let loadedImages = 0;
        images.forEach((image, index) => {
            const img = new Image();
            img.src = image.src;
            img.onload = () => {
                images[index].img = img;
                loadedImages++;
                if (loadedImages === images.length) {
                    callback();
                }
            };
        });
    }

    function drawImages() {
        ctx.clearRect(0, 0, canvas.width, canvas.height);
        images.forEach(image => {
            ctx.drawImage(image.img, image.x, image.y, image.width, image.height);
        });
        // Draw 3D divider line
        draw3DDivider();
    }

    function draw3DDivider() {
        const gradient = ctx.createLinearGradient(0, 80, canvas.width, 80);
        gradient.addColorStop(0, '#d3d3d3');
        gradient.addColorStop(0.5, '#ffffff');
        gradient.addColorStop(1, '#d3d3d3');

        ctx.strokeStyle = gradient;
        ctx.lineWidth = 4;
        ctx.beginPath();
        ctx.moveTo(0, 80); // Adjust the y-coordinate as needed
        ctx.lineTo(canvas.width, 80);
        ctx.stroke();

        ctx.strokeStyle = 'rgba(0, 0, 0, 0.2)';
        ctx.lineWidth = 2;
        ctx.beginPath();
        ctx.moveTo(0, 82); // Slightly below the main line for shadow effect
        ctx.lineTo(canvas.width, 82);
        ctx.stroke();
    }

    function getMousePos(canvas, evt) {
        const rect = canvas.getBoundingClientRect();
        return {
            x: evt.clientX - rect.left,
            y: evt.clientY - rect.top
        };
    }

    function isMouseInImage(mouse, image) {
        return mouse.x > image.x && mouse.x < image.x + image.width &&
               mouse.y > image.y && mouse.y < image.y + image.height;
    }

    canvas.addEventListener('mousedown', (evt) => {
        const mousePos = getMousePos(canvas, evt);
        images.forEach((image, index) => {
            if (isMouseInImage(mousePos, image)) {
                image.isDragging = true;
                dragIndex = index;
            }
        });
    });

    canvas.addEventListener('mousemove', (evt) => {
        if (dragIndex !== -1) {
            const mousePos = getMousePos(canvas, evt);
            const image = images[dragIndex];
            image.x = mousePos.x - image.width / 2;
            image.y = mousePos.y - image.height / 2;
            drawImages();
        } else {
            const mousePos = getMousePos(canvas, evt);
            let hoveredImage = null;
            images.forEach(image => {
                if (isMouseInImage(mousePos, image)) {
                    hoveredImage = image;
                }
            });
            if (hoveredImage) {
                canvas.title = hoveredImage.name;
            } else {
                canvas.title = '';
            }
        }
    });

    canvas.addEventListener('mouseup', () => {
        if (dragIndex !== -1) {
            images[dragIndex].isDragging = false;
            dragIndex = -1;
        }
    });

    canvas.addEventListener('mouseout', () => {
        if (dragIndex !== -1) {
            images[dragIndex].isDragging = false;
            dragIndex = -1;
        }
    });

    loadImages(drawImages);
</script>

<style>
    body {
        background-color: #f0f0f0;
        font-family: Arial, sans-serif;
    }

    canvas {
        display: block;
        margin: 20px auto;
        background: url('arc1.png') no-repeat center center;
        background-size: cover;
        border: 5px solid #333;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
    }

    .draggable-icon {
        margin: 10px 0;
        cursor: grab;
        /* border: 2px solid #333; */ /* Remove this line to remove the black border */
        border-radius: 10px;
        box-shadow: 0 0 5px rgba(0, 0, 0, 0.3);
        transition: transform 0.2s;
        background-color: rgba(255, 255, 255, 0.8); /* Light background to differentiate from canvas */
    }

    .draggable-icon:active {
        cursor: grabbing;
        transform: scale(1.1);
    }

    #iconContainer {
        display: flex;
        flex-direction: column;
        align-items: center;
        padding: 10px;
        background-color: #fff;
        border: 2px solid #333;
        border-radius: 10px;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
    }
</style>
{% endraw %}
