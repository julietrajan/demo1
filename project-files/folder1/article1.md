---
layout: default
title:  "Need for MFA"
category: "Case Study"
sub-category: "Security"
courses: [SC-200,SC-300, AZ-500]
---

Tips for Trainers: Play this comic-style play, scene-by-scene, while asking questions in between scenes to initiate classroom discussions.

Characters Intro: This is a conversation between Alice - a program manager and John - a security consultant, over the mandatory multifactor authentication for Azure Sign-in in Contoso.



<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Styled Crossword Puzzle</title>
    <style>
        table {
            border-collapse: collapse;
            margin: 20px auto;
        }
        td {
            border: 2px solid #333; /* Darker border */
            width: 40px; /* Larger cells */
            height: 40px;
            text-align: center;
            background-color: #f9f9f9; /* Light grey background */
        }
        input {
            width: 100%;
            height: 100%;
            text-align: center;
            border: none;
            font-size: 18px; /* Larger font size */
            font-weight: bold; /* Bold text */
            background-color: transparent;
        }
        .incorrect {
            background-color: #ffcccc; /* Light red background for incorrect answers */
        }
        .correct {
            background-color: #ccffcc; /* Light green background for correct answers */
        }
        button {
            display: block;
            margin: 20px auto;
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            border: none;
            background-color: #007bff;
            color: white;
            border-radius: 5px;
        }
        button:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>
    <h1 style="text-align: center;">Styled Crossword Puzzle</h1>

    <table>
        <tr>
            <td><input type="text" maxlength="1" id="1-1"></td>
            <td></td>
            <td></td>
            <td><input type="text" maxlength="1" id="1-4"></td>
            <td></td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td><input type="text" maxlength="1" id="4-1"></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td><input type="text" maxlength="1" id="4-6"></td>
            <td></td>
        </tr>
        <tr>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td><input type="text" maxlength="1" id="7-1"></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
        </tr>
    </table>

    <button onclick="checkAnswers()">Check Answers</button>
    <button onclick="helpMe()">Help Me</button>

    <script>
        const answers = {
            "1-1": "B", "1-4": "S",
            "4-1": "W", "4-6": "P",
            "7-1": "A"
        };

        function checkAnswers() {
            for (const id in answers) {
                const input = document.getElementById(id);
                if (input.value.toUpperCase() !== answers[id]) {
                    input.classList.add("incorrect");
                    input.classList.remove("correct");
                } else {
                    input.classList.add("correct");
                    input.classList.remove("incorrect");
                }
            }
        }

        function helpMe() {
            for (const id in answers) {
                const input = document.getElementById(id);
                input.value = answers[id];
                input.classList.remove("incorrect");
                input.classList.add("correct");
            }
        }
    </script>
</body>
</html>
