---
layout: default
title:  "Article 5"
category: "Comic"
sub-category: "Security"
---
## Article 5

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

<!--
## Scene 2: Benefits of Azure Front Door

**Let's set up Azure Front Door step by step!**
<br>
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

<button onclick="checkOrderSetup()">Check Order</button>
<button onclick="helpMeSetup()">Help me</button>

<p id="feedback-setup"></p>

<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
<script src="https://code.jquery.com/ui/1.12.1/jquery-ui.min.js"></script>
<link rel="stylesheet" href="https://code.jquery.com/ui/1.12.1/themes/base/jquery-ui.css">

<script>
  $(function() {
    $("#sortable-setup").sortable();
    $("#sortable-setup").disableSelection();
  });

  function checkOrderSetup() {
    var items = $("#sortable-setup li");
    var correct = true;
    items.each(function(index) {
      if ($(this).data("order") !== index + 1) {
        correct = false;
      }
    });
    var feedback = document.getElementById("feedback-setup");
    if (correct) {
      feedback.textContent = "Correct order!";
      feedback.style.color = "green";
    } else {
      feedback.textContent = "Incorrect order. Try again.";
      feedback.style.color = "red";
    }
  }

  function helpMeSetup() {
    var items = $("#sortable-setup li").sort(function(a, b) {
      return $(a).data("order") - $(b).data("order");
    });
    $("#sortable-setup").html(items);
    document.getElementById("feedback-setup").textContent = "Here is the correct order.";
    document.getElementById("feedback-setup").style.color = "blue";
  }
</script>
-->
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

  #feedback-setup {
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


**Question 2: Below are the tasks involved in the implementation phase. They are currently out of order. Please reorder them correctly.**


<ul id="sortable-setup" class="styled-list">
  <li class="ui-state-default" data-order="5">Testing and Deployment: The chatbot undergoes rigorous testing to ensure it meets user needs and performs reliably. It is then deployed within Microsoft Teams for easy access.</li>
  <li class="ui-state-default" data-order="3">Integration with Corporate Resources: The chatbot is connected to various knowledge bases and document repositories using APIs, ensuring it can retrieve and present information from multiple sources.</li>
  <li class="ui-state-default" data-order="1">Requirement Gathering: Ben's team conducts interviews with employees to understand their needs and the types of queries they typically have.</li>
  <li class="ui-state-default" data-order="6">Results: The outcomes of the implementation, such as improved efficiency and enhanced user experience.</li>
  <li class="ui-state-default" data-order="2">Design and Development: Using Azure AI Bot Service, the team designs the chatbot's conversational flow and integrates it with Azure OpenAI Service for natural language understanding.</li>
  <li class="ui-state-default" data-order="4">Grounding Responses: Ground the responses of Azure OpenAI Service to the corporate resources.</li>
</ul>

<button onclick="checkOrderSetup()">Check Order</button>
<button onclick="helpMeSetup()">Help me</button>

<p id="feedback-setup"></p>

<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
<script src="https://code.jquery.com/ui/1.12.1/jquery-ui.min.js"></script>
<link rel="stylesheet" href="https://code.jquery.com/ui/1.12.1/themes/base/jquery-ui.css">

<script>
  $(function() {
    $("#sortable-setup").sortable();
    $("#sortable-setup").disableSelection();
  });

  function checkOrderSetup() {
    var items = $("#sortable-setup li");
    var correct = true;
    items.each(function(index) {
      if ($(this).data("order") !== index + 1) {
        correct = false;
      }
    });
    var feedback = document.getElementById("feedback-setup");
    if (correct) {
      feedback.textContent = "Correct order!";
      feedback.style.color = "green";
    } else {
      feedback.textContent = "Incorrect order. Try again.";
      feedback.style.color = "red";
    }
  }

  function helpMeSetup() {
    var items = $("#sortable-setup li").sort(function(a, b) {
      return $(a).data("order") - $(b).data("order");
    });
    $("#sortable-setup").html(items);
    document.getElementById("feedback-setup").textContent = "Here is the correct order.";
    document.getElementById("feedback-setup").style.color = "blue";
  }
</script>

## Question 1
To address the challenges of dispersed information, user experience, and security, which Azure services should Ben use? Select all that apply.

<form id="quiz-form">
  <label class="checkbox-container"><input type="checkbox" name="service" value="1"> Azure AI Cognitive Service Account<span class="checkmark"></span></label><br>
  <label class="checkbox-container"><input type="checkbox" name="service" value="2"> Azure OpenAI Service<span class="checkmark"></span></label><br>
  <label class="checkbox-container"><input type="checkbox" name="service" value="3"> Azure AI Search<span class="checkmark"></span></label><br>
  <label class="checkbox-container"><input type="checkbox" name="service" value="4"> Azure AI Document Intelligence<span class="checkmark"></span></label><br>
  <label class="checkbox-container"><input type="checkbox" name="service" value="5"> Azure AI Bot Service<span class="checkmark"></span></label><br>
  <label class="checkbox-container"><input type="checkbox" name="service" value="6"> Private Endpoint<span class="checkmark"></span></label><br>
  <label class="checkbox-container"><input type="checkbox" name="service" value="7"> Azure SQL Database<span class="checkmark"></span></label><br>
  <label class="checkbox-container"><input type="checkbox" name="service" value="8"> Azure DevOps<span class="checkmark"></span></label><br>
  <label class="checkbox-container"><input type="checkbox" name="service" value="9"> Azure Machine Learning<span class="checkmark"></span></label><br>
  <label class="checkbox-container"><input type="checkbox" name="service" value="10"> Managed Identity<span class="checkmark"></span></label><br>
  <br>
  <button type="button" onclick="checkAnswers()">Check Answer</button>
  <button type="button" onclick="showAnswers()">Help Me</button>
