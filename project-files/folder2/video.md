---
layout: default
title: "video"
category: "Comic"
sub-category: "Security"
---

# My Video

Here is an embedded video:

<iframe src="/demo1/project-files/folder2/azurefun1/azurefun1_player.html" width="1024" height="600" frameborder="0" allowfullscreen></iframe>


    <img src="1.png" alt="Interactive Image" style="width: 100%;">
    <img src="2.jpeg" alt="Icon 1" class="icon" style="top: 20%; left: 30%;" onclick="showTooltip(event, 'Answer 1')">
    <img src="3.png" alt="Icon 2" class="icon" style="top: 50%; left: 60%;" onclick="showTooltip(event, 'Answer 2')">

<div id="tooltip" class="tooltip"></div>

<script>
    function showTooltip(event, text) {
        var tooltip = document.getElementById('tooltip');
        tooltip.innerHTML = text;
        tooltip.style.display = 'block';
        tooltip.style.top = event.clientY + 'px';
        tooltip.style.left = event.clientX + 'px';
    }

    document.addEventListener('click', function(event) {
        var tooltip = document.getElementById('tooltip');
        if (!event.target.classList.contains('icon')) {
            tooltip.style.display = 'none';
        }
    });
</script>
