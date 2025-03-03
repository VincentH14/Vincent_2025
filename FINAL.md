---
layout: base
title: Final Review
description: Final
hide: true
image: /posts.png
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
                <li>
                    <button class="toggle-btn" onclick="toggleSection('binaryCalcFrontend')">Binary Calculator Frontend</button>
                    <div id="binaryCalcFrontend" class="content">
                        <p>Developing the Binary Calculator frontend allowed me to demonstrate my skills in web development, particularly in HTML, CSS, and JavaScript. By creating a user-friendly interface that accepts binary input and displays results, I was able to show that I can design interactive programs that meet user needs. It helped me understand the importance of user experience and the role it plays in the functionality of a program.</p>
                    </div>
                </li>
                <li>
                    <button class="toggle-btn" onclick="toggleSection('binaryOverflow')">Binary Overflow</button>
                    <div id="binaryOverflow" class="content">
                        <p></p>
                    </div>
                </li>
                <li>
                    <button class="toggle-btn" onclick="toggleSection('frontendReviewSite')">Developed Stylish Frontend for Binary Review Site</button>
                    <div id="frontendReviewSite" class="content">
                        <p>By developing the frontend for the Binary Review Site, I was able to apply design principles and improve my ability to create engaging, functional web pages. I learned how to implement responsive design to ensure that the site would work well on different devices. The collaboration I did with Shaurya was also essential in helping me grow. It helped me understand the impact of a well-designed frontend on user experience and the effectiveness of a website or application.</p>
                    </div>
                </li>
                <li>
                    <button class="toggle-btn" onclick="toggleSection('binaryCalcBackend')">Developed Binary Calculator Backend</button>
                    <div id="binaryCalcBackend" class="content">
                        <p>Details about Binary Calculator Backend development...</p>
                    </div>
                </li>
                <li>
                    <button class="toggle-btn" onclick="toggleSection('collaborationSkills')">Improved Collaboration Skills through 8-Person Group Project</button>
                    <div id="collaborationSkills" class="content">
                        <p>Details about collaboration in the 8-person group project...</p>
                    </div>
                </li>
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
            <img src="posts.png" width="500">
            <p>
                The feature utilizes <strong>data abstraction</strong>, through the use of databases, to manage user-generated content and track interactions.
            </p>
            <img src="database.png" width="500">
            <p>
                Additionally, it demonstrates <strong>procedural abstraction</strong> by breaking down tasks into reusable functions that handle posting, retrieving, and moderating discussions.
            </p>
            <img src="1.png" width="500">
            <img src="2.png" width="500">
            <img src="3.png" width="500">
            <p>
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
