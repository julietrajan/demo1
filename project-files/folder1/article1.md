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
    <td></td><td><input id="1-1" maxlength="1"></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td>
  </tr>
  <tr>
    <td></td><td><input id="2-1" maxlength="1"></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td>
  </tr>
  <tr>
    <td></td><td><input id="3-1" maxlength="1"></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td>
  </tr>
  <tr>
    <td></td><td><input id="4-1" maxlength="1"></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td>
  </tr>
  <tr>
    <td></td><td><input id="5-1" maxlength="1"></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td>
  </tr>
  <tr>
    <td><input id="6-0" maxlength="1"></td><td><input id="6-1" maxlength="1"></td><td><input id="6-2" maxlength="1"></td><td><input id="6-3" maxlength="1"></td><td><input id="6-4" maxlength="1"></td><td><input id="6-5" maxlength="1"></td><td><input id="6-6" maxlength="1"></td><td></td><td></td><td></td><td></td><td></td><td></td>
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
    "1-1": "A", "2-1": "Z", "3-1": "U", "4-1": "R", "5-1": "E",
    "6-0": "C", "6-1": "O", "6-2": "S", "6-3": "M", "6-4": "O", "6-5": "S", "6-6": "D"
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
