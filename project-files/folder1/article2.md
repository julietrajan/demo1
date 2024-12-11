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



## Question: Interactive way to write a code to analyse and transform data

<form id="petForm">
  <label for="letterN"></label>
  <input type="text" id="letterN" maxlength="1" class="letter-input" oninput="this.value = this.value.toUpperCase()">
  <label for="letterO"></label>
  <input type="text" id="letterO" maxlength="1" class="letter-input" oninput="this.value = this.value.toUpperCase()">
  <label for="letterT"></label>
  <input type="text" id="letterT" maxlength="1" class="letter-input" oninput="this.value = this.value.toUpperCase()">
  <label for="letterE"></label>
  <input type="text" id="letterE" maxlength="1" class="letter-input" oninput="this.value = this.value.toUpperCase()">
  <label for="letterB"></label>
  <input type="text" id="letterB" maxlength="1" class="letter-input" oninput="this.value = this.value.toUpperCase()">
  <label for="letterO2"></label>
  <input type="text" id="letterO2" maxlength="1" class="letter-input" oninput="this.value = this.value.toUpperCase()">
  <label for="letterO3"></label>
  <input type="text" id="letterO3" maxlength="1" class="letter-input" oninput="this.value = this.value.toUpperCase()">
  <label for="letterK"></label>
  <input type="text" id="letterK" maxlength="1" class="letter-input" oninput="this.value = this.value.toUpperCase()">
  <br>
  <button type="button" onclick="checkAnswer()">Submit</button>
  <button type="button" onclick="clearAll()">Clear All</button>
  <button type="button" onclick="fillCorrectAnswer()">Fill Correct Answer</button>
</form>

<p id="result"></p>

<style>
  .letter-input {
    width: 30px;
    height: 30px;
    text-align: center;
    font-size: 18px;
    border: 2px solid #ccc;
    border-radius: 5px;
    margin: 0 5px;
    transition: border-color 0.3s;
  }

  .letter-input:focus {
    border-color: #007bff;
    outline: none;
  }

  button {
    margin: 10px 5px;
    padding: 5px 10px;
    font-size: 16px;
    border: none;
    border-radius: 5px;
    background-color: #007bff;
    color: white;
    cursor: pointer;
    transition: background-color 0.3s;
  }

  button:hover {
    background-color: #0056b3;
  }

  #result {
    margin-top: 10px;
    font-size: 18px;
  }
</style>

<script>
  function checkAnswer() {
    var n = document.getElementById('letterN').value.toUpperCase();
    var o = document.getElementById('letterO').value.toUpperCase();
    var t = document.getElementById('letterT').value.toUpperCase();
    var e = document.getElementById('letterE').value.toUpperCase();
    var b = document.getElementById('letterB').value.toUpperCase();
    var o2 = document.getElementById('letterO2').value.toUpperCase();
    var o3 = document.getElementById('letterO3').value.toUpperCase();
    var k = document.getElementById('letterK').value.toUpperCase();
    var isCorrect = true;

    if (n !== 'N') {
      document.getElementById('letterN').style.color = 'red';
      isCorrect = false;
    } else {
      document.getElementById('letterN').style.color = 'black';
    }

    if (o !== 'O') {
      document.getElementById('letterO').style.color = 'red';
      isCorrect = false;
    } else {
      document.getElementById('letterO').style.color = 'black';
    }

    if (t !== 'T') {
      document.getElementById('letterT').style.color = 'red';
      isCorrect = false;
    } else {
      document.getElementById('letterT').style.color = 'black';
    }

    if (e !== 'E') {
      document.getElementById('letterE').style.color = 'red';
      isCorrect = false;
    } else {
      document.getElementById('letterE').style.color = 'black';
    }

    if (b !== 'B') {
      document.getElementById('letterB').style.color = 'red';
      isCorrect = false;
    } else {
      document.getElementById('letterB').style.color = 'black';
    }

    if (o2 !== 'O') {
      document.getElementById('letterO2').style.color = 'red';
      isCorrect = false;
    } else {
      document.getElementById('letterO2').style.color = 'black';
    }

     if (o3 !== 'O') {
      document.getElementById('letterO3').style.color = 'red';
      isCorrect = false;
    } else {
      document.getElementById('letterO3').style.color = 'black';
    }

    if (k !== 'K') {
      document.getElementById('letterK').style.color = 'red';
      isCorrect = false;
    } else {
      document.getElementById('letterK').style.color = 'black';
    }

    if (isCorrect) {
      document.getElementById('result').innerText = 'Correct!';
    } else {
      document.getElementById('result').innerText = 'Try Again';
    }
  }

  function clearAll() {
    document.getElementById('letterN').value = '';
    document.getElementById('letterO').value = '';
    document.getElementById('letterT').value = '';
    document.getElementById('letterE').value = '';
    document.getElementById('letterB').value = '';
    document.getElementById('letterO2').value = '';
    document.getElementById('letterO3').value = '';
    document.getElementById('letterK').value = '';
    document.getElementById('letterN').style.color = 'black';
    document.getElementById('letterO').style.color = 'black';
    document.getElementById('letterT').style.color = 'black';
    document.getElementById('letterE').style.color = 'black';
    document.getElementById('letterB').style.color = 'black';
    document.getElementById('letterO2').style.color = 'black';
    document.getElementById('letterO3').style.color = 'black';
    document.getElementById('letterK').style.color = 'black';
    document.getElementById('result').innerText = '';
  }

  function fillCorrectAnswer() {
    document.getElementById('letterN').value = 'N';
    document.getElementById('letterO').value = 'O';
    document.getElementById('letterT').value = 'T';
    document.getElementById('letterE').value = 'E';
    document.getElementById('letterB').value = 'B';
    document.getElementById('letterO2').value = 'O';
    document.getElementById('letterO3').value = 'O';
    document.getElementById('letterK').value = 'K';
    document.getElementById('letterN').style.color = 'black';
    document.getElementById('letterO').style.color = 'black';
    document.getElementById('letterT').style.color = 'black';
    document.getElementById('letterE').style.color = 'black';
    document.getElementById('letterB').style.color = 'black';
    document.getElementById('letterO2').style.color = 'black';
    document.getElementById('letterO3').style.color = 'black';
    document.getElementById('letterK').style.color = 'black';
    document.getElementById('result').innerText = '';
  }
</script>
