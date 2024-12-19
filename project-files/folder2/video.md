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
    <title>Scenario-Based Learning Tile</title>
    <style>
        .tile-container {
            perspective: 1000px;
        }
        .tile {
            width: 300px;
            height: 200px;
            position: relative;
            transform-style: preserve-3d;
            transition: transform 0.6s;
            cursor: pointer;
            border-radius: 15px;
            margin: 20px;
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
            font-size: 18px;
            border-radius: 15px;
            padding: 20px;
            box-sizing: border-box;
        }
        .tile .front {
            background-color: blue;
        }
        .tile .back {
            background-color: green;
            transform: rotateY(180deg);
            text-align: left;
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
                <h2>Scenario: Scaling an Application</h2>
            </div>
            <div class="back">
                <p>Your web application is experiencing increased traffic. Choose the best scaling strategy:</p>
                <ul>
                    <li>Option 1: Scale up (increase the size of the VM)</li>
                    <li>Option 2: Scale out (add more VMs)</li>
                    <li>Option 3: Use Azure Autoscale</li>
                </ul>
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
