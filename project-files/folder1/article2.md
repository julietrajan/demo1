---
layout: default
title:  "Article 2"
category: "Case Study"
sub-category: "Data"
---

### Quiz 1: After Panel 2
**Question:** What is the main benefit of using Azure API Management?

- [ ] A) It helps manage APIs efficiently.
- [ ] B) It increases the number of APIs.
- [ ] C) It makes APIs slower.

**Correct Answer:** A

### Quiz 2: After Panel 4
**Question:** What can policies in APIM be used for?

- [ ] A) To secure and optimize APIs.
- [ ] B) To delete APIs.
- [ ] C) To create new APIs.

**Correct Answer:** A

### Quiz 3: After Panel 5
**Question:** What does a rate-limiting policy do?

- [ ] A) It limits the number of requests to prevent abuse.
- [ ] B) It increases the number of requests.
- [ ] C) It deletes requests.

**Correct Answer:** A

## Sample Question

What is the capital of France?

<form id="quizForm">
  <input type="radio" id="paris" name="capital" value="paris">
  <label for="paris">Paris</label><br>
  <input type="radio" id="london" name="capital" value="london">
  <label for="london">London</label><br>
  <input type="radio" id="berlin" name="capital" value="berlin">
  <label for="berlin">Berlin</label><br>
  <input type="radio" id="madrid" name="capital" value="madrid">
  <label for="madrid">Madrid</label><br>
  <button type="button" onclick="checkAnswer()" class="styled-button">Submit</button>
</form>

<p id="result"></p>

<script>
  function checkAnswer() {
    var radios = document.getElementsByName('capital');
    var correctAnswer = 'paris';
    var result = document.getElementById('result');
    var selected = false;

    for (var i = 0; i < radios.length; i++) {
      if (radios[i].checked) {
        selected = true;
        if (radios[i].value === correctAnswer) {
          result.textContent = 'Correct!';
          result.style.color = 'green';
        } else {
          result.textContent = 'Incorrect. Try again!';
          result.style.color = 'red';
        }
        break;
      }
    }

    if (!selected) {
      result.textContent = 'Please select an answer.';
      result.style.color = 'orange';
    }
  }
</script>

<style>
  .styled-button {
    background-color: #4CAF50; /* Green */
    border: none;
    color: white;
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
    border-radius: 12px;
  }

  .styled-button:hover {
    background-color: #45a049;
  }
</style>

## Question: What is your pet animal?

<form id="petForm">
  <label for="letterC">C:</label>
  <input type="text" id="letterC" maxlength="1">
  <label for="letterA">A:</label>
  <input type="text" id="letterA" maxlength="1">
  <label for="letterT">T:</label>
  <input type="text" id="letterT" maxlength="1">
  <button type="button" onclick="checkAnswer()">Submit</button>
</form>

<p id="result1"></p>

<script>
  function checkAnswer() {
    var c = document.getElementById('letterC').value.toUpperCase();
    var a = document.getElementById('letterA').value.toUpperCase();
    var t = document.getElementById('letterT').value.toUpperCase();
    
    if (c === 'C' && a === 'A' && t === 'T') {
      document.getElementById('result').innerText = 'Correct!';
    } else {
      document.getElementById('letterC').value = '';
      document.getElementById('letterA').value = '';
      document.getElementById('letterT').value = '';
      document.getElementById('result1').innerText = 'Try Again';
    }
  }
</script>
