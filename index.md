---
layout: base
title: Student Home 
description: Home Page
hide: true
image: /images/mario_animation.png
---


<style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f0f0f0;
        }
        .grid-container {
            display: grid;
            grid-template-columns: repeat(3, 150px); /* 3 columns */
            grid-gap: 30px; /* Increased gap */
            position: relative;
        }
        .backdrop {
            position: absolute;
            top: -15px; /* Adjusted for slight overflow */
            left: -15px; /* Adjusted for slight overflow */
            width: calc(100% + 30px); /* Slightly wider than the grid */
            height: calc(100% + 30px); /* Slightly taller than the grid */
            background-color: rgba(0, 0, 0, 0.5);
            z-index: 1;
            border-radius: 10px; /* Optional: rounded corners */
        }
        .grid-button {
            position: relative;
            padding: 30px; /* Increased padding for larger buttons */
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 20px; /* Increased font size */
            cursor: pointer;
            transition: background-color 0.3s;
            text-decoration: none; /* Remove underline */
            display: inline-block; /* Make anchor behave like a button */
            text-align: center; /* Center text */
            z-index: 2; /* Ensure buttons are above the backdrop */
        }
        .grid-button:hover {
            background-color: #0056b3;
        }
        .tooltip {
            visibility: hidden;
            width: 120px; /* Increased width */
            background-color: rgba(0, 0, 0, 0.75);
            color: #fff;
            text-align: center;
            border-radius: 5px;
            padding: 5px;
            position: absolute;
            bottom: -50px; /* Adjusted for further distance from button */
            left: 50%;
            transform: translateX(-50%);
            z-index: 3; /* Ensure tooltips are above buttons */
            transition: visibility 0.2s, opacity 0.2s ease-in-out;
            opacity: 0;
        }
        .grid-button:hover .tooltip {
            visibility: visible;
            opacity: 1;
        }
    </style>
</head>
<body>

<div class="grid-container">
    <div class="backdrop"></div>
    <a href="page3.1.html" class="grid-button">
        3.1
        <span class="tooltip">Description 3.1</span>
    </a>
    <a href="page3.2.html" class="grid-button">
        3.2
        <span class="tooltip">Description 3.2</span>
    </a>
    <a href="page3.3.html" class="grid-button">
        3.3
        <span class="tooltip">Description 3.3</span>
    </a>
    <a href="page3.4.html" class="grid-button">
        3.4
        <span class="tooltip">Description 3.4</span>
    </a>
    <a href="page3.5.html" class="grid-button">
        3.5
        <span class="tooltip">Description 3.5</span>
    </a>
    <a href="page3.6.html" class="grid-button">
        3.6
        <span class="tooltip">Description 3.6</span>
    </a>
    <a href="page3.7.html" class="grid-button">
        3.7
        <span class="tooltip">Description 3.7</span>
    </a>
    <a href="page3.8.html" class="grid-button">
        3.8
        <span class="tooltip">Description 3.8</span>
    </a>
    <a href="page3.9.html" class="grid-button">
        3.9
        <span class="tooltip">Description 3.9</span>
    </a>
    <a href="page3.10.html" class="grid-button">
        3.10
        <span class="tooltip">Description 3.10</span>
    </a>
    <a href="page3.11.html" class="grid-button">
        3.11
        <span class="tooltip">Description 3.11</span>
    </a>
    <a href="page3.12.html" class="grid-button">
        3.12
        <span class="tooltip">Description 3.12</span>
    </a>
    <a href="page3.13.html" class="grid-button">
        3.13
        <span class="tooltip">Description 3.13</span>
    </a>
    <a href="page3.14.html" class="grid-button">
        3.14
        <span class="tooltip">Description 3.14</span>
    </a>
    <a href="page3.15.html" class="grid-button">
        3.15
        <span class="tooltip">Description 3.15</span>
    </a>
    <a href="page3.16.html" class="grid-button">
        3.16
        <span class="tooltip">Description 3.16</span>
    </a>
    <a href="page3.17.html" class="grid-button">
        3.17
        <span class="tooltip">Description 3.17</span>
    </a>
    <a href="page3.18.html" class="grid-button">
        3.18
        <span class="tooltip">Description 3.18</span>
    </a>
</div>
