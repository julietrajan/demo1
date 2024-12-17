---
layout: default
title:  "Article 8"
category: "Comic"
sub-category: "Security"
---

Once upon a time in the land of Techville, there was a bustling company called Tailwind Trader’s. They were known for their innovative use of technology, but their cybersecurity team, led by Captain Synapse, faced constant challenges from the mischievous Data Gremlins. One day, Captain Synapse decided to deploy a series of powerful tools and features to protect their data fortress. With the help of Azure Synapse Analytics, they embarked on a quest to outsmart the Data Gremlins and secure their kingdom. Let's see how well you know the tools they used!

1. **What is the set of business and technical data definitions that are pre-designed to meet the needs of a particular industry?**  
   Answer: <input type="text" id="q1" size="18" maxlength="18">

2. **What feature defines the connection information needed for Azure Synapse Analytics to connect to external resources?**  
   Answer: <input type="text" id="q2" size="15" maxlength="15">

3. **What is the cost-saving feature of a dedicated SQL pool?**  
   Answer: <input type="text" id="q3" size="5" maxlength="5">

4. **What feature tracks SQL Pool events and writes them to an audit log in your Azure storage account?**  
   Answer: <input type="text" id="q4" size="18" maxlength="18">

5. **What is the Synapse Spark pool feature that increases and decreases the number of nodes depending on demand?**  
   Answer: <input type="text" id="q5" size="11" maxlength="11">

6. **What is the ad-hoc query execution feature?**  
   Answer: <input type="text" id="q6" size="19" maxlength="19">

7. **What is the interactive way to write code to analyze and transform data?**  
   Answer: <input type="text" id="q7" size="8" maxlength="8">

8. **What is the graphical web portal interface to configure and manage Azure Synapse functionalities?**  
   Answer: <input type="text" id="q8" size="20" maxlength="20">

9. **What feature is a named view of data that simply points or references the data you want to use in your activities as inputs and outputs?**  
   Answer: <input type="text" id="q9" size="7" maxlength="7">

10. **What is the cloud-native hybrid transactional and analytical processing (HTAP) capability that enables near real-time analytics over operational data in Azure Cosmos DB?**  
    Answer: <input type="text" id="q10" size="18" maxlength="18">

11. **What is the name of the serverless SQL Pool?**  
    Answer: <input type="text" id="q11" size="8" maxlength="8">

12. **What is the in-memory distributed data processing framework?**  
    Answer: <input type="text" id="q12" size="5" maxlength="5">

<button type="button" onclick="checkAnswers()" class="styled-button">Submit</button>

<p id="result"></p>

<script>
  function checkAnswers() {
    const answers = [
      "DATABASE TEMPLATES",
      "LINKED SERVICES",
      "PAUSE",
      "AZURE SQL AUDITING",
      "AUTOSCALING",
      "SERVERLESS SQL POOL",
      "NOTEBOOK",
      "AZURE SYNAPSE STUDIO",
      "DATASET",
      "AZURE SYNAPSE LINK",
      "BUILT-IN",
      "SPARK"
    ];

    let allCorrect = true;

    for (let i = 1; i <= 12; i++) {
      const input = document.getElementById(`q${i}`);
      const answer = answers[i - 1];
      const inputValue = input.value.toUpperCase();
      let resultHTML = '';

      for (let j = 0; j < answer.length; j++) {
        if (inputValue[j] === answer[j]) {
          resultHTML += `<span style="color: black;">${inputValue[j] || ''}</span>`;
        } else {
          resultHTML += `<span style="color: red;">${inputValue[j] || ''}</span>`;
          allCorrect = false;
        }
      }

      input.value = '';
      input.insertAdjacentHTML('beforebegin', resultHTML);
    }

    const result = document.getElementById('result');
    if (allCorrect) {
      result.textContent = 'Congratulations! All answers are correct!';
      result.style.color = 'green';
    } else {
      result.textContent = 'Some answers are incorrect. Please try again.';
      result.style.color = 'red';
    }
  }
</script>