</form>

<p id="result"></p>

<style>
  .checkbox-container {
    display: block;
    position: relative;
    padding-left: 35px;
    margin-bottom: 12px;
    cursor: pointer;
    font-size: 22px;
    user-select: none;
  }

  .checkbox-container input {
    position: absolute;
    opacity: 0;
    cursor: pointer;
    height: 0;
    width: 0;
  }

  .checkmark {
    position: absolute;
    top: 0;
    left: 0;
    height: 25px;
    width: 25px;
    background-color: #eee;
  }

  .checkbox-container input:checked ~ .checkmark {
    background-color: #2196F3;
  }

  .checkmark:after {
    content: "";
    position: absolute;
    display: none;
  }

  .checkbox-container input:checked ~ .checkmark:after {
    display: block;
  }

  .checkbox-container .checkmark:after {
    left: 9px;
    top: 5px;
    width: 5px;
    height: 10px;
    border: solid white;
    border-width: 0 3px 3px 0;
    transform: rotate(45deg);
  }

  #result {
    font-size: 20px;
    margin-top: 20px;
  }

  #result.correct {
    color: blue;
  }

  #result.incorrect {
    color: red;
  }
</style>

<script>
  const correctAnswers = [2, 3, 5, 6, 10];

  function checkAnswers() {
    const selected = Array.from(document.querySelectorAll('input[name="service"]:checked')).map(cb => parseInt(cb.value));
    const isCorrect = correctAnswers.every(val => selected.includes(val)) && selected.length === correctAnswers.length;
    const resultElement = document.getElementById('result');
    resultElement.innerText = isCorrect ? 'Correct' : 'Try again';
    resultElement.className = isCorrect ? 'correct' : 'incorrect';
  }

  function showAnswers() {
    document.querySelectorAll('input[name="service"]').forEach(cb => {
      cb.checked = correctAnswers.includes(parseInt(cb.value));
    });
    const resultElement = document.getElementById('result');
    resultElement.innerText = 'This is the correct order';
    resultElement.className = 'correct';
  }
</script>

## Azure Services Validation
{% raw %}
<form id="validation-form">
  <div class="service-row">
    <select name="service" class="service-dropdown">
      <option value="Azure AI Search">Azure AI Search</option>
      <option value="Azure OpenAI">Azure OpenAI</option>
      <option value="Azure AI Bot Service">Azure AI Bot Service</option>
    </select>
    <textarea name="answer" class="service-textarea" placeholder="Enter your answer here..."></textarea>
    <button type="button" onclick="validateAnswer(this)">Validate</button>
    <span class="result"></span>
  </div>
  <div class="service-row">
    <select name="service" class="service-dropdown">
      <option value="Azure AI Search">Azure AI Search</option>
      <option value="Azure OpenAI">Azure OpenAI</option>
      <option value="Azure AI Bot Service">Azure AI Bot Service</option>
    </select>
    <textarea name="answer" class="service-textarea" placeholder="Enter your answer here..."></textarea>
    <button type="button" onclick="validateAnswer(this)">Validate</button>
    <span class="result"></span>
  </div>
  <div class="service-row">
    <select name="service" class="service-dropdown">
      <option value="Azure AI Search">Azure AI Search</option>
      <option value="Azure OpenAI">Azure OpenAI</option>
      <option value="Azure AI Bot Service">Azure AI Bot Service</option>
    </select>
    <textarea name="answer" class="service-textarea" placeholder="Enter your answer here..."></textarea>
    <button type="button" onclick="validateAnswer(this)">Validate</button>
    <span class="result"></span>
  </div>
</form>

<style>
  .service-row {
    display: flex;
    align-items: center;
    margin-bottom: 20px;
  }
  .service-dropdown {
    margin-right: 10px;
  }
  .service-textarea {
    margin-right: 10px;
    width: 300px;
    height: 50px;
  }
  .result {
    font-size: 16px;
    margin-left: 10px;
  }
  .result.correct {
    color: blue;
  }
</style>

<script>
  const correctAnswers = {
    "Azure AI Search": "Efficient Query Processing: Optimized for fast and efficient query processing, ensuring quick response times.",
    "Azure OpenAI": "Diverse Models: Models can be used for content generation, summarization, semantic search, natural language to code translation, and more.",
    "Azure AI Bot Service": "Integrated Development Environment: Low-Code and No-Code Options, Offers various templates for different bot scenarios, including Q&A, customer service, and more, to speed up development."
  };

  function validateAnswer(button) {
    const row = button.closest('.service-row');
    const service = row.querySelector('.service-dropdown').value;
    const resultElement = row.querySelector('.result');
    resultElement.innerText = correctAnswers[service];
    resultElement.className = 'result correct';
  }
</script>
{% endraw %}
