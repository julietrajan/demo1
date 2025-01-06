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
    border: 2px solid #0F6CBD;
    display: flex;
    justify-content: center;
    align-items: center;
    transition: transform 0.3s, box-shadow 0.3s;
    border-radius: 15px;
}

.fruits img.selected, .colors div.selected {
    border: 5px solid #0F6CBD;
    box-shadow: 0 0 30px #0F6CBD;
}

.fruits img:hover {
    transform: scale(1.1);
    box-shadow: 0 0 15px rgba(0, 0, 0, 0.5);
}

#message {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    font-size: 24px;
    color: red;
    font-weight: bold;
    display: none; /* Initially hidden */
}
    </style>
</head>
<body>
    <div class="container">
        <div class="fruits">
            <img src="b1.jpeg" alt="Grape" id="grape">
            <img src="bl2.jpeg" alt="Apple" id="apple">
            <img src="b1.jpeg" alt="Banana" id="banana">
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
            selectedFruit.classList.remove('selected');
        }
        selectedFruit = fruit;
        selectedFruit.classList.add('selected');
        checkMatch();
    });
});

document.querySelectorAll('.colors div').forEach(color => {
    color.addEventListener('click', () => {
        if (selectedColor) {
            selectedColor.classList.remove('selected');
        }
        selectedColor = color;
        selectedColor.classList.add('selected');
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
                { color: 'blue', size: 4 }
            );
            document.getElementById('message').innerText = '';
             document.getElementById('message').style.display = 'none';
        } else {
            document.getElementById('message').innerText = 'Oops! Try Again!';
            document.getElementById('message').style.display = 'block';
        }

        selectedFruit.classList.remove('selected');
        selectedColor.classList.remove('selected');
        selectedFruit = null;
        selectedColor = null;
    }
}
    </script>
</body>
</html>
