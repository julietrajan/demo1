---
layout: default
title: "video"
category: "Comic"
sub-category: "Security"
---
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flipping Tile</title>
    <style>
        .tile-container {
            perspective: 1000px;
        }
        .tile {
            width: 300px; /* Increased width */
            height: 150px; /* Increased height */
            position: relative;
            transform-style: preserve-3d;
            transition: transform 0.6s;
            cursor: pointer;
            border-radius: 15px; /* Rounded edges */
        }
        .tile .front, .tile .back {
            position: absolute;
            width: 100%;
            height: 100%;
            backface-visibility: hidden;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 20px;
            border-radius: 15px; /* Rounded edges */
        }
        .tile .front {
            background-color: blue;
        }
        .tile .back {
            background-color: green;
            transform: rotateY(180deg);
        }
        .tile.flipped {
            transform: rotateY(180deg);
        }
    </style>
</head>
<body>
    <div class="tile-container">
        <div class="tile" onclick="flipTile(this)">
            <div class="front">
                <h2>Click Me!</h2>
            </div>
            <div class="back">
                <h2>Flipped Side</h2>
            </div>
        </div>
    </div>

    <script>
        function flipTile(tile) {
            tile.classList.toggle('flipped');
        }
    </script>
</body>
</html>
