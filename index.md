---
layout: base
title: Student Home 
description: Home Page
hide: true
image: /images/mario_animation.png
---


<style>
        .grid-container {
            display: grid;
            grid-template-columns: repeat(3, 100px);
            grid-gap: 20px;
            position: relative;
        }
        .backdrop {
            position: absolute;
            top: -10px;
            left: -10px;
            width: calc(100% + 20px);
            height: calc(100% + 20px);
            background-color: rgba(0, 0, 0, 0.5);
            z-index: 1;
            border-radius: 10px; /* Optional: rounded corners */
        }
        .grid-button {
            position: relative;
            padding: 20px;
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 18px;
            cursor: pointer;
            transition: background-color 0.3s;
            text-decoration: none; /* Remove underline */
            display: inline-block; /* Make anchor behave like a button */
            text-align: center; /* Center text */
        }
        .grid-button:hover {
            background-color: #0056b3;
        }
        .tooltip {
            visibility: hidden;
            width: 100px;
            background-color: rgba(0, 0, 0, 0.75);
            color: #fff;
            text-align: center;
            border-radius: 5px;
            padding: 5px;
            position: absolute;
            bottom: -30px;
            left: 50%;
            transform: translateX(-50%);
            z-index: 10;
            transition: visibility 0.2s, opacity 0.2s ease-in-out;
            opacity: 0;
        }
        .grid-button:hover .tooltip {
            visibility: visible;
            opacity: 1;
        }
    </style>



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
</div>

