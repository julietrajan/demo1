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
  <select id="quiz-dropdown" onchange="checkAnswer()">
    <option value="">Select an answer</option>
    <option value="correct">Correct Answer</option>
    <option value="wrong1">Wrong Answer 1</option>
    <option value="wrong2">Wrong Answer 2</option>
  </select>
  <p id="feedback"></p>
</details>

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

<ul id="sortable">
  <li class="ui-state-default" data-order="1">Item 1</li>
  <li class="ui-state-default" data-order="2">Item 2</li>
  <li class="ui-state-default" data-order="3">Item 3</li>
  <li class="ui-state-default" data-order="4">Item 4</li>
</ul>

<button onclick="checkOrder()">Check Order</button>
<button onclick="helpMe()">Help me</button>

<p id="feedback"></p>

<script src="https://code.jquery.com/ui/1.12.1/jquery-ui.js"></script>
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
