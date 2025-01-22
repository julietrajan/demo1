---
layout: default
title:  "escape"
category: "Comic"
sub-category: "Security"
---


<html lang="en">
<head>


    <style>
        body { font-family: Arial, sans-serif; text-align: center; margin: 20px; }
        .puzzle { display: none; }
        .clue { margin-top: 20px; }
    </style>
</head>
<body>
    <h1>Virtual AI Escape Room</h1>
    <div id="intro">
        <p>Welcome to the Virtual AI Escape Room! Solve the puzzles using your knowledge of Azure OpenAI to escape.</p>
        <button onclick="startEscapeRoom()">Start</button>
    </div>
   puzzle">
        <h2>Puzzle 1</h2>
        <p>What is the primary use of Azure OpenAI?</p>
        <input type="text" id="answer1">
        <button onclick="checkAnswer(1)">Submit</button>
        <div class="clue" id="clue1"></div>
    </div>
    <div id="puzzle2" class="puzzle">
        <h2>Puzzle 2</h2>
        <p>Which Azure OpenAI feature can analyze text sentiment?</p>
        <input type="text" id="answer2">
        <button onclick="checkAnswer(2)">Submit</button>
        <div class="clue" id="clue2"></div>
    </div>
    <div id="finalChallenge" class="puzzle">
        <h2>Final Challenge</h2>
        <p>Combine the clues to solve the final challenge and escape the room!</p>
        <input type="text" id="finalAnswer">
        <button onclick="checkFinalAnswer()">Submit</button>
        <div class="clue" id="finalClue"></div>
    </div>

    <script>
    let currentPuzzle = 1;
    const clues = ["AI Tools", "Sentiment Analysis"];

    function startEscapeRoom() {
        document.getElementById('intro').style.display = 'none';
        showPuzzle(currentPuzzle);
    }

    function showPuzzle(puzzleNumber) {
        document.getElementById(`puzzle${puzzleNumber}`).style.display = 'block';
    }

    function checkAnswer(puzzleNumber) {
        const answer = document.getElementById(`answer${puzzleNumber}`).value.toLowerCase();
        const correctAnswers = ["ai tools", "sentiment analysis"];
        const clueElement = document.getElementById(`clue${puzzleNumber}`);

        if (answer === correctAnswers[puzzleNumber - 1]) {
            clueElement.textContent = `Correct! Clue: ${clues[puzzleNumber - 1]}`;
            currentPuzzle++;
            if (currentPuzzle <= clues.length) {
                setTimeout(() => {
                    document.getElementById(`puzzle${puzzleNumber}`).style.display = 'none';
                    showPuzzle(currentPuzzle);
                }, 1000);
            } else {
                setTimeout(() => {
                    document.getElementById(`puzzle${puzzleNumber}`).style.display = 'none';
                    document.getElementById('finalChallenge').style.display = 'block';
                }, 1000);
            }
        } else {
            clueElement.textContent = 'Incorrect, try again!';
        }
    }

    function checkFinalAnswer() {
        const finalAnswer = document.getElementById('finalAnswer').value.toLowerCase();
        const finalClueElement = document.getElementById('finalClue');

        if (finalAnswer === 'ai tools sentiment analysis') {
            finalClueElement.textContent = 'Congratulations! You have escaped the room!';
        } else {
            finalClueElement.textContent = 'Incorrect, try again!';
        }
    }
</script>
</body>
</html>
