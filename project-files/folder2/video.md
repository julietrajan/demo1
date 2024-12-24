---
layout: default
title: "video1"
category: "Comic"
sub-category: "Security"
---
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
