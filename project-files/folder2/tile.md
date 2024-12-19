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
    <title>Azure Learning Tiles</title>
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
            width: 250px; /* Increased width */
            height: 150px; /* Increased height */
            display: flex;
            align-items: center;
            justify-content: center;
            background-color: blue;
            color: white;
            border-radius: 10px;
            cursor: pointer;
            transition: background-color 0.3s;
            padding: 10px; /* Added padding */
            text-align: center; /* Center text */
            box-sizing: border-box; /* Include padding in size */
        }
        .tile:hover {
            background-color: darkblue;
        }
        .hidden {
            display: none;
        }
    </style>
</head>
<body>
    <div id="question1" class="question-container">
        <div class="question">Which Azure service will you use to host your web application?</div>
        <div class="tile-container">
            <div class="tile" onclick="showNextQuestion('question2')">Azure App Service</div>
            <div class="tile" onclick="showNextQuestion('question2')">Azure Virtual Machines</div>
            <div class="tile" onclick="showNextQuestion('question2')">Azure Kubernetes Service (AKS)</div>
            <div class="tile" onclick="showNextQuestion('question2')">Azure Functions</div>
        </div>
    </div>

    <div id="question2" class="question-container hidden">
        <div class="question">How will you secure your Azure App Service?</div>
        <div class="tile-container">
            <div class="tile" onclick="showNextQuestion('question3')">Use Azure Active Directory (AAD) for authentication</div>
            <div class="tile" onclick="showNextQuestion('question3')">Enable Managed Identity</div>
            <div class="tile" onclick="showNextQuestion('question3')">Configure SSL/TLS for your app</div>
            <div class="tile" onclick="showNextQuestion('question3')">Use Azure Key Vault to manage secrets</div>
        </div>
    </div>

    <div id="question3" class="question-container hidden">
        <div class="question">How will you ensure high availability and scalability for your Azure App Service?</div>
        <div class="tile-container">
            <div class="tile" onclick="showNextQuestion('question4')">Enable autoscaling</div>
            <div class="tile" onclick="showNextQuestion('question4')">Use Traffic Manager for load balancing</div>
            <div class="tile" onclick="showNextQuestion('question4')">Deploy across multiple regions</div>
            <div class="tile" onclick="showNextQuestion('question4')">Use Azure Front Door</div>
        </div>
    </div>

    <script>
        function showNextQuestion(nextQuestionId) {
            document.querySelectorAll('.question-container').forEach(container => {
                container.classList.add('hidden');
            });
            document.getElementById(nextQuestionId).classList.remove('hidden');
        }
    </script>
</body>
</html>
