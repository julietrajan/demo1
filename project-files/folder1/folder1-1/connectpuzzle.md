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

.fruits img, .colors div {
    width: 100px;
    height: 100px;
    margin: 10px;
    cursor: pointer;
    border: 2px solid #000;
    display: flex;
    justify-content: center;
    align-items: center;
}
    </style>
</head>
<body>
    <div class="container">
        <div class="fruits">
            <img src="apple.png" alt="Apple" id="apple">
            <img src="banana.png" alt="Banana" id="banana">
            <img src="grape.png" alt="Grape" id="grape">
        </div>
        <div class="colors">
            <div id="red">Red</div>
            <div id="yellow">Yellow</div>
            <div id="purple">Purple</div>
        </div>
    </div>
    <div id="message"></div>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/leader-line/1.0.7/leader-line.min.js"></script>
    <script>
        let selectedFruit = null;
let selectedColor = null;

document.querySelectorAll('.fruits img').forEach(fruit => {
    fruit.addEventListener('click', () => {
        if (selectedFruit) {
            selectedFruit.style.border = '2px solid #000';
        }
        selectedFruit = fruit;
        selectedFruit.style.border = '2px solid blue';
        checkMatch();
    });
});

document.querySelectorAll('.colors div').forEach(color => {
    color.addEventListener('click', () => {
        if (selectedColor) {
            selectedColor.style.border = '2px solid #000';
        }
        selectedColor = color;
        selectedColor.style.border = '2px solid blue';
        checkMatch();
    });
});

function checkMatch() {
    if (selectedFruit && selectedColor) {
        let isMatch = false;
        if ((selectedFruit.id === 'apple' && selectedColor.id === 'red') ||
            (selectedFruit.id === 'banana' && selectedColor.id === 'yellow') ||
            (selectedFruit.id === 'grape' && selectedColor.id === 'purple')) {
            isMatch = true;
        }

        if (isMatch) {
            new LeaderLine(
                document.getElementById(selectedFruit.id),
                document.getElementById(selectedColor.id),
                { color: 'green', size: 4 }
            );
            document.getElementById('message').innerText = '';
        } else {
            document.getElementById('message').innerText = 'Error: Incorrect match!';
        }

        selectedFruit.style.border = '2px solid #000';
        selectedColor.style.border = '2px solid #000';
        selectedFruit = null;
        selectedColor = null;
    }
}
    </script>
</body>
</html>
