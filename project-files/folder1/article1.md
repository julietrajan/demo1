---
layout: default
title:  "Need for MFA"
category: "Case Study"
sub-category: "Security"
courses: [SC-200,SC-300, AZ-500]
---
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Drag and Drop Example</title>
    <style>
        .square {
            width: 50px;
            height: 50px;
            margin: 10px;
            display: inline-block;
        }
        .red { background-color: red; }
        .blue { background-color: blue; }
        .green { background-color: green; }
        .drop-area {
            width: 100px;
            height: 100px;
            border: 2px dashed #ccc;
            margin: 10px;
            display: inline-block;
        }
    </style>
</head>
<body>
    <div>
        <div class="square red" draggable="true" ondragstart="drag(event)" id="redSquare"></div>
        <div class="square blue" draggable="true" ondragstart="drag(event)" id="blueSquare"></div>
        <div class="square green" draggable="true" ondragstart="drag(event)" id="greenSquare"></div>
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

            if (draggedElement.classList.contains(dropAreaColor)) {
                event.target.appendChild(draggedElement);
                document.getElementById("message").innerText = "Correct!";
            } else {
                document.getElementById("message").innerText = "Error: Incorrect match.";
            }
        }
    </script>
</body>
</html>
