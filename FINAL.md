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
        hr {
            border: 0;
            height: 1px;
            background-color: white;
            margin: 15px 0;
            opacity: 0.5;
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
        <h2>5/5 Points - 12 Week Progress Overview</h2>
        <button class="toggle-btn" onclick="toggleSection('progress')">See More</button>
        <div id="progress" class="content">
            <h3>Five Things Accomplished</h3>
            <ul>
                <li>
                    <button class="toggle-btn" onclick="toggleSection('binaryCalcFrontend')">Binary Calculator Frontend</button>
                    <div id="binaryCalcFrontend" class="content">
                        <p>Developing the Binary Calculator frontend allowed me to demonstrate my skills in web development, particularly in HTML, CSS, and JavaScript. By creating a user-friendly interface that accepts binary input and displays results, I was able to show that I can design interactive programs that meet user needs. It helped me understand the importance of user experience and the role it plays in the functionality of a program.</p>
                        <img src="4.png" width=500>
                    </div>
                </li>
                <li>
                    <button class="toggle-btn" onclick="toggleSection('binaryOverflow')">Binary Overflow</button>
                    <div id="binaryOverflow" class="content">
                        <p>Binary Overflow was a significant step in my development as a computer scientist, as it involved both frontend and backend programming. I worked on the feature's design, implemented a dynamic interface, and integrated it with a backend that stores and retrieves posts. This project matters for CSP because it required me to apply algorithms and data structures while solving real-world problems like data storage and user interaction. Building this feature helped me better understand how software can facilitate collaboration and problem-solving, which is central to the concepts covered in CSP.</p>
                    </div>
                </li>
                <li>
                    <button class="toggle-btn" onclick="toggleSection('frontendReviewSite')">Developed Stylish Frontend for Binary Review Site</button>
                    <div id="frontendReviewSite" class="content">
                        <p>By developing the frontend for the Binary Review Site, I was able to apply design principles and improve my ability to create engaging, functional web pages. I learned how to implement responsive design to ensure that the site would work well on different devices. The collaboration I did with Shaurya was also essential in helping me grow. It helped me understand the impact of a well-designed frontend on user experience and the effectiveness of a website or application.</p>
                        <img src="5.png" width=500>
                    </div>
                </li>
                <li>
                    <button class="toggle-btn" onclick="toggleSection('binaryCalcBackend')">Developed Binary Calculator Backend</button>
                    <div id="binaryCalcBackend" class="content">
                    <a href="http://127.0.0.1:4100/Vincent_2025/snake">Binary Calc</a>
                    </div>
                </li>
                <li>
                    <button class="toggle-btn" onclick="toggleSection('collaborationSkills')">Improved Collaboration Skills through 8-Person Group Project</button>
                    <div id="collaborationSkills" class="content">
                        <p>Working in an 8-person group was possibly the most difficult part of this class. I worked closely with others to divide tasks, share code, and integrate our work into a cohesive product. As software development often involves teams of people working together, the experience taught me how to communicate effectively, resolve conflicts, and ensure that everyone's contributions were integrated successfully, skills that are essential for any aspiring computer scientist.</p>
                    </div>
                </li>
            </ul>
        </div>
    </div>

<div class="section">
        <h2>2/2 Points - Full Stack Project Demo</h2>
        <button class="toggle-btn" onclick="toggleSection('feedback')">See More</button>
        <h3>N@tM Feedback</h3>
    <div class="feedback" id="feedback">
        <p><strong>1. Anu Herranen (Parent)</strong></p>
        <p>Positive: The website is well-structured and easy to navigate.</p>
        <p>Negative: Some of the text could be larger for better readability.</p>
        <hr>
        <p><strong>2. Juha Herranen (Parent)</strong></p>
        <p>Positive: I like how interactive the learning experience is.</p>
        <p>Negative: Some explanations could be clearer for beginners.</p>
        <hr>
        <p><strong>3. Jowan Elzein (Student)</strong></p>
        <p>Positive: I like how there were quizzes, tests, and games for your features.</p>
        <p>Negative: The quiz form could be improved to make it a little more aesthetically pleasing.</p>
        <hr>
        <p><strong>4. Joanna Hu (Student)</strong></p>
        <p>Positive: Everything works and flows together really well!</p>
        <p>Negative: Page is a little bland, add some more frontend pizzazz.</p>
        <hr>
        <p><strong>5. Matthew Wakayama (Student)</strong></p>
        <p>Positive: The design of the website is very cool and slick.</p>
        <p>Negative: There are a lot of binary games out there that could be interesting to incorporate into your website. For example, logic circuits.</p>
        <hr>
        <p><strong>6. Lisa Hadzicki (Neighbor)</strong></p>
        <p>Positive: The site does a great job of making learning engaging.</p>
        <p>Negative: The color contrast could be improved for better visibility.</p>
        <hr>
        <p><strong>7. Eemil Herranen (Brother)</strong></p>
        <p>Positive: The calculator feature is really useful and well implemented.</p>
        <p>Negative: Some buttons could have clearer labels for ease of use.</p>
        <hr>
        <h3><strong><u>8. Bardia Rezai (Adult)</u></strong></h3>
        <h5><u>Positive: I really like the concept of using interactive games to teach binary, it can be used as an engaging and effective way to simplify a complex topic.</u></h5>
        <h5><u>Negative: Consider adding structured learning paths and more in depth analytics to track progress. These features would make it more appealing for schools, coding bootcamps, and corporate training programs, improving scalability on the whole.</u></h5>
        <hr>
        <p><strong>9. Bailey Leeder (Student)</strong></p>
        <p>Positive: Very nice variety of games to learn binary.</p>
        <p>Negative: I would have liked titles for the games that more accurately reflect what the game actually is.</p>
        <hr>
        <p><strong>10. Noah Harris (Student)</strong></p>
        <p>Positive: I like the games. I think the website is a great tool to teach others binary. I also like the homepage design.</p>
        <p>Negative: One thing I can think of is making the styling more dynamic to make it more appealing to the user. For example, on the game where you translate a hexadecimal number into a bit, instead of just red and blue dots, you could use images or icons. Maybe make the game like a board game, where there are different paths and possible challenge questions that involve risk.</p>
    </div>
</div>

<div class="section">
        <h2>1/1 Point - Project Feature Blog Write-Up</h2>
        <button class="toggle-btn" onclick="toggleSection('blog')">See More</button>
        <div id="blog" class="content">
        <img src="posts.png" width="500">
        <img src="burndown.png" width="500">
        <p>
            The <strong>Binary Overflow</strong> feature, inspired by Stack Overflow, allows users to collaborate, post, and discuss other features on our group’s website, fostering a shared knowledge base for problem-solving and innovation.
            This feature incorporates fundamental programming concepts such as <strong>dictionaries, lists, sequencing, selection, and iteration</strong> to ensure efficient functionality.
        </p>
        <p>
            <strong>Dictionaries</strong> are used to store and retrieve user data, posts, and comments, allowing for quick access and organization. <strong>Lists</strong> manage collections of posts, enabling sorting and filtering based on user preferences or trending discussions.
        </p>
        <img src="database.png" width="500">
        <p>
            <strong>Sequencing</strong> ensures that operations such as posting, editing, and retrieving discussions occur in a logical order, maintaining data integrity.
        </p>
        <img src="1.png" width="500">
        <p>
            <strong>Selection</strong> is implemented through conditional statements that determine user permissions, such as moderating content or restricting certain actions based on user roles.
            Finally, <strong>iteration</strong> is applied in features like looping through posts to display them on the website, searching through comments, or updating user statistics dynamically.
        </p>
            <img src="2.png" width="500">
            <img src="6.png" width="500">
        </div>
    </div>

<div class="section">
        <h2>1/1 Point - MCQ</h2>
        <button class="toggle-btn" onclick="toggleSection('mcq')">See More</button>
        <div id="mcq" class="content">
            <img src="9.png" width=1000>
            <img src="10.png" width=1000>
            <img src="11.png" width=1000>
            <p>Looking at my AP College Board MCQ results, I did really well in areas like Boolean expressions, conditionals, iteration, and computing ethics, where I scored 100%. I also feel confident in developing algorithms and extracting information from data, though there's still some room for improvement. However, I struggled with mathematical expressions, calling procedures, and undecidable problems, which are areas I need to work on. If I can strengthen my understanding of these weaker topics, I’ll be in a much better position overall.</p>
        </div>
    </div>

<div class="section mcq">
        <h2>1 Point - Retrospective</h2>
        <button class="toggle-btn" onclick="toggleSection('retro')">See More</button>
        <div id="retro" class="content">
            <p><strong>Personal Review</strong></p>
            <img src="8.png" width=500>
            <h3>Individual Strengths, Weaknesses</h3>
            <p>Compared to Trimester 1, I have improved signifcantly. From not doing any work and leaving it to the last minute, to being productive everyday when I walked in has shown me my potential and what I could do when im productive. I would still like to improve on my collaboration skills as well as checking in with you more often.</p>
            <h4>Overall Trimester Grade: 9.4/10</h4>
            <p>5 Points come from each of the things I was able to accomplish this Trimester.</p>
            <p>1 Point comes from solo demoing my groups features and sites to 10 differente people</p>
            <p>1 Point come from my blog write up on my specific feature, outlining how it meets CPT requriments</p>
            <p>1 Point comes from completing and doing an anlyisis on my AP college board MCQ practice test</p>
            <p>The 0.4 comes from my improvments from Trimester 1, where I completely avoided work and was lazy. Additonally, our group was forced to restart, completely remaking our features with just a week left. Following this we worked on better improving our communication and collaboration.</p>
        </div>
    </div>

</body>
