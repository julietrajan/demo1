---
layout: default
title:  "Article 4"
category: "Comic"
sub-category: "Security"
---
## Article 4

This is a test article

### Section 1
## Scene 1: Introduction to Azure Front Door

!Azure Front Door Superhero

**Meet Azure Front Door, your superhero for fast, reliable, and secure web content delivery!**

<img src="./mfa1.jpg" alt="img" width="800" height="350">

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

## Scene 2: Benefits of Azure Front Door

!Azure Front Door Flying

**Azure Front Door ensures your content is delivered quickly and securely, no matter where your users are!**

<img src="./mfa1.jpg" alt="img" width="800" height="350">

### Arrange the benefits of Azure Front Door in the correct order:
<ul id="sortable-benefits" class="styled-list">
  <li class="ui-state-default" data-order="1">High availability</li>
  <li class="ui-state-default" data-order="2">Reduced latency</li>
  <li class="ui-state-default" data-order="3">Increased scalability</li>
  <li class="ui-state-default" data-order="4">Improved security</li>
</ul>

<button onclick="checkOrderBenefits()">Check Order</button>
<button onclick="helpMeBenefits()">Help me</button>

<p id="feedback-benefits"></p>

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


## Scene 3: How Azure Front Door Works

!Azure Front Door Control Panel

**Azure Front Door uses intelligent routing to manage traffic and ensure optimal performance.**

<img src="./mfa1.jpg" alt="img" width="800" height="350">

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
