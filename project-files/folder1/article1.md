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
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"><input maxlength="1" data-answer="Y"></div>
    <div class="cell"><input maxlength="1" data-answer="N"></div>
    <div class="cell"><input maxlength="1" data-answer="A"></div>

    <!-- Add the rest of the rows with appropriate cells and answers -->
    <!-- Include clue numbers and answers for both across and down clues -->
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
    <li><strong>7:</strong> The service in Azure Synapse that integrates with Power BI for data visualization. (<strong>Synapse</strong>)</li>
    <li><strong>9:</strong> The type of analytics that Azure Synapse is primarily used for. (<strong>Big Data</strong>)</li>
  </ul>
  <h3>Down</h3>
  <ul>
    <li><strong>1:</strong> The component in Azure Synapse that provides big data analytics. (<strong>Spark</strong>)</li>
    <li><strong>2:</strong> The type of pool used for on-demand SQL queries in Azure Synapse. (<strong>Serverless</strong>)</li>
    <li><strong>4:</strong> The Azure service that Azure Synapse integrates with for machine learning. (<strong>ML</strong>)</li>
    <li><strong>6:</strong> The type of data processing that Azure Synapse supports, which involves batch and stream processing. (<strong>Hybrid</strong>)</li>
    <li><strong>8:</strong> The programming language often used for data transformation in Azure Synapse. (<strong>SQL</strong>)</li>
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
