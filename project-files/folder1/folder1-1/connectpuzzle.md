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

.questions, .answers {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.questions img {
    width: 100px;
    height: 100px;
    margin: 10px;
    cursor: pointer;
    
    display: flex;
    justify-content: center;
    align-items: center;
    transition: transform 0.3s, box-shadow 0.3s;
    border-radius: 15px;
}

.answers div {
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

.questions img.selected, .answers div.selected {
    border: 5px solid #0F6CBD;
    box-shadow: 0 0 30px #0F6CBD;
}

.questions img:hover {
    transform: scale(1.1);
    box-shadow: 0 0 15px rgba(0, 0, 0, 0.5);
}

#message {
    font-size: 24px;
    color: red;
    font-weight: bold;
    display: none; /* Initially hidden */
}
    </style>
</head>
<body>
    <div class="container">
        <div class="questions">
            <img src="b1.jpeg" alt="Grape" id="q1">
            <img src="bl2.jpeg" alt="Apple" id="q2">
            <img src="b1.jpeg" alt="Banana" id="q3">
            <img src="b1.jpeg" alt="Banana" id="q4">
            <img src="b1.jpeg" alt="Banana" id="q5">
        </div>
        <div class="answers">
            <div id="a1">Analyzes the sentiment of the text (positive, negative, neutral)</div>
            <div id="a2">Identifies the language of the input text</div>
            <div id="a3">Links entities in the text to their corresponding entries in a knowledge base</div>
            <div id="a4">Extracts important phrases from the text</div>
            <div id="a5">Identifies and categorizes entities (e.g., people, organizations) in the text</div>
        </div>
    </div>
    <div id="message"></div>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/leader-line/1.0.7/leader-line.min.js"></script>
    <script>

let selectedQuestion = null;
let selectedAnswer = null;

document.querySelectorAll('.questions img').forEach(question => {
    question.addEventListener('click', () => {
        if (selectedQuestion) {
            selectedQuestion.classList.remove('selected');
        }
        selectedQuestion = question;
        selectedQuestion.classList.add('selected');
        checkMatch();
    });
});

document.querySelectorAll('.answers div').forEach(answer => {
    answer.addEventListener('click', () => {
        if (selectedAnswer) {
            selectedAnswer.classList.remove('selected');
        }
        selectedAnswer = answer;
        selectedAnswer.classList.add('selected');
        checkMatch();
    });
});

function checkMatch() {
    if (selectedQuestion && selectedAnswer) {
        let isMatch = false;
        if ((selectedQuestion.id === 'q1' && selectedAnswer.id === 'a2') ||
            (selectedQuestion.id === 'q2' && selectedAnswer.id === 'a4') ||
            (selectedQuestion.id === 'q3' && selectedAnswer.id === 'a1')) ||
            (selectedQuestion.id === 'q4' && selectedAnswer.id === 'a5')) ||
            (selectedQuestion.id === 'q5' && selectedAnswer.id === 'a3')){
            isMatch = true;
        }

        if (isMatch) {
            new LeaderLine(
                document.getElementById(selectedQuestion.id),
                document.getElementById(selectedAnswer.id),
                { color: 'gray', size: 4 }
            );
            document.getElementById('message').innerText = '';
             document.getElementById('message').style.display = 'none';
        } else {
            document.getElementById('message').innerText = 'Oops! Try Again!';
            document.getElementById('message').style.display = 'block';
        }

        selectedQuestion.classList.remove('selected');
        selectedAnswer.classList.remove('selected');
        selectedQuestion = null;
        selectedAnswer = null;
    }
}
    </script>
</body>
</html>
