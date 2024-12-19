---
layout: default
title: "Tile"
category: "Comic"
sub-category: "Security"
---
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Favorite Animal Quiz</title>
    <style>
        .question {
            font-size: 20px;
            margin-bottom: 10px;
        }
        .tile-container {
            display: flex;
            gap: 10px;
            margin-bottom: 20px;
            flex-wrap: wrap; /* Allow wrapping for better layout */
        }
        .tile {
            width: 200px;
            height: 100px;
            display: flex;
            align-items: center;
            justify-content: center;
            background-color: blue;
            color: white;
            border-radius: 10px;
            cursor: pointer;
            transition: transform 0.6s, background-color 0.3s;
            padding: 10px; /* Added padding */
            text-align: center; /* Center text */
            box-sizing: border-box; /* Include padding in size */
            position: relative;
            transform-style: preserve-3d;
        }
        .tile:hover {
            background-color: darkblue;
        }
        .tile .front, .tile .back {
            position: absolute;
            width: 100%;
            height: 100%;
            backface-visibility: hidden;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 10px;
        }
        .tile .back {
            transform: rotateY(180deg);
        }
        .tile.flipped {
            transform: rotateY(180deg);
        }
        .hidden {
            display: none;
        }
    </style>
</head>
<body>
    <div class="question">What is your favorite animal?</div>
    <div class="tile-container">
        <div class="tile" onclick="checkAnswer(this, 'incorrect')">
            <div class="front">Cat</div>
            <div class="back" style="background-color: red;">Incorrect</div>
        </div>
        <div class="tile" onclick="checkAnswer(this, 'incorrect')">
            <div class="front">Bat</div>
            <div class="back" style="background-color: red;">Incorrect</div>
        </div>
        <div class="tile" onclick="checkAnswer(this, 'incorrect')">
            <div class="front">Dog</div>
            <div class="back" style="background-color: red;">Incorrect</div>
        </div>
        <div class="tile" onclick="checkAnswer(this, 'correct')">
            <div class="front">Cow</div>
            <div class="back" style="background-color: green;">Correct</div>
        </div>
    </div>

    <script>
        function checkAnswer(tile, result) {
            if (result === 'correct') {
                tile.querySelector('.back').style.backgroundColor = 'green';
                tile.querySelector('.back').textContent = 'Correct';
            } else {
                tile.querySelector('.back').style.backgroundColor = 'red';
                tile.querySelector('.back').textContent = 'Incorrect';
            }
            tile.classList.add('flipped');
        }
    </script>
</body>
</html>
