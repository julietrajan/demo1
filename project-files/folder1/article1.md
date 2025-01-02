---
layout: default
title:  "Need for MFA"
category: "Case Study"
sub-category: "Security"
courses: [SC-200,SC-300, AZ-500]
---


<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Drag and Drop Text Example</title>
    <style>
        .draggable-text {
            display: inline-block;
            margin: 10px;
            padding: 5px;
            border: 1px solid #ccc;
            cursor: pointer;
        }
        .drop-area {
            width: 100px;
            height: 50px;
            border: 2px dashed #ccc;
            margin: 10px;
            display: inline-block;
            vertical-align: top;
        }
    </style>
</head>
<body>
    <div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="redText">Red</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="blueText">Blue</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="greenText">Green</div>
    </div>
    <div>
        <p>Red</p>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-color="red"></div>
    </div>
    <div>
        <p>Blue</p>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-color="blue"></div>
    </div>
    <div>
        <p>Green</p>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-color="green"></div>
    </div>
    <p id="message"></p>

    <script>
        function allowDrop(event) {
            event.preventDefault();
        }

        function drag(event) {
            event.dataTransfer.setData("text", event.target.id);
        }

        function drop(event) {
            event.preventDefault();
            var data = event.dataTransfer.getData("text");
            var draggedElement = document.getElementById(data);
            var dropAreaColor = event.target.getAttribute("data-color");

            if (draggedElement.innerText.toLowerCase() === dropAreaColor) {
                event.target.appendChild(draggedElement);
                document.getElementById("message").innerText = "Correct!";
            } else {
                document.getElementById("message").innerText = "Error: Incorrect match.";
            }
        }
    </script>
</body>
</html>
