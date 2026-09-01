---
layout: post
title: About
permalink: /about/
comments: true
---

## As a conversation Starter

Here are some places I have lived.

<comment>
Flags are made using Wikipedia images
</comment>

<style>
    /* Style looks pretty compact, 
       - grid-container and grid-item are referenced the code 
    */
    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); /* Dynamic columns */
        gap: 10px;
    }
    .grid-item {
        text-align: center;
    }
    .grid-item img {
        width: 100%;
        height: 100px; /* Fixed height for uniformity */
        object-fit: contain; /* Ensure the image fits within the fixed height */
    }
    .grid-item p {
        margin: 5px 0; /* Add some margin for spacing */
    }

    .image-gallery {
        display: flex;
        flex-wrap: nowrap;
        overflow-x: auto;
        gap: 10px;
        }

    .image-gallery img {
        max-height: 150px;
        object-fit: cover;
        border-radius: 5px;
    }
</style>

<!-- This grid_container class is used by CSS styling and the id is used by JavaScript connection -->
<div class="grid-container" id="grid_container">
    <!-- content will be added here by JavaScript -->
</div>

<script>
    // 1. Make a connection to the HTML container defined in the HTML div
    var container = document.getElementById("grid_container"); // This container connects to the HTML div

    // 2. Define a JavaScript object for our http source and our data rows for the Living in the World grid
    var http_source = "https://upload.wikimedia.org/wikipedia/commons/";
    var living_in_the_world = [
        {"flag": "0/01/Flag_of_California.svg", "greeting": "Hey", "description": "California - place of residence"},
        {"flag": "b/b7/Flag_of_Europe.svg", "greeting": "Hi", "description": "Europe - France, Germany, Italy, Greece"},
        {"flag": "4/48/Flag_of_Singapore.svg", "greeting": "What's up", "description": "Singapore"},
        {"flag": "c/cb/Flag_of_the_United_Arab_Emirates.svg", "greeting": "Marhaba", "description": "United Arab Emirates - Dubai"},
        {"flag": "4/41/Flag_of_India.svg", "greeting": "Namaste", "description": "India - Mumbai and Kolkata"},

    ];

    // 3a. Consider how to update style count for size of container
    // The grid-template-columns has been defined as dynamic with auto-fill and minmax

    // 3b. Build grid items inside of our container for each row of data
    for (const location of living_in_the_world) {
        // Create a "div" with "class grid-item" for each row
        var gridItem = document.createElement("div");
        gridItem.className = "grid-item";  // This class name connects the gridItem to the CSS style elements
        // Add "img" HTML tag for the flag
        var img = document.createElement("img");
        img.src = http_source + location.flag; // concatenate the source and flag
        img.alt = location.flag + " Flag"; // add alt text for accessibility

        // Add "p" HTML tag for the description
        var description = document.createElement("p");
        description.textContent = location.description; // extract the description

        // Add "p" HTML tag for the greeting
        var greeting = document.createElement("p");
        greeting.textContent = location.greeting;  // extract the greeting

        // Append img and p HTML tags to the grid item DIV
        gridItem.appendChild(img);
        gridItem.appendChild(description);
        gridItem.appendChild(greeting);

        // Append the grid item DIV to the container DIV
        container.appendChild(gridItem);
    }
</script>

### Journey through Life

Here is what I did at those places

- 🏫 I went to Design39Campus for elementary and middle school
- 🏫 I am currently in Del Norte High School

### Culture, Family, and Fun

Everything for me, as for many others, revolves around family

- My mother and father are both from India, specifically from Karnataka and West Bengal
- I have 4 other members of my immediate family living in San Diego

<comment>
Some pics...
</comment>
<div class="image-gallery">
  <img src="https://www.google.com/imgres?q=pizza&imgurl=https%3A%2F%2Fwww.recipetineats.com%2Ftachyon%2F2023%2F05%2FGarlic-cheese-pizza_9.jpg&imgrefurl=https%3A%2F%2Fwww.recipetineats.com%2Fgarlic-cheese-pizza%2F&docid=q1QEfArNbtrKPM&tbnid=hC6g14ntYr3OqM&vet=12ahUKEwj2jNne3c2WAxURJkQIHRk0Ab4QnPAOegQIQxAA..i&w=900&h=1125&hcb=2&ved=2ahUKEwj2jNne3c2WAxURJkQIHRk0Ab4QnPAOegQIQxAA" alt="Image 1">
  <img src="https://www.google.com/imgres?q=ice%20cream&imgurl=https%3A%2F%2Fwww.cravethegood.com%2Fwp-content%2Fuploads%2F2021%2F04%2Fsous-vide-chocolate-ice-cream-15.jpg&imgrefurl=https%3A%2F%2Fwww.cravethegood.com%2Fsous-vide-chocolate-ice-cream%2F&docid=va1yc0oDrfApLM&tbnid=6cYY3grIMgrI2M&vet=12ahUKEwii7Zvr3c2WAxWvBrwBHSKDK3sQnPAOegQIQxAA..i&w=1467&h=2200&hcb=2&ved=2ahUKEwii7Zvr3c2WAxWvBrwBHSKDK3sQnPAOegQIQxAA" alt="Image 2">
</div>
