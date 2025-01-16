---
layout: default
title:  "Need for MFA"
category: "Case Study"
sub-category: "Security"
courses: [SC-200,SC-300, AZ-500]
---

<script>
  fetch('https://github.com/julietrajan/demo1/blob/6fce9c86ae018393453209e6ed8c14cee265bccb/project-files/folder1/visitors.txt')
    .then(response => response.text())
    .then(data => {
      document.getElementById('visitor-count').innerText = `You are visitor no ${data.trim()}`;
    });
</script>

<h2 id="visitor-count">Loading...</h2>

