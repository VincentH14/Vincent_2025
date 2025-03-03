---
layout: base
title: Final Review
description: Final
hide: true
image: /images/posts.png
---
<style>
        body {
            font-family: Arial, sans-serif;
            margin: 40px;
            background-color: #121212;
            color: white;
        }
        h1, h2, h3 {
            color: white;
        }
        .section {
            background: #2c2c2c;
            padding: 20px;
            margin: 20px 0;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(255, 255, 255, 0.1);
            color: white;
        }
        .content {
            display: none;
            margin-top: 10px;
        }
        .toggle-btn {
            background-color: #1e90ff;
            color: white;
            border: none;
            padding: 10px;
            cursor: pointer;
            border-radius: 5px;
            margin-top: 10px;
        }
        .toggle-btn:hover {
            background-color: #187bcd;
        }
</style>
<script>
        function toggleSection(id) {
            var content = document.getElementById(id);
            if (content.style.display === "none" || content.style.display === "") {
                content.style.display = "block";
            } else {
                content.style.display = "none";
            }
        }
</script>

<body>
    <h1>Project Summary</h1>
    
<div class="section">
        <h2>5 Points - 12 Week Progress Overview</h2>
        <button class="toggle-btn" onclick="toggleSection('progress')">See More</button>
        <div id="progress" class="content">
            <h3>Five Things Accomplished</h3>
            <ul>
                <li>Binary Calculator Frontend</li>
                <li><a href="https://example.com"><u>Binary Overflow</u></a></li>
                <li>Developed Stylish Frontend for Binary Review Site</li>
                <li><a href="https://example.com"><u>Developed Binary Calculator Backend</u></a></li>
                <li><a href="https://example.com"><u>Improved on Collabartion Skills through 8 person group project</u></a></li>
            </ul>
        </div>
    </div>
    
<div class="section">
        <h2>2 Points - Full Stack Project Demo</h2>
        <button class="toggle-btn" onclick="toggleSection('demo')">See More</button>
        <div id="demo" class="content">
            <h3>CPT Requirement Highlights</h3>
            <p></p>
            <h3>N@tM Feedback</h3>
            <p></p>
        </div>
    </div>
    
<div class="section">
        <h2>1 Point - Project Feature Blog Write-Up</h2>
        <button class="toggle-btn" onclick="toggleSection('blog')">See More</button>
        <div id="blog" class="content">
            <p>
                The <strong>Binary Overflow</strong> feature, inspired by Stack Overflow, allows users to collaborate, post, and discuss other features on our group’s website, fostering a shared knowledge base for problem-solving and innovation.
                I met the <strong>CPT</strong> requirements by demonstrating <strong>program development, algorithm implementation, and user interaction</strong>.
            </p>
            <p>
                Specifically, it required <strong>designing and implementing a program</strong> that enables users to submit posts, categorize discussions, and respond to others.
            </p>
            <img src="/images/posts.png" width="100">
            <p>
                The feature utilizes <strong>data abstraction</strong>, through the use of databases, to manage user-generated content and track interactions. 
            </p>
            <p>
                Additionally, it demonstrates <strong>procedural abstraction</strong> by breaking down tasks into reusable functions that handle posting, retrieving, and moderating discussions.
            </p>
                The creation process also involved <strong>testing and debugging</strong>, ensuring smooth functionality and user experience. Finally, it meets the requirement of including a <strong>written explanation</strong> by allowing for detailed documentation of how the feature works, the problems solved during development, and how it enhances the overall website.
            </p>
        </div>
    </div>
    
<div class="section mcq">
        <h2>1 Point - MCQ</h2>
        <button class="toggle-btn" onclick="toggleSection('mcq')">See More</button>
        <div id="mcq" class="content">
            <p><strong>Question:</strong></p>
            <ul>
                <li>A. </li>
                <li>B. </li>
                <li>C. </li>
                <li>D. </li>
            </ul>
            <p><strong>Answer:</strong></p>
        </div>
    </div>
</body>