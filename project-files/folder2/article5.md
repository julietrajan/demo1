---
layout: default
title:  "Article 5"
category: "Comic"
sub-category: "Security"
---
## Article 4

This is a test article

## Scene 1: Introduction to Azure Front Door

**Meet Azure Front Door, your superhero for fast, reliable, and secure web content delivery!**
<a href="./1.png" download>
  <img src="./1.png" alt="Digital and App Innovation">
</a>

### What is Azure Front Door?
<select id="quiz-dropdown-1" onchange="checkAnswer1()" class="styled-dropdown">
  <option value="">Select an answer</option>
  <option value="correct">A) A global load balancer and CDN</option>
  <option value="wrong1">B) A database service</option>
  <option value="wrong2">C) A storage solution</option>
</select>
<p id="feedback-1"></p>

<script>
  function checkAnswer1() {
    var dropdown = document.getElementById("quiz-dropdown-1");
    var feedback = document.getElementById("feedback-1");
    if (dropdown.value === "correct") {
      feedback.textContent = "Correct!";
      feedback.style.color = "green";
    } else {
      feedback.textContent = "Try again.";
      feedback.style.color = "red";
    }
  }
</script>

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


## Scene 2: Benefits of Azure Front Door

**Let's set up Azure Front Door step by step!**
<a href="./2.jpeg" download>
  <img src="./2.jpeg" alt="Digital and App Innovation">
</a>

### Arrange the steps to set up Azure Front Door in the correct order:
<ul id="sortable-setup" class="styled-list">
  <li class="ui-state-default" data-order="1">Create a Front Door profile</li>
  <li class="ui-state-default" data-order="2">Add backend pools</li>
  <li class="ui-state-default" data-order="3">Configure routing rules</li>
  <li class="ui-state-default" data-order="4">Set up health probes</li>
</ul>

<button onclick="checkOrderBenefits()">Check Order</button>
<button onclick="helpMeBenefits()">Help me</button>

<p id="feedback-benefits"></p>

<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
<script src="https://code.jquery.com/ui/1.12.1/jquery-ui.min.js"></script>
<link rel="stylesheet" href="https://code.jquery.com/ui/1.12.1/themes/base/jquery-ui.css">

<script>
  $(function() {
    $("#sortable-benefits").sortable();
    $("#sortable-benefits").disableSelection();
  });

  function checkOrderBenefits() {
    var items = $("#sortable-benefits li");
    var correct = true;
    items.each(function(index) {
      if ($(this).data("order") !== index + 1) {
        correct = false;
      }
    });
    var feedback = document.getElementById("feedback-benefits");
    if (correct) {
      feedback.textContent = "Correct order!";
      feedback.style.color = "green";
    } else {
      feedback.textContent = "Incorrect order. Try again.";
      feedback.style.color = "red";
    }
  }

  function helpMeBenefits() {
    var items = $("#sortable-benefits li").sort(function(a, b) {
      return $(a).data("order") - $(b).data("order");
    });
    $("#sortable-benefits").html(items);
    document.getElementById("feedback-benefits").textContent = "Here is the correct order.";
    document.getElementById("feedback-benefits").style.color = "blue";
  }
</script>

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

  #feedback-benefits {
    margin-top: 10px;
    font-size: 16px;
  }
</style>

## Scene 3: How Azure Front Door Works

**Azure Front Door uses intelligent routing to manage traffic and ensure optimal performance.**
<a href="./3.png" download>
  <img src="./3.png" alt="Digital and App Innovation">
</a>

### Select the correct routing method used by Azure Front Door:
<select id="quiz-dropdown-2" onchange="checkAnswer2()" class="styled-dropdown">
  <option value="">Select an answer</option>
  <option value="correct">A) Path-based routing</option>
  <option value="wrong1">B) IP-based routing</option>
  <option value="wrong2">C) DNS-based routing</option>
</select>
<p id="feedback-2"></p>

<script>
  function checkAnswer2() {
    var dropdown = document.getElementById("quiz-dropdown-2");
    var feedback = document.getElementById("feedback-2");
    if (dropdown.value === "correct") {
      feedback.textContent = "Correct!";
      feedback.style.color = "green";
    } else {
      feedback.textContent = "Try again.";
      feedback.style.color = "red";
    }
  }
</script>
