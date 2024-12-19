---
layout: default
title: "video"
category: "Comic"
sub-category: "Security"
---

# My Video

<div class="tile" onclick="toggleFeatures()">
    <h2>Azure Firewall</h2>
    <div id="features" class="features">
        <ul>
            <li>Feature 1: Built-in high availability</li>
            <li>Feature 2: Unrestricted cloud scalability</li>
            <li>Feature 3: Threat intelligence-based filtering</li>
            <li>Feature 4: Application FQDN filtering rules</li>
            <li>Feature 5: Network traffic logging</li>
        </ul>
    </div>
</div>

<style>
    .tile {
        border: 1px solid #ccc;
        padding: 20px;
        margin: 20px;
        cursor: pointer;
        background-color: #f9f9f9;
        transition: background-color 0.3s;
    }
    .tile:hover {
        background-color: #e0e0e0;
    }
    .features {
        display: none;
        margin-top: 10px;
    }
</style>

<script>
    function toggleFeatures() {
        var features = document.getElementById('features');
        if (features.style.display === 'none' || features.style.display === '') {
            features.style.display = 'block';
        } else {
            features.style.display = 'none';
        }
    }
</script>
