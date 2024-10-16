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
            bottom: -10px;
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
            background-color: #535452;
            color: #fbfcfa;
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
            bottom: -20px; /* Adjusted for further distance from button */
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


<div class="grid-container">
    <div class="backdrop"></div>
    <a href="https://github.com/VincentH14" class="grid-button">
        Github
    </a>
    <a href="https://nighthawkcoders.github.io/portfolio_2025/analytics" class="grid-button">
        Github Analytics
    </a>
    <a href="https://vincenth14.github.io/Vincent_2025/2024/10/16/3-11_IPYNB_2_.html" class="grid-button">
        JS for Loops
    </a>
    <a href="https://vincenth14.github.io/Vincent_2025/2024/10/09/3-1_IPYNB_2_.html" class="grid-button">
        3.1
        <span class="tooltip">3.1.1-3.1.4</span>
    </a>
    <a href="https://vincenth14.github.io/Vincent_2025/2024/10/09/3-2_IPYNB_2_.html" class="grid-button">
        3.2
        <span class="tooltip">3.2.1-3.2.9</span>
    </a>
    <a href="http://127.0.0.1:4100/Vincent_2025/2024/10/09/3-3-,-3-5_IPYNB_2_.html" class="grid-button">
        3.3
        <span class="tooltip">3.3.1-3.3.4</span>
    </a>
    <a href="http://127.0.0.1:4100/Vincent_2025/2024/10/09/3-4_IPYNB_2_.html" class="grid-button">
        3.4
        <span class="tooltip">3.4.1-3.4.4</span>
    </a>
    <a href="http://127.0.0.1:4100/Vincent_2025/2024/10/09/3-3-,-3-5_IPYNB_2_.html" class="grid-button">
        3.5
        <span class="tooltip">3.5.1-3.5.4</span>
    </a>
    <a href="https://nighthawkcoders.github.io/portfolio_2025/csp/big-idea/p2/3-6" class="grid-button">
        3.6
        <span class="tooltip">3.6.1-3.6.2</span>
    </a>
    <a href="https://nighthawkcoders.github.io/portfolio_2025/csp/big-idea/p2/3-7" class="grid-button">
        3.7
        <span class="tooltip">3.7.1-3.7.2</span>
    </a>
    <a href="http://127.0.0.1:4100/Vincent_2025/2024/10/04/3-8_IPYNB_2_.html" class="grid-button">
        3.8
        <span class="tooltip">3.8.1-3.8.4</span>
    </a>
    <a href="http://127.0.0.1:4100/Vincent_2025/2024/10/04/3-10_IPYNB_2_.html" class="grid-button">
        3.10
        <span class="tooltip">3.10.1-3.10.4.9</span>
    </a>
</div>
