---
layout: default
title:  "Need for MFA"
category: "Case Study"
sub-category: "Security"
courses: [SC-200,SC-300, AZ-500]
---

<!DOCTYPE html>
<html>
<head>
    <style>
        .grid {
            display: grid;
            grid-template-columns: repeat(12, 30px); /* Adjust the column count based on crossword width */
            gap: 2px;
        }
        .cell {
            width: 30px;
            height: 30px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 16px;
        }
        .editable {
            border: 1px solid #000;
            background-color: #fff;
        }
        .non-editable {
            background-color: #ccc;
            border: 1px solid #ccc;
        }
        input {
            width: 100%;
            height: 100%;
            border: none;
            text-align: center;
            font-size: 16px;
        }
        input:focus {
            outline: none;
        }
        .incorrect {
            background-color: #ffcccc; /* Red highlight for incorrect answers */
        }
    </style>
    <script>
        // Store the correct answers in the grid
        const correctAnswers = [
            ['A', 'Z', 'U', 'R', 'E', '', '', '', '', '', '', ''],
            ['', 'C', 'O', 'S', 'M', 'O', 'S', 'D', 'B', '', '', ''],
            ['', '', 'A', 'P', 'I', 'S', 'E', '', '', '', '', ''],
            ['', '', 'F', 'U', 'N', 'C', 'T', 'I', 'O', 'N', 'S', ''],
            ['', 'A', 'Z', 'U', 'R', 'E', 'S', 'Q', 'L', 'D', 'A', 'T'],
            ['A', 'Z', 'U', 'R', 'E', 'S', 'Q', 'L', 'D', 'A', 'T', 'A'],
        ];

        // Check if the entered answers are correct
        function checkAnswers() {
            const inputs = document.querySelectorAll('.editable input');
            inputs.forEach((input, index) => {
                const row = Math.floor(index / 12); // Calculate row index
                const col = index % 12; // Calculate column index
                const correctAnswer = correctAnswers[row][col];
                if (correctAnswer && input.value.toUpperCase() !== correctAnswer) {
                    input.classList.add('incorrect'); // Highlight incorrect answers
                } else {
                    input.classList.remove('incorrect'); // Remove highlight for correct answers
                }
            });
        }

        // Fill all correct answers in the grid
        function revealAnswers() {
            const inputs = document.querySelectorAll('.editable input');
            inputs.forEach((input, index) => {
                const row = Math.floor(index / 12); // Calculate row index
                const col = index % 12; // Calculate column index
                const correctAnswer = correctAnswers[row][col];
                if (correctAnswer) {
                    input.value = correctAnswer; // Fill correct answer
                    input.classList.remove('incorrect'); // Remove incorrect highlight
                }
            });
        }
    </script>
</head>
<body>

<div class="grid">
    <!-- Grid Rows -->
    <!-- Row 1 -->
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell non-editable"></div>
    <div class="cell non-editable"></div>
    <div class="cell non-editable"></div>
    <div class="cell non-editable"></div>
    <div class="cell non-editable"></div>
    <div class="cell non-editable"></div>
    <div class="cell non-editable"></div>

    <!-- Row 2 -->
    <div class="cell non-editable"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell non-editable"></div>
    <div class="cell non-editable"></div>
    <div class="cell non-editable"></div>

    <!-- Row 3 -->
    <div class="cell non-editable"></div>
    <div class="cell non-editable"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell non-editable"></div>
    <div class="cell non-editable"></div>
    <div class="cell non-editable"></div>
    <div class="cell non-editable"></div>
    <div class="cell non-editable"></div>

    <!-- Row 4 -->
    <div class="cell non-editable"></div>
    <div class="cell non-editable"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell non-editable"></div>

    <!-- Row 5 -->
    <div class="cell non-editable"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>

    <!-- Row 6 -->
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
    <div class="cell editable"><input type="text" maxlength="1"></div>
</div>

<br>
<button onclick="checkAnswers()">Check Answers</button>
<button onclick="revealAnswers()">Reveal Answers</button>

</body>
</html>
