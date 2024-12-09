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
      grid-template-columns: repeat(10, 40px);
      grid-template-rows: repeat(10, 40px);
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
    <div class="cell"><input maxlength="1" data-answer="S"><span class="clue-number">3</span></div>
    <div class="cell"><input maxlength="1" data-answer="P"></div>
    <div class="cell"><input maxlength="1" data-answer="A"></div>
    <div class="cell"><input maxlength="1" data-answer="R"></div>
    
    <!-- Row 2 -->
    <div class="cell"><input maxlength="1" data-answer="N"><span class="clue-number">1</span></div>
    <div class="cell"><input maxlength="1" data-answer="O"></div>
    <div class="cell"><input maxlength="1" data-answer="T"></div>
    <div class="cell"><input maxlength="1" data-answer="E"></div>
    <div class="cell"><input maxlength="1" data-answer="B"></div>

    <div class="cell"><input maxlength="1" data-answer="O"></div>
    <div class="cell"><input maxlength="1" data-answer="O"></div>
    <div class="cell"><input maxlength="1" data-answer="K"></div>
    <div class="cell"></div>
    <div class="cell"></div>

    <!-- Row 3 -->
    <div class="cell"><input maxlength="1" data-answer="B"><span class="clue-number">5</span></div>
    <div class="cell"><input maxlength="1" data-answer="L"></div>
    <div class="cell"><input maxlength="1" data-answer="O"></div>
    <div class="cell"><input maxlength="1" data-answer="B"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>

    <!-- Row 4 -->
    <div class="cell"></div>
    <div class="cell"><input maxlength="1" data-answer="B"><span class="clue-number">2</span></div>
    <div class="cell"><input maxlength="1" data-answer="I"></div>
    <div class="cell"><input maxlength="1" data-answer="G"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>

    <!-- Row 5 -->
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"><input maxlength="1" data-answer="A"><span class="clue-number">4</span></div>
    <div class="cell"><input maxlength="1" data-answer="U"></div>
    <div class="cell"><input maxlength="1" data-answer="T"></div>
    <div class="cell"><input maxlength="1" data-answer="O"></div>
    <div class="cell"><input maxlength="1" data-answer="S"></div>
    <div class="cell"></div>

    <!-- Row 6 -->
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"><input maxlength="1" data-answer="S"><span class="clue-number">6</span></div>
    <div class="cell"><input maxlength="1" data-answer="E"></div>
    <div class="cell"><input maxlength="1" data-answer="R"></div>
    <div class="cell"><input maxlength="1" data-answer="V"></div>
    <div class="cell"><input maxlength="1" data-answer="E"></div>

    <!-- Row 7 -->
    <div class="cell"><input maxlength="1" data-answer="D"><span class="clue-number">7</span></div>
    <div class="cell"><input maxlength="1" data-answer="A"></div>
    <div class="cell"><input maxlength="1" data-answer="T"></div>
    <div class="cell"><input maxlength="1" data-answer="A"></div>
    <div class="cell"><input maxlength="1" data-answer="S"></div>
    <div class="cell"><input maxlength="1" data-answer="E"></div>
    <div class="cell"><input maxlength="1" data-answer="T"></div>
    <div class="cell"></div>
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
    <li><strong>1:</strong> The language used for querying data in Azure Synapse Analytics. (<strong>SQL</strong>)</li>
    <li><strong>3:</strong> A feature in Azure Synapse that allows for real-time data processing. (<strong>Spark</strong>)</li>
    <li><strong>5:</strong> The type of storage used by Azure Synapse for data warehousing. (<strong>Blob</strong>)</li>
    <li><strong>7:</strong> Feature which is a named view of data that simply points or references the data you want to use in your (<strong>Dataset</strong>)</li>
  </ul>
  <h3>Down</h3>
  <ul>
    <li><strong>1:</strong> Interactive way to write a code to analyze and transform data. (<strong>Notebook</strong>)</li>
    <li><strong>2:</strong> The type of analytics that Azure Synapse is primarily used for. (<strong>Big Data</strong>)</li>
    <li><strong>4:</strong> Synapse spark pool feature which increases and decreases the number of nodes depending on demand. (<strong>Autoscaling</strong>)</li>
    <li><strong>6:</strong> The type of pool used for on-demand SQL queries in Azure Synapse. (<strong>Serverless</strong>)</li>
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

