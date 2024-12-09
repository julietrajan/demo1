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
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Azure Synapse Crossword Puzzle</title>
    <style>
        table {
            border-collapse: collapse;
            margin: 20px auto;
        }
        td {
            border: 2px solid #333;
            width: 40px;
            height: 40px;
            text-align: center;
            background-color: #f9f9f9;
        }
        input {
            width: 100%;
            height: 100%;
            text-align: center;
            border: none;
            font-size: 18px;
            font-weight: bold;
            background-color: transparent;
        }
        .incorrect {
            background-color: #ffcccc;
        }
        .correct {
            background-color: #ccffcc;
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
    <h1 style="text-align: center;">Azure Synapse Crossword Puzzle</h1>

    <table>
        <!-- Add your crossword grid here -->
        <tr>
            <td><input type="text" maxlength="1" id="1-1"></td>
            <td><input type="text" maxlength="1" id="1-2"></td>
            <td><input type="text" maxlength="1" id="1-3"></td>
            <td><input type="text" maxlength="1" id="1-4"></td>
            <td><input type="text" maxlength="1" id="1-5"></td>
            <td><input type="text" maxlength="1" id="1-6"></td>
            <td><input type="text" maxlength="1" id="1-7"></td>
            <td><input type="text" maxlength="1" id="1-8"></td>
            <td><input type="text" maxlength="1" id="1-9"></td>
            <td><input type="text" maxlength="1" id="1-10"></td>
            <td><input type="text" maxlength="1" id="1-11"></td>
            <td><input type="text" maxlength="1" id="1-12"></td>
            <td><input type="text" maxlength="1" id="1-13"></td>
            <td><input type="text" maxlength="1" id="1-14"></td>
            <td><input type="text" maxlength="1" id="1-15"></td>
            <td><input type="text" maxlength="1" id="1-16"></td>
            <td><input type="text" maxlength="1" id="1-17"></td>
            <td><input type="text" maxlength="1" id="1-18"></td>
        </tr>
        <tr>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
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
            <td></td>
            <td></td>
            <td></td>
            <td></td>
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
            <td></td>
            <td></td>
            <td></td>
            <td></td>
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
            <td></td>
            <td></td>
            <td></td>
            <td></td>
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
            <td></td>
            <td></td>
            <td></td>
            <td></td>
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
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
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
    <button onclick="clearAll()">Clear All</button>

    <h2>Across</h2>
    <ol>
        <li>Set of business and technical data definitions that are pre-designed to meet the needs of a particular industry (18)</li>
        <li>Graphical web portal interface to configure and manage Azure Synapse functionalities (20)</li>
        <li>Feature which is a named view of data that simply points or references the data you want to use in your activities as inputs and outputs (7)</li>
        <li>Cloud-native hybrid transactional and analytical processing (HTAP) capability that enables near real-time analytics over operational data in Azure Cosmos DB (18)</li>
        <li>Name of serverless SQL Pool (8)</li>
    </ol>

    <h2>Down</h2>
    <ol>
        <li>Feature which defines the connection information needed for Azure Synapse Analytics to connect to external resources (15)</li>
        <li>Cost-saving feature of dedicated SQL pool (5)</li>
        <li>Feature which tracks SQL Pool events and writes them to an audit log in your Azure storage account (18)</li>
        <li>Synapse spark pool feature which increases and decreases the number of nodes depending on demand (11)</li>
        <li>Ad-hoc query execution (19)</li>
        <li>Interactive way to write code to analyze and transform data (8)</li>
        <li>In-memory distributed data processing framework (12)</li>
    </ol>
<script>
    const answers = {
        "1-1": "D", "1-2": "A", "1-3": "T", "1-4": "A", "1-5": "B", "1-6": "A", "1-7": "S", "1-8": "E", "1-9": "T", "1-10": "E", "1-11": "M", "1-12": "P", "1-13": "L", "1-14": "A", "1-15": "T", "1-16": "E", "1-17": "S",
        "8-1": "I", "8-2": "N", "8-3": "T", "8-4": "E", "8-5": "G", "8-6": "R", "8-7": "A", "8-8": "T", "8-9": "E", "8-10": "D", "8-11": "S", "8-12": "E", "8-13": "R", "8-14": "V", "8-15": "I", "8-16": "C", "8-17": "E",
        "9-1": "D", "9-2": "A", "9-3": "T", "9-4": "A", "9-5": "S", "9-6": "E", "9-7": "T",
        "10-1": "A", "10-2": "Z", "10-3": "U", "10-4": "R", "10-5": "E", "10-6": "S", "10-7": "Y", "10-8": "N", "10-9": "A", "10-10": "P", "10-11": "S", "10-12": "E", "10-13": "L", "10-14": "I", "10-15": "N", "10-16": "K",
        "11-1": "N", "11-2": "O", "11-3": "T", "11-4": "E", "11-5": "B", "11-6": "O", "11-7": "O", "11-8": "K",
        "2-1": "A", "2-2": "P", "2-3": "A", "2-4": "C", "2-5": "H", "2-6": "E", "2-7": "S", "2-8": "P", "2-9": "A", "2-10": "R", "2-11": "K",
        "4-1": "A", "4-2": "U", "4-3": "T", "4-4": "O", "4-5": "S", "4-6": "C", "4-7": "A", "4-8": "L", "4-9": "I", "4-10": "N", "4-11": "G",
        "6-1": "S", "6-2": "E", "6-3": "R", "6-4": "V", "6-5": "E", "6-6": "R", "6-7": "L", "6-8": "E", "6-9": "S", "6-10": "S", "6-11": "S", "6-12": "Q", "6-13": "L", "6-14": "P", "6-15": "O", "6-16": "O", "6-17": "L",
        "7-1": "A", "7-2": "U", "7-3": "D", "7-4": "I", "7-5": "T", "7-6": "I", "7-7": "N", "7-8": "G",
        "11a-1": "A", "11a-2": "Z", "11a-3": "U", "11a-4": "R", "11a-5": "E", "11a-6": "S", "11a-7": "Y", "11a-8": "N", "11a-9": "A", "11a-10": "P", "11a-11": "S", "11a-12": "E", "11a-13": "L", "11a-14": "I", "11a-15": "N", "11a-16": "K",
        "11b-1": "B", "11b-2": "U", "11b-3": "I", "11b-4": "L", "11b-5": "T", "11b-6": "-", "11b-7": "I", "11b-8": "N"
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

    function clearAll() {
        const inputs = document.querySelectorAll('input[type="text"]');
        inputs.forEach(input => {
            input.value = '';
            input.classList.remove("incorrect");
            input.classList.remove("correct");
        });
    }
</script>
    
