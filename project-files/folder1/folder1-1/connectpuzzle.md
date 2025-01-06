---
layout: default
title:  "connect puzzle"
category: "Case Study"
sub-category: "Security"
courses: [SC-200,SC-300, AZ-500]
---

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fruit Color Matching Game</title>
    <style>
      body {
    font-family: Arial, sans-serif;
}

.container {
    display: flex;
    justify-content: space-around;
    margin-top: 50px;
}

.fruits, .colors {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.fruits img {
    width: 100px;
    height: 100px; /* Ensures all images are the same size */
    margin: 10px;
    cursor: pointer;
}

.colors div {
    width: 100px;
    height: 100px; /* Ensures all color divs are the same size */
    margin: 10px;
    display: flex;
    justify-content: center;
    align-items: center;
    border: 2px solid #000;
    cursor: pointer;
}
    </style>
</head>
<body>
    <div class="container">
        <div class="fruits">
            <img src="b1.jpg" alt="Apple" id="apple" draggable="true" ondragstart="drag(event)">
            <img src="b1.jpeg" alt="Banana" id="banana" draggable="true" ondragstart="drag(event)">
            <img src="bl2.jpeg" alt="Grape" id="grape" draggable="true" ondragstart="drag(event)">
        </div>
        <div class="colors">
            <div id="red" ondrop="drop(event)" ondragover="allowDrop(event)">Red</div>
            <div id="yellow" ondrop="drop(event)" ondragover="allowDrop(event)">Yellow</div>
            <div id="purple" ondrop="drop(event)" ondragover="allowDrop(event)">Purple</div>
        </div>
    </div>
    <div id="message"></div>
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
    var fruit = document.getElementById(data);
    var color = event.target.id;

    if ((fruit.id === "apple" && color === "red") ||
        (fruit.id === "banana" && color === "yellow") ||
        (fruit.id === "grape" && color === "purple")) {
        event.target.appendChild(fruit);
        document.getElementById("message").innerText = "";
    } else {
        document.getElementById("message").innerText = "Error: Incorrect match!";
    }
}
    </script>
</body>
</html>

