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
    table {
      border-collapse: collapse;
    }
    td {
      width: 30px;
      height: 30px;
      text-align: center;
      border: 1px solid black;
    }
    input {
      width: 100%;
      height: 100%;
      border: none;
      text-align: center;
    }
    .incorrect {
      background-color: red;
    }
  </style>
</head>
<body>

<table>
  <tr>
    <td></td><td><input id="0-1" maxlength="1"></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td>
  </tr>
  <tr>
    <td></td><td><input id="1-1" maxlength="1"></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td>
  </tr>
  <tr>
    <td></td><td><input id="2-1" maxlength="1"></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td>
  </tr>
  <tr>
    <td></td><td><input id="3-1" maxlength="1"></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td>
  </tr>
  <tr>
    <td></td><td><input id="4-1" maxlength="1"></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td>
  </tr>
  <tr>
    <td><input id="5-0" maxlength="1"></td><td><input id="5-1" maxlength="1"></td><td><input id="5-2" maxlength="1"></td><td><input id="5-3" maxlength="1"></td><td><input id="5-4" maxlength="1"></td><td><input id="5-5" maxlength="1"></td><td><input id="5-6" maxlength="1"></td><td><input id="5-7" maxlength="1"></td><td><input id="5-8" maxlength="1"></td><td><input id="5-9" maxlength="1"></td><td><input id="5-10" maxlength="1"></td><td><input id="5-11" maxlength="1"></td><td><input id="5-12" maxlength="1"></td><td><input id="5-13" maxlength="1"></td><td><input id="5-14" maxlength="1"></td><td><input id="5-15" maxlength="1"></td><td><input id="5-16" maxlength="1"></td>
  </tr>
  <tr>
    <td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td>
  </tr>
  <tr>
    <td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td>
  </tr>
  <tr>
    <td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td>
  </tr>
  <tr>
    <td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td>
  </tr>
  <tr>
    <td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td>
  </tr>
  <tr>
    <td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td>
  </tr>
</table>

<button onclick="checkAnswers()">Check Answers</button>
<button onclick="fillAnswers()">Help Me</button>

<script>
  const answers = {
    "0-1": "C", "1-1": "O", "2-1": "S", "3-1": "M", "4-1": "O", "5-0": "C", "5-1": "O", "5-2": "S", "5-3": "M", "5-4": "O", "5-5": "S", "5-6": "D",
    "5-7": "F", "5-8": "U", "5-9": "N", "5-10": "C", "5-11": "T", "5-12": "I", "5-13": "O", "5-14": "N", "5-15": "S",
    "6-0": "A", "6-1": "P", "6-2": "I", "6-3": "M", "6-4": "A", "6-5": "N", "6-6": "A", "6-7": "G", "6-8": "E", "6-9": "M", "6-10": "E", "6-11": "N", "6-12": "T",
    "7-0": "A", "7-1": "Z", "7-2": "U", "7-3": "R", "7-4": "E", "7-5": "S", "7-6": "Q", "7-7": "L", "7-8": "D", "7-9": "A", "7-10": "T", "7-11": "A", "7-12": "B", "7-13": "A", "7-14": "S", "7-15": "E",
    "8-0": "A", "8-1": "I", "8-2": "S", "8-3": "E", "8-4": "A", "8-5": "R", "8-6": "C", "8-7": "H",
    "9-0": "A", "9-1": "Z", "9-2": "U", "9-3": "R", "9-4": "E", "9-5": "M", "9-6": "A", "9-7": "C", "9-8": "H", "9-9": "I", "9-10": "N", "9-11": "E", "9-12": "L", "9-13": "E", "9-14": "A", "9-15": "R", "9-16": "N", "9-17": "I", "9-18": "N", "9-19": "G"
  };

  function checkAnswers() {
    for (const id in answers) {
      const input = document.getElementById(id);
      if (input.value.toUpperCase() !== answers[id]) {
        input.classList.add("incorrect");
      } else {
        input.classList.remove("incorrect");
      }
    }
  }

  function fillAnswers() {
    for (const id in answers) {
      document.getElementById(id).value = answers[id];
    }
  }
</script>

</body>
</html>
