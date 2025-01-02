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
            padding: 10px 20px;
            border: 2px solid #ccc;
            border-radius: 5px;
            background-color: #fff;
            cursor: pointer;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            transition: background-color 0.3s, transform 0.3s;
        }
        .draggable-text:hover {
            background-color: #e0e0e0;
            transform: scale(1.05);
        }
        .drop-area {
            width: 150px;
            height: 50px;
            border: 2px dashed #ccc;
            border-radius: 5px;
            margin: 10px;
            display: inline-block;
            vertical-align: top;
            background-color: #fafafa;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            transition: background-color 0.3s, border-color 0.3s;
        }
        .drop-area:hover {
            background-color: #f0f0f0;
            border-color: #bbb;
        }
        .drop-area.correct {
            background-color: #d4edda;
            border-color: #c3e6cb;
        }
        .drop-area.incorrect {
            background-color: #f8d7da;
            border-color: #f5c6cb;
        }
        #message {
            font-size: 1.2em;
            margin-top: 20px;
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
                event.target.classList.add("correct");
                event.target.classList.remove("incorrect");
                document.getElementById("message").innerText = "Correct!";
            } else {
                event.target.classList.add("incorrect");
                event.target.classList.remove("correct");
                document.getElementById("message").innerText = "Error: Incorrect match.";
            }
        }
    </script>
</body>
</html>
