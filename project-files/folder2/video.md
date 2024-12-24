---
layout: default
title: "video1"
category: "Comic"
sub-category: "Security"
---
{% raw %}
<h1>Hangman Game</h1>
<p>Guess the word by selecting the letters. You have 6 attempts!</p>

<div id="hangman-game">
    <p id="word"></p>
    <p id="message"></p>
    <div id="letters"></div>
    <p>Attempts left: <span id="attempts">6</span></p>
    <button onclick="resetGame()">Reset Game</button>
</div>

<script>
    const words = ["javascript", "jekyll", "github", "markdown", "hangman"];
    let selectedWord = words[Math.floor(Math.random() * words.length)];
    let attempts = 6;
    let guessedLetters = [];

    function displayWord() {
        const wordDisplay = selectedWord.split('').map(letter => guessedLetters.includes(letter) ? letter : '_').join(' ');
        document.getElementById('word').innerText = wordDisplay;
    }

    function displayLetters() {
        const letters = 'abcdefghijklmnopqrstuvwxyz'.split('');
        const lettersContainer = document.getElementById('letters');
        lettersContainer.innerHTML = '';
        letters.forEach(letter => {
            const button = document.createElement('button');
            button.innerText = letter;
            button.onclick = () => guessLetter(letter);
            lettersContainer.appendChild(button);
        });
    }

    function guessLetter(letter) {
        if (guessedLetters.includes(letter) || attempts === 0) return;
        guessedLetters.push(letter);
        if (!selectedWord.includes(letter)) {
            attempts--;
            document.getElementById('attempts').innerText = attempts;
        }
        displayWord();
        checkGameStatus();
    }

    function checkGameStatus() {
        const wordDisplay = document.getElementById('word').innerText;
        if (!wordDisplay.includes('_')) {
            document.getElementById('message').innerText = 'Congratulations! You guessed the word!';
            disableButtons();
        } else if (attempts === 0) {
            document.getElementById('message').innerText = `Game Over! The word was "${selectedWord}".`;
            disableButtons();
        }
    }

    function disableButtons() {
        const buttons = document.querySelectorAll('#letters button');
        buttons.forEach(button => button.disabled = true);
    }

    function resetGame() {
        selectedWord = words[Math.floor(Math.random() * words.length)];
        attempts = 6;
        guessedLetters = [];
        document.getElementById('attempts').innerText = attempts;
        document.getElementById('message').innerText = '';
        displayWord();
        displayLetters();
    }

    // Initialize game
    displayWord();
    displayLetters();
</script>

<style>
    #letters button {
        margin: 5px;
        padding: 10px;
        font-size: 16px;
    }
    #word {
        font-size: 24px;
        letter-spacing: 10px;
    }
    #message {
        font-size: 20px;
        color: green;
    }
</style>
{% endraw %}
