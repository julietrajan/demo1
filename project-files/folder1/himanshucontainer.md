---
layout: default
title:  "Himanshu Container"
category: "Case Study"
sub-category: "Security"
courses: [AI-102, AI-3016, AI-3018]
---

# ACR: Journey to Containerization

## Introduction:

Welcome to the world of TechWave Solutions, a dynamic and innovative company that has been at the forefront of technological advancements for over a decade. TechWave Solutions specializes in developing cutting-edge software applications that cater to a diverse range of industries, from healthcare to finance. As the demand for scalable and efficient solutions continues to grow, TechWave Solutions has decided to embark on a transformative journey to modernize their application infrastructure.
The company has recognized the immense potential of containerization in streamlining their development and deployment processes. By leveraging Docker and Azure Container Registry, TechWave Solutions aims to enhance the portability, security, and scalability of their applications. This transformation will not only improve their operational efficiency but also enable them to deliver high-quality solutions to their clients with greater speed and reliability.
In this activity, you will step into the shoes of TechWave Solutions' development team. Your mission is to create a Docker file, build the image, and push it to the Azure Container Registry. 

## Scenario: 

You are a developer tasked with containerizing your Python app and run it. Your app code is present in ‘sample.py’ present in your local machine. Use the instructions given and arrange them in order to complete the task given to you on the right-hand side.

## Question 1: 

Rearrange the following instructions and create a functional Docker file for the python application that you are developing. 
Dockerfile Instructions:

<div class="column1">
  <ul id="sortable-setup" class="styled-list">
    <li class="ui-state-default" data-order="4">WORKDIR /app</li>
    <li class="ui-state-default" data-order="6">CMD [“python”, “sample.py”]</li>
    <li class="ui-state-default" data-order="5">COPY sample.py ./</li>
    <li class="ui-state-default" data-order="2">Run apt-get update && apt-get install -y</li>
    <li class="ui-state-default" data-order="3">RUN mkdir /app</li>
    <li class="ui-state-default" data-order="1">FROM python</li>
  </ul>
</div>  

<button onclick="checkOrderSetup()">Check Order</button>
<button onclick="helpMeSetup()">Help me</button>
<p id="feedback-setup"></p>


## Question 2: 
Now since you got the Dockerfile now, you are ready to build the container image and push it to the container registry. We will be using Azure Container Registry (ACR) for hosting our container images. Please select what tools you can use to build your image and push it to ACR. Choose all that apply.

<form id="quizForm2">
  <input type="radio" id="q2a" name="q2" value="A">
  <label for="q2a">A. Docker CLI</label><br>
  <input type="radio" id="q2b" name="q2" value="B">
  <label for="q2b">B. Azure ACR Tasks</label><br>
  <input type="radio" id="q2c" name="q2" value="C">
  <label for="q2c">C. Kubectl</label><br>
  <input type="radio" id="q2d" name="q2" value="D">
  <label for="q2d">D. Azure CLI</label><br>
  <button type="button" onclick="checkAnswer2()" class="styled-button">Submit</button>
</form>

<p id="result2"></p>

## Question 3: 
Please select the right Azure ACR Task command to build the container image and push the image to ACR. Select one.

<form id="quizForm3">
  <input type="radio" id="q3a" name="q3" value="A">
  <label for="q3a">A. az acr build --registry $ACR_NAME --image <image-name>:v1 --file /path/to/Dockerfile /path/to/build/context</label><br>
  <input type="radio" id="q3b" name="q3" value="B">
  <label for="q3b">B. az build -–registry $ACR_Name –image  <image-name>:v1 Dockerfile</label><br>
  <input type="radio" id="q3c" name="q3" value="C">
  <label for="q3c">C. acr build -–registry $ACR_Name –image  <image-name>:v1 Dockerfile </label><br>
  <button type="button" onclick="checkAnswer3()" class="styled-button">Submit</button>
</form>

<p id="result3"></p>


<script>
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

  function checkAnswer2() {
    var radios = document.getElementsByName('q2');
    var correctAnswer = ['A', 'B'];
    var result = document.getElementById('result2');
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

  function checkAnswer3() {
    var radios = document.getElementsByName('q3');
    var correctAnswer = 'A';
    var result = document.getElementById('result3');
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
