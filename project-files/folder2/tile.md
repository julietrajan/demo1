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
        <!-- Question 1 -->
        <div class="tile" onclick="flipTile(this, 'q2')">
            <div class="front">
                <h2>Scenario: Deploying an E-commerce Web Application</h2>
                <p>Which Azure service will you use to host your web application?</p>
            </div>
            <div class="back" id="q1">
                <ul>
                    <li onclick="nextQuestion('q2')">Azure App Service</li>
                    <li onclick="nextQuestion('q2')">Azure Virtual Machines</li>
                    <li onclick="nextQuestion('q2')">Azure Kubernetes Service (AKS)</li>
                    <li onclick="nextQuestion('q2')">Azure Functions</li>
                </ul>
            </div>
        </div>

        <!-- Question 2 -->
        <div class="tile" id="q2" style="display: none;" onclick="flipTile(this, 'q3')">
            <div class="front">
                <h2>How will you secure your Azure App Service?</h2>
            </div>
            <div class="back" id="q3">
                <ul>
                    <li onclick="nextQuestion('q4')">Use Azure Active Directory (AAD) for authentication</li>
                    <li onclick="nextQuestion('q4')">Enable Managed Identity</li>
                    <li onclick="nextQuestion('q4')">Configure SSL/TLS for your app</li>
                    <li onclick="nextQuestion('q4')">Use Azure Key Vault to manage secrets</li>
                </ul>
            </div>
        </div>

        <!-- Question 3 -->
        <div class="tile" id="q3" style="display: none;" onclick="flipTile(this, 'q4')">
            <div class="front">
                <h2>How will you ensure high availability and scalability for your Azure App Service?</h2>
            </div>
            <div class="back" id="q4">
                <ul>
                    <li onclick="nextQuestion('q5')">Enable autoscaling</li>
                    <li onclick="nextQuestion('q5')">Use Traffic Manager for load balancing</li>
                    <li onclick="nextQuestion('q5')">Deploy across multiple regions</li>
                    <li onclick="nextQuestion('q5')">Use Azure Front Door</li>
                </ul>
            </div>
        </div>

        <!-- Additional questions follow the same pattern -->
    </div>

    <script>
        function flipTile(tile, nextQuestionId) {
            tile.classList.toggle('flipped');
            setTimeout(() => {
                document.getElementById(nextQuestionId).style.display = 'block';
            }, 600); // Wait for the flip animation to complete
        }

        function nextQuestion(nextQuestionId) {
            document.getElementById(nextQuestionId).style.display = 'block';
        }
    </script>
</body>
</html>
