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
