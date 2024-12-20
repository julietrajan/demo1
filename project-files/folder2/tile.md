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
    <title>Favorite Azure Service Quiz</title>
    <style>
        .question {
            font-size: 20px;
            margin-bottom: 10px;
        }
        .tile-container {
            display: flex;
            gap: 40px;
            margin-bottom: 20px;
            flex-wrap: wrap; /* Allow wrapping for better layout */
            justify-content: center; /* Center the tiles */
        }
        .tile {
            width: 300px;
            height: 400px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(135deg, #e0f7fa, #80deea);
            color: white;
            border-radius: 40px;
            cursor: pointer;
            transition: transform 0.6s, background-color 0.3s;
            padding: 10px; /* Added padding */
            text-align: center; /* Center text */
            box-sizing: border-box; /* Include padding in size */
            position: relative;
            transform-style: preserve-3d;
            margin-bottom: 20px; /* Add margin for spacing */
        }
        .tile:hover {
            background: linear-gradient(135deg, #b2ebf2, #4dd0e1);
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
    <div class="question">What is your favorite Azure service?</div>
    <div class="tile-container">
        <div class="tile" onclick="checkAnswer(this, 'Azure Virtual Machines (VMs)')">
            <div class="front">Clue: This service provides scalable, on-demand computing resources with full control over the operating system and applications, similar to having your own physical server in the cloud.</div>
            <div class="back">Azure Virtual Machines (VMs)</div>
        </div>
        <div class="tile" onclick="checkAnswer(this, 'Azure App Service')">
            <div class="front">Clue: This fully managed platform allows you to build, deploy, and scale web apps and APIs quickly, supporting multiple languages and frameworks with built-in CI/CD.</div>
            <div class="back">Azure App Service</div>
        </div>
        <div class="tile" onclick="checkAnswer(this, 'Azure Kubernetes Service (AKS)')">
            <div class="front">Clue: This service offers a managed Kubernetes environment for deploying, managing, and scaling containerized applications using open-source Kubernetes.</div>
            <div class="back">Azure Kubernetes Service (AKS)</div>
        </div>
        <div class="tile" onclick="checkAnswer(this, 'Azure Container Instances (ACI)')">
            <div class="front">Clue: This service enables you to run containers on Azure without managing virtual machines or having to adopt a higher-level service, providing a quick and easy way to deploy containers.</div>
            <div class="back">Azure Container Instances (ACI)</div>
        </div>
        <div class="tile" onclick="checkAnswer(this, 'Azure Functions')">
            <div class="front">Clue: This serverless compute service allows you to run event-driven code without provisioning or managing infrastructure, charging you only for the time your code runs.</div>
            <div class="back">Azure Functions</div>
        </div>
        <div class="tile" onclick="checkAnswer(this, 'Azure Logic Apps')">
            <div class="front">Clue: This service helps you automate workflows and integrate apps, data, and services across organizations using a visual designer and pre-built connectors.</div>
            <div class="back">Azure Logic Apps</div>
        </div>
    </div>

    <script>
        function checkAnswer(tile, answer) {
            if (tile.classList.contains('flipped')) {
                tile.classList.remove('flipped');
                setTimeout(() => {
                    tile.querySelector('.back').style.backgroundColor = '';
                    tile.querySelector('.back').textContent = '';
                }, 600); // Wait for the flip animation to complete
            } else {
                tile.querySelector('.back').style.backgroundColor = 'green';
                tile.querySelector('.back').textContent = answer;
                tile.classList.add('flipped');
            }
        }
    </script>
</body>
</html>
