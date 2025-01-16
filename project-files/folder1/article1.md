---
layout: default
title:  "Need for MFA"
category: "Case Study"
sub-category: "Security"
courses: [SC-200,SC-300, AZ-500]
---

<script>
  // Function to trigger GitHub Actions workflow
  async function triggerWorkflow() {
    const response = await fetch('https://api.github.com/repos/julietrajan/demo1/actions/workflows/update-visitor-count.yml/dispatches', {
      method: 'POST',
      headers: {
        'Authorization': 'token YOUR_GITHUB_TOKEN',
        'Accept': 'application/vnd.github.v3+json'
      },
      body: JSON.stringify({ ref: 'refs/heads/main' })
    });
    if (response.ok) {
      console.log('Workflow triggered successfully');
    } else {
      console.error('Failed to trigger workflow');
    }
  }

  // Fetch the visitor count and update the page
  async function updateVisitorCount() {
    await triggerWorkflow();
    const response = await fetch('https://raw.githubusercontent.com/julietrajan/demo1/refs/heads/main/project-files/folder1/visitors.txt');
    const data = await response.text();
    document.getElementById('visitor-count').innerText = `You are visitor no ${data.trim()}`;
  }

  // Trigger the workflow and update the visitor count on page load
  document.addEventListener('DOMContentLoaded', updateVisitorCount);
</script>

<h2 id="visitor-count">Loading...</h2>
