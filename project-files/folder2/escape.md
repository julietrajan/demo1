---
layout: default
title:  "escape"
category: "Comic"
sub-category: "Security"
---

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Virtual AI Escape Room</title>
    <style>
        .room { 
            font-family: Arial, sans-serif; 
            text-align: center; 
            margin: 20px; 
            background-color: #2c3e50; 
            color: #ecf0f1; 
        }
        h1, h2 {
            color: #e74c3c;
        }
        .puzzle { 
            display: none; 
            background-color: #34495e; 
            padding: 20px; 
            border-radius: 10px; 
            margin-bottom: 20px; 
        }
        .clue { 
            margin-top: 20px; 
            font-weight: bold; 
        }
        .puzzle input[type="radio"], .puzzle button { 
            margin: 10px auto; 
        }
        button {
            background-color: #e74c3c; 
            color: #ecf0f1; 
            border: none; 
            padding: 10px 20px; 
            border-radius: 5px; 
            cursor: pointer; 
        }
        button:hover {
            background-color: #c0392b;
        }
        #intro {
            background-color: #34495e; 
            padding: 20px; 
            border-radius: 10px; 
        }
    </style>
</head>
<body>
    <div class="room">
    <h1>Virtual AI Escape Room</h1>
    <div id="intro">
        <p>Welcome to the Virtual AI Escape Room! Solve the puzzles using your knowledge of Azure OpenAI to escape.</p>
        <button onclick="startEscapeRoom()">Start</button>
    </div>
    <div id="puzzle1" class="puzzle">
        <h2>Chapter 1: The Creative Campaign</h2>
        <p>Which generative AI tool would be most suitable for generating creative content for your marketing campaign?</p>
        <label><input type="radio" name="answer1" value="a"> A) Azure Cognitive Services</label>
        <label><input type="radio" name="answer1" value="b"> B) Azure Open AI services</label>
        <label><input type="radio" name="answer1" value="c"> C) Azure Machine Learning</label>
        <label><input type="radio" name="answer1" value="d"> D) Azure Data Factory</label>
        <button onclick="checkAnswer(1)">Submit</button>
        <button onclick="helpMe(1)">Help Me</button>
        <div class="clue" id="clue1"></div>
    </div>
    <div id="puzzle2" class="puzzle">
        <h2>Chapter 2: Customer Insights</h2>
        <p>Which generative AI model would you use to analyze customer feedback and generate summaries?</p>
        <label><input type="radio" name="answer2" value="a"> A) BERT</label>
        <label><input type="radio" name="answer2" value="b"> B) GPT</label>
        <label><input type="radio" name="answer2" value="c"> C) DALL-E</label>
        <label><input type="radio" name="answer2" value="d"> D) Azure Synapse Analytics</label>
        <button onclick="checkAnswer(2)">Submit</button>
        <button onclick="helpMe(2)">Help Me</button>
        <div class="clue" id="clue2"></div>
    </div>
    <div id="puzzle3" class="puzzle">
        <h2>Chapter 3: The Chatbot Challenge</h2>
        <p>Which Azure service would you choose to implement a chatbot for handling customer queries?</p>
        <label><input type="radio" name="answer3" value="a"> A) Azure Bot Services</label>
        <label><input type="radio" name="answer3" value="b"> B) Azure Open AI services</label>
        <label><input type="radio" name="answer3" value="c"> C) Azure Cognitive Search</label>
        <label><input type="radio" name="answer3" value="d"> D) Azure Data Lake</label>
        <button onclick="checkAnswer(3)">Submit</button>
        <button onclick="helpMe(3)">Help Me</button>
        <div class="clue" id="clue3"></div>
    </div>
    <div id="puzzle4" class="puzzle">
        <h2>Chapter 4: Code Generation</h2>
        <p>Which generative AI model would be most appropriate for generating code snippets?</p>
        <label><input type="radio" name="answer4" value="a"> A) BERT</label>
        <label><input type="radio" name="answer4" value="b"> B) GPT</label>
        <label><input type="radio" name="answer4" value="c"> C) DALL-E</label>
        <label><input type="radio" name="answer4" value="d"> D) Azure Cognitive Services</label>
        <button onclick="checkAnswer(4)">Submit</button>
        <button onclick="helpMe(4)">Help Me</button>
        <div class="clue" id="clue4"></div>
    </div>
    <div id="puzzle5" class="puzzle">
        <h2>Chapter 5: Design Studio</h2>
        <p>Which generative AI model should you use to generate realistic images from text descriptions?</p>
        <label><input type="radio" name="answer5" value="a"> A) GPT</label>
        <label><input type="radio" name="answer5" value="b"> B) BERT</label>
        <label><input type="radio" name="answer5" value="c"> C) DALL-E</label>
        <label><input type="radio" name="answer5" value="d"> D) Azure Machine Learning</label>
        <button onclick="checkAnswer(5)">Submit</button>
        <button onclick="helpMe(5)">Help Me</button>
        <div class="clue" id="clue5"></div>
    </div>
    <div id="puzzle6" class="puzzle">
        <h2>Chapter 6: Data Analysis</h2>
        <p>Which Azure service would be best suited for generating detailed reports from large datasets?</p>
        <label><input type="radio" name="answer6" value="a"> A) Azure Data Factory</label>
        <label><input type="radio" name="answer6" value="b"> B) Azure Synapse Analytics</label>
        <label><input type="radio" name="answer6" value="c"> C) Azure Open AI services</label>
        <label><input type="radio" name="answer6" value="d"> D) Azure Cognitive Services</label>
        <button onclick="checkAnswer(6)">Submit</button>
        <button onclick="helpMe(6)">Help Me</button>
        <div class="clue" id="clue6"></div>
    </div>
    <div id="puzzle7" class="puzzle">
        <h2>Chapter 7: Personalized Content</h2>
        <p>Which Azure service would you use to generate personalized content for a mobile application?</p>
        <label><input type="radio" name="answer7" value="a"> A) Azure Cognitive Services</label>
        <label><input type="radio" name="answer7" value="b"> B) Azure Open AI services</label>
        <label><input type="radio" name="answer7" value="c"> C) Azure Machine Learning</label>
        <label><input type="radio" name="answer7" value="d"> D) Azure Data Lake</label>
        <button onclick="checkAnswer(7)">Submit</button>
        <button onclick="helpMe(7)">Help Me</button>
        <div class="clue" id="clue7"></div>
    </div>
    <div id="puzzle8" class="puzzle">
        <h2>Chapter 8: Document Summarization</h2>
        <p>Which generative AI model would be most effective for generating natural language summaries of technical documents?</p>
        <label><input type="radio" name="answer8" value="a"> A) BERT</label>
        <label><input type="radio" name="answer8" value="b"> B) GPT</label>
        <label><input type="radio" name="answer8" value="c"> C) DALL-E</label>
        <label><input type="radio" name="answer8" value="d"> D) Azure Cognitive Search</label>
        <button onclick="checkAnswer(8)">Submit</button>
        <button onclick="helpMe(8)">Help Me</button>
        <div class="clue" id="clue8"></div>
    </div>
    <div id="finalChallenge" class="puzzle">
    <h2>Final Challenge: The Ultimate Test</h2>
    <p>To complete your mission, you need to demonstrate your understanding of prompt engineering. Fill in the blank to complete the statement:</p>
    <p>Effective prompt engineering involves crafting prompts that are clear, concise, and provide sufficient </p>
    <input type="text" id="finalAnswer" style="display: block; margin: 10px auto;">
    <button onclick="checkFinalAnswer()">Submit</button>
    <button onclick="helpMe('final')">Help Me</button>
    <div class="clue" id="finalClue"></div>
    </div>
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
        const selectedOption = document.querySelector(`input[name="answer${puzzleNumber}"]:checked`);
        const clueElement = document.getElementById(`clue${puzzleNumber}`);

        if (selectedOption && selectedOption.value === correctAnswers[puzzleNumber - 1]) {
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
            document.getElementById('finalAnswer').value = 'context';
        } else {
            document.querySelector(`input[name="answer${puzzleNumber}"][value="${correctAnswers[puzzleNumber - 1]}"]`).checked = true;
        }
    }

    function checkFinalAnswer() {
        const finalAnswer = document.getElementById('finalAnswer').value.toLowerCase();
        const finalClueElement = document.getElementById('finalClue');

        if (finalAnswer === 'context') {
            finalClueElement.textContent = 'Congratulations! You have escaped the room!';
        } else {
            finalClueElement.textContent = 'Incorrect, try again!';
        }
    }
</script>
</body>
</html>
