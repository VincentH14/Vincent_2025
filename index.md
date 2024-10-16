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
        .backdrop {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
            z-index: 1;
        }
        .grid-container {
            display: grid;
            grid-template-columns: repeat(3, 100px);
            grid-gap: 20px;
            position: relative;
            z-index: 2;
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
            bottom: -30px; /* Position the tooltip below the button */
            left: 50%;
            transform: translateX(-50%);
            z-index: 10; /* Ensure tooltip is above the backdrop */
            transition: visibility 0.2s, opacity 0.2s ease-in-out;
            opacity: 0;
        }
        .grid-button:hover .tooltip {
            visibility: visible;
            opacity: 1;
        }
    </style>

<body>

<div class="backdrop"></div>
<div class="grid-container">
    <button class="grid-button">
        3.1
        <span class="tooltip">Description 3.1</span>
    </button>
    <button class="grid-button">
        3.2
        <span class="tooltip">Description 3.2</span>
    </button>
    <button class="grid-button">
        3.3
        <span class="tooltip">Description 3.3</span>
    </button>
    <button class="grid-button">
        3.4
        <span class="tooltip">Description 3.4</span>
    </button>
    <button class="grid-button">
        3.5
        <span class="tooltip">Description 3.5</span>
    </button>
    <button class="grid-button">
        3.6
        <span class="tooltip">Description 3.6</span>
    </button>
    <button class="grid-button">
        3.7
        <span class="tooltip">Description 3.7</span>
    </button>
    <button class="grid-button">
        3.8
        <span class="tooltip">Description 3.8</span>
    </button>
    <button class="grid-button">
        3.9
        <span class="tooltip">Description 3.9</span>
    </button>
</div>

</body>
