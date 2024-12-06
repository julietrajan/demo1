---
layout: default
title:  "Article 4"
category: "Comic"
sub-category: "Security"
---
## Article 4

This is a test article

### Section 1

Test

### Section 2

## Quiz

<details>
  <summary>Choose the correct answer:</summary>
  <select id="quiz-dropdown" onchange="checkAnswer()" class="styled-dropdown">
    <option value="">Select an answer</option>
    <option value="correct">Correct Answer</option>
    <option value="wrong1">Wrong Answer 1</option>
    <option value="wrong2">Wrong Answer 2</option>
  </select>
  <p id="feedback"></p>
</details>

<style>
  .styled-dropdown {
    width: 200px;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 4px;
    background-color: #f9f9f9;
    font-size: 16px;
    color: #333;
    appearance: none;
    -webkit-appearance: none;
    -moz-appearance: none;
  }

  .styled-dropdown:focus {
    border-color: #007bff;
    box-shadow: 0 0 5px rgba(0, 123, 255, 0.5);
    outline: none;
  }

  details summary {
    cursor: pointer;
    font-weight: bold;
  }

  details[open] summary::after {
    content: "▲";
    float: right;
  }

  details summary::after {
    content: "▼";
    float: right;
  }
</style>
<script>
  function checkAnswer() {
    var dropdown = document.getElementById("quiz-dropdown");
    var feedback = document.getElementById("feedback");
    if (dropdown.value === "correct") {
      feedback.textContent = "Correct!";
      feedback.style.color = "green";
    } else {
      feedback.textContent = "Try again.";
      feedback.style.color = "red";
    }
  }
</script>



## Reordering List

<ul id="sortable" class="styled-list">
  <li class="ui-state-default" data-order="1">Item 1</li>
  <li class="ui-state-default" data-order="2">Item 2</li>
  <li class="ui-state-default" data-order="3">Item 3</li>
  <li class="ui-state-default" data-order="4">Item 4</li>
</ul>

<button onclick="checkOrder()">Check Order</button>
<button onclick="helpMe()">Help me</button>

<p id="feedback"></p>

<!-- jQuery and jQuery UI -->
<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
<script src="https://code.jquery.com/ui/1.12.1/jquery-ui.min.js"></script>
<link rel="stylesheet" href="https://code.jquery.com/ui/1.12.1/themes/base/jquery-ui.css">

<style>
  .styled-list {
    list-style-type: none;
    padding: 0;
    margin: 0;
    width: 300px;
  }

  .styled-list li {
    margin: 5px 0;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 4px;
    background-color: #f9f9f9;
    font-size: 16px;
    cursor: move;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .styled-list li:hover {
    background-color: #e9e9e9;
  }

  button {
    margin: 10px 5px;
    padding: 10px 15px;
    border: none;
    border-radius: 4px;
    background-color: #007bff;
    color: white;
    font-size: 16px;
    cursor: pointer;
  }

  button:hover {
    background-color: #0056b3;
  }

  #feedback {
    margin-top: 10px;
    font-size: 16px;
  }
</style>

<script>
  $(function() {
    $("#sortable").sortable();
    $("#sortable").disableSelection();
  });

  function checkOrder() {
    var items = $("#sortable li");
    var correct = true;
    items.each(function(index) {
      if ($(this).data("order") !== index + 1) {
        correct = false;
      }
    });
    var feedback = document.getElementById("feedback");
    if (correct) {
      feedback.textContent = "Correct order!";
      feedback.style.color = "green";
    } else {
      feedback.textContent = "Incorrect order. Try again.";
      feedback.style.color = "red";
    }
  }

  function helpMe() {
    var items = $("#sortable li").sort(function(a, b) {
      return $(a).data("order") - $(b).data("order");
    });
    $("#sortable").html(items);
    document.getElementById("feedback").textContent = "Here is the correct order.";
    document.getElementById("feedback").style.color = "blue";
  }
</script>
