---
layout: page
title: 
permalink: /about/
image: /images/finland.png
---

{% include nav/home.html %}
<h1>About Me</h1>


<style>
    /* Style looks pretty compact, trace grid-container and grid-item in the code */
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
</style>

<!-- This grid_container class is for the CSS styling, the id is for JavaScript connection -->
<div class="grid-container" id="grid_container">
    <!-- content will be added here by JavaScript -->
</div>

<script>
    // 1. Make a connection to the HTML container defined in the HTML div
    var container = document.getElementById("grid_container"); // This container connects to the HTML div

    // 2. Define a JavaScript object for our http source and our data rows for the Living in the World grid
    
    var http_source = "https://upload.wikimedia.org/wikipedia/commons/";
    var living_in_the_world = [
        {"flag": "0/01/Flag_of_California.svg", "greeting": "Lived in Califronia for 10 years", "description": " "},
        {"flag": "b/bc/Flag_of_Finland.svg", "greeting": "Born in Finland", "description": " "},
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




<p>My name is Vincent Herranen, I was born and raised in Finland. When I was 6 I moved to California and I loved it here. I love sports and watch any soccer game from whatever league or country ever chance I have. 
I took a computer science class because I wanted to challenge myself and gain a deeper understanding of how computers work. I also thought it would help with many aspects in whatever career I choose to pursue. </p>

## My Favorite Things
<a href="https://en.wikipedia.org/wiki/Lacrosse"><img src="https://upload.wikimedia.org/wikipedia/commons/4/4c/Lacrosse_stick_8028.jpg" alt="Lacrosse Stick" width=250></a>
<a href="https://en.wikipedia.org/wiki/Association_football"><img src="https://upload.wikimedia.org/wikipedia/commons/e/ec/Soccer_ball.svg" alt="Soccer ball" width=250></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/2/2a/Spaghetti_al_Pomodoro.JPG" alt="Pasta" width=250>


## My Background
<p>The move from Finland was extremely hard as I had to learn a new language and a adapt to a new culture.</p>

