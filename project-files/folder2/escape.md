---
layout: default
title:  "escape"
category: "Comic"
sub-category: "Security"
---

<html lang="en">
<head>
    <title>Virtual AI Escape Room</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; margin: 20px; }
        .puzzle { display: none; }
        .clue { margin-top: 20px; }
        .puzzle input, .puzzle button { display: block; margin: 10px auto; }
    </style>
</head>
<body>
    <h1>Virtual AI Escape Room</h1>
    <div id="intro">
        <p>Welcome to the Virtual AI Escape Room! Solve the puzzles using your knowledge of Azure OpenAI to escape.</p>
        <button onclick="startEscapeRoom()">Start</button>
    </div>
    <div id="puzzle1" class="puzzle">
        <h2>Chapter 1: The Creative Campaign</h2>
        <p>Which generative AI tool would be most suitable for generating creative content for your marketing campaign?</p>
        <p>A) Azure Cognitive Services<br>B) Azure Open AI services<br>C) Azure Machine Learning<br>D) Azure Data Factory</p>
        <input type="text" id="answer1">
        <button onclick="checkAnswer(1)">Submit</button>
        <button onclick="helpMe(1)">Help Me</button>
        <div class="clue" id="clue1"></div>
    </div>
    <div id="puzzle2" class="puzzle">
        <h2>Chapter 2: Customer Insights</h2>
        <p>Which generative AI model would you use to analyze customer feedback and generate summaries?</p>
        <p>A) BERT<br>B) GPT<br>C) DALL-E<br>D) Azure Synapse Analytics</p>
        <input type="text" id="answer2">
        <button onclick="checkAnswer(2)">Submit</button>
        <button onclick="helpMe(2)">Help Me</button>
        <div class="clue" id="clue2"></div>
    </div>
    <div id="puzzle3" class="puzzle">
        <h2>Chapter 3: The Chatbot Challenge</h2>
        <p>Which Azure service would you choose to implement a chatbot for handling customer queries?</p>
        <p>A) Azure Bot Services<br>B) Azure Open AI services<br>C) Azure Cognitive Search<br>D) Azure Data Lake</p>
        <input type="text" id="answer3">
        <button onclick="checkAnswer(3)">Submit</button>
        <button onclick="helpMe(3)">Help Me</button>
        <div class="clue" id="clue3"></div>
    </div>
    <div id="puzzle4" class="puzzle">
        <h2>Chapter 4: Code Generation</h2>
        <p>Which generative AI model would be most appropriate for generating code snippets?</p>
        <p>A) BERT<br>B) GPT<br>C) DALL-E<br>D) Azure Cognitive Services</p>
        <input type="text" id="answer4">
        <button onclick="checkAnswer(4)">Submit</button>
        <button onclick="helpMe(4)">Help Me</button>
        <div class="clue" id="clue4"></div>
    </div>
    <div id="puzzle5" class="puzzle">
        <h2>Chapter 5: Design Studio</h2>
        <p>Which generative AI model should you use to generate realistic images from text descriptions?</p>
        <p>A) GPT<br>B) BERT<br>C) DALL-E<br>D) Azure Machine Learning</p>
        <input type="text" id="answer5">
        <button onclick="checkAnswer(5)">Submit</button>
        <button onclick="helpMe(5)">Help Me</button>
        <div class="clue" id="clue5"></div>
    </div>
    <div id="puzzle6" class="puzzle">
        <h2>Chapter 6: Data Analysis</h2>
        <p>Which Azure service would be best suited for generating detailed reports from large datasets?</p>
        <p>A) Azure Data Factory<br>B) Azure Synapse Analytics<br>C) Azure Open AI services<br>D) Azure Cognitive Services</p>
        <input type="text" id="answer6">
        <button onclick="checkAnswer(6)">Submit</button>
        <button onclick="helpMe(6)">Help Me</button>
        <div class="clue" id="clue6"></div>
    </div>
    <div id="puzzle7" class="puzzle">
        <h2>Chapter 7: Personalized Content</h2>
        <p>Which Azure service would you use to generate personalized content for a mobile application?</p>
        <p>A) Azure Cognitive Services<br>B) Azure Open AI services<br>C) Azure Machine Learning<br>D) Azure Data Lake</p>
        <input type="text" id="answer7">
        <button onclick="checkAnswer(7)">Submit</button>
        <button onclick="helpMe(7)">Help Me</button>
        <div class="clue" id="clue7"></div>
    </div>
    <div id="puzzle8" class="puzzle">
        <h2>Chapter 8: Document Summarization</h2>
        <p>Which generative AI model would be most effective for generating natural language summaries of technical documents?</p>
        <p>A) BERT<br>B) GPT<br>C) DALL-E<br>D) Azure Cognitive Search</p>
        <input type="text" id="answer8">
        <button onclick="checkAnswer(8)">Submit</button>
        <button onclick="helpMe(8)">Help Me</button>
        <div class="clue" id="clue8"></div>
    </div>
    <div id="finalChallenge" class="puzzle">
        <h2>Final Challenge</h2>
        <p>Combine the clues to solve the final challenge and escape the room!</p>
        <input type="text" id="finalAnswer">
        <button onclick="checkFinalAnswer()">Submit</button>
        <button onclick="helpMe('final')">Help Me</button>
        <div class="clue" id="finalClue"></div>
    </div>

    <script>
        let currentPuzzle = 1;
        const clues = ["Azure Open AI services", "GPT", "Azure Bot Services", "GPT", "DALL-E", "Azure Synapse Analytics", "Azure Open AI services", "GPT"];
        const correctAnswers = ["b", "b", "a", "b", "c", "b", "b", "b"];

        function startEscapeRoom() {
            document.getElementById('intro').style.display = 'none';
            showPuzzle(currentPuzzle);
        }

        function showPuzzle(puzzleNumber) {
            document.getElementById(`puzzle${puzzleNumber}`).style.display = 'block';
        }

        function checkAnswer(puzzleNumber) {
            const answer = document.getElementById(`answer${puzzleNumber}`).value.toLowerCase();
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

        function helpMe(puzzleNumber) {
            if (puzzleNumber === 'final') {
                document.getElementById('finalAnswer').value = 'azure open ai services gpt azure bot services gpt dall-e azure synapse analytics azure open ai services gpt';
            } else {
                document.getElementById(`answer${puzzleNumber}`).value = correctAnswers[puzzleNumber - 1];
            }
        }

        function checkFinalAnswer() {
            const finalAnswer = document.getElementById('finalAnswer').value.toLowerCase();
            const finalClueElement = document.getElementById('finalClue');

            if (finalAnswer === 'azure open ai services gpt azure bot services gpt dall-e azure synapse analytics azure open ai services gpt') {
                finalClueElement.textContent = 'Congratulations! You have escaped the room!';
            } else {
                finalClueElement.textContent = 'Incorrect, try again!';
            }
        }
    </script>
</body>
</html>
