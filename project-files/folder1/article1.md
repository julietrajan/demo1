---
layout: default
title:  "Need for MFA"
category: "Case Study"
sub-category: "Security"
courses: [SC-200,SC-300, AZ-500]
---

Tips for Trainers: Play this comic-style play, scene-by-scene, while asking questions in between scenes to initiate classroom discussions.

Characters Intro: This is a conversation between Alice - a program manager and John - a security consultant, over the mandatory multifactor authentication for Azure Sign-in in Contoso.

<!DOCTYPE html>
<html>
<head>
  <title>Azure Synapse Crossword Puzzle</title>
  <style>
    body {
      font-family: Arial, sans-serif;
    }
    .grid {
      display: grid;
      grid-template-columns: repeat(9, 40px);
      grid-template-rows: repeat(9, 40px);
      gap: 5px;
    }
    .cell {
      width: 40px;
      height: 40px;
      border: 1px solid #ddd;
      text-align: center;
      font-size: 16px;
      font-weight: bold;
      position: relative;
    }
    .cell input {
      width: 100%;
      height: 100%;
      border: none;
      text-align: center;
      font-size: 16px;
      font-weight: bold;
      text-transform: uppercase;
    }
    .cell input.incorrect {
      background-color: red;
      color: white;
    }
    .buttons {
      margin: 20px 0;
    }
    button {
      margin-right: 10px;
      padding: 10px 15px;
      font-size: 16px;
    }
    .clue-number {
      position: absolute;
      top: 2px;
      left: 2px;
      font-size: 12px;
      color: gray;
    }
  </style>
</head>
<body>
  <h1>Azure Synapse Crossword Puzzle</h1>
  <p>Complete the crossword puzzle by answering the clues below. Click "Check" to validate your answers or "Help Me" to reveal them.</p>

  <div class="grid">
    <!-- Row 1 -->
    <div class="cell"><input maxlength="1" data-answer="S"><span class="clue-number">1</span></div>
    <div class="cell"><input maxlength="1" data-answer="Q"></div>
    <div class="cell"><input maxlength="1" data-answer="L"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"><input maxlength="1" data-answer="S"><span class="clue-number">3</span></div>
    <div class="cell"><input maxlength="1" data-answer="P"></div>

    <!-- Row 2 -->
    <div class="cell"><input maxlength="1" data-answer="P"><span class="clue-number">2</span></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"><input maxlength="1" data-answer="A"></div>
    <div class="cell"><input maxlength="1" data-answer="R"></div>
    <div class="cell"><input maxlength="1" data-answer="K"></div>

    <!-- Row 3 -->
    <div class="cell"><input maxlength="1" data-answer="A"><span class="clue-number">4</span></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>

    <!-- Row 4 -->
    <div class="cell"><input maxlength="1" data-answer="R"></div>
    <div class="cell"><input maxlength="1" data-answer="T"></div>
    <div class="cell"><input maxlength="1" data-answer="H"></div>
    <div class="cell"><input maxlength="1" data-answer="Q"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"><input maxlength="1" data-answer="S"></div>
    <div class="cell"></div>
    <div class="cell"></div>

    <!-- Row 5 -->
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"><input maxlength="1" data-answer="B"><span class="clue-number">5</span></div>
    <div class="cell"><input maxlength="1" data-answer="L"></div>
    <div class="cell"><input maxlength="1" data-answer="O"></div>
    <div class="cell"><input maxlength="1" data-answer="B"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>

    <!-- Row 6 -->
    <div class="cell"><input maxlength="1" data-answer="N"></div>
    <div class="cell"><input maxlength="1" data-answer="O"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"><input maxlength="1" data-answer="I"><span class="clue-number">6</span></div>
    <div class="cell"></div>

    <!-- Row 7 -->
    <div class="cell"><input maxlength="1" data-answer="S"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"><input maxlength="1" data-answer="Y"><span class="clue-number">7</span></div>
    <div class="cell"><input maxlength="1" data-answer="N"></div>
    <div class="cell"><input maxlength="1" data-answer="A"></div>
    <div class="cell"><input maxlength="1" data-answer="P"></div>

    <!-- Row 8 -->
    <div class="cell"></div>
    <div class="cell"><input maxlength="1" data-answer="S"><span class="clue-number">8</span></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"><input maxlength="1" data-answer="B"></div>
    <div class="cell"><input maxlength="1" data-answer="I"></div>
    <div class="cell"></div>
    <div class="cell"></div>
  </div>

  <div class="buttons">
    <button id="checkButton">Check</button>
    <button id="helpButton">Help Me</button>
  </div>

  <h2>Clues</h2>
  <h3>Across</h3>
  <ul>
    <li><strong>1:</strong> SQL</li>
    <li><strong>3:</strong> Spark</li>
    <li><strong>5:</strong> Blob</li>
    <li><strong>7:</strong> Synapse</li>
    <li><strong>9:</strong> Big Data</li>
  </ul>
  <h3>Down</h3>
  <ul>
    <li><strong>1:</strong> Spark</li>
    <li><strong>2:</strong> Serverless</li>
    <li><strong>4:</strong> ML</li>
    <li><strong>6:</strong> Hybrid</li>
    <li><strong>8:</strong> SQL</li>
  </ul>

  <script>
    document.getElementById('checkButton').addEventListener('click', () => {
      const cells = document.querySelectorAll('.cell input');
      cells.forEach(cell => {
        if (cell.dataset.answer && cell.value.toUpperCase() !== cell.dataset.answer) {
          cell.classList.add('incorrect');
        } else {
          cell.classList.remove('incorrect');
        }
      });
    });

    document.getElementById('helpButton').addEventListener('click', () => {
      const cells = document.querySelectorAll('.cell input');
      cells.forEach(cell => {
        if (cell.dataset.answer) {
          cell.value = cell.dataset.answer;
          cell.classList.remove('incorrect');
        }
      });
    });
  </script>
</body>
</html>
