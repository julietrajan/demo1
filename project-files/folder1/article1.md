---
layout: default
title:  "Need for MFA"
category: "Case Study"
sub-category: "Security"
courses: [SC-200,SC-300, AZ-500]
---

Tips for Trainers: Play this comic-style play, scene-by-scene, while asking questions in between scenes to initiate classroom discussions.

Characters Intro: This is a conversation between Alice - a program manager and John - a security consultant, over the mandatory multifactor authentication for Azure Sign-in in Contoso.

Across:

1. The language used for querying data in Azure Synapse Analytics. (SQL)
3. A feature in Azure Synapse that allows for real-time data processing. (Spark)
5. The type of storage used by Azure Synapse for data warehousing. (Blob)
7. The service in Azure Synapse that integrates with Power BI for data visualization. (Synapse)
9. The type of analytics that Azure Synapse is primarily used for. (Big Data)
Down:

1. The component in Azure Synapse that provides big data analytics. (Spark)
2. The type of pool used for on-demand SQL queries in Azure Synapse. (Serverless)
4. The Azure service that Azure Synapse integrates with for machine learning. (ML)
6. The type of data processing that Azure Synapse supports, which involves batch and stream processing. (Hybrid)
8. The programming language often used for data transformation in Azure Synapse. (SQL)


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
  </style>
</head>
<body>
  <h1>Azure Synapse Crossword Puzzle</h1>
  <p>Solve the crossword puzzle by answering the clues provided.</p>
  <div class="grid">
    <!-- Add grid cells with placeholder input fields -->
    <div class="cell"><input maxlength="1" data-answer="S"></div>
    <div class="cell"><input maxlength="1" data-answer="Q"></div>
    <div class="cell"><input maxlength="1" data-answer="L"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"></div>
    <div class="cell"><input maxlength="1" data-answer="S"></div>
    <div class="cell"><input maxlength="1" data-answer="P"></div>
    <!-- Add the rest of the grid structure similarly -->
  </div>
  <div class="buttons">
    <button id="checkButton">Check</button>
    <button id="helpButton">Help Me</button>
  </div>
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
