---
layout: base
title: Game Page
description: Games
hide: true
---

{% include nav/home.html %}

<style>
    body {
            background-color: #f0f0f0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            font-family: Arial, sans-serif;
        }
        .container {
            text-align: center;
        }
        h1 {
            margin-bottom: 40px;
        }
        .games {
            display: flex;
            justify-content: center;
            gap: 50px;
        }
        .game-link {
            text-align: center;
            text-decoration: none;
            color: black;
        }
        .game-icon {
            width: 150px;
            height: 150px;
            border: 2px solid #ccc;
            border-radius: 15px;
            padding: 10px;
            background-color: white;
            transition: transform 0.2s ease;
        }
        .game-icon:hover {
            transform: scale(1.1);
        }
        .game-title {
            margin-top: 10px;
            font-size: 20px;
        }
</style>


<div class="container">
    <h1>Select a Game</h1>
        <div class="games">
            <a href="{{site.baseurl}}/snake" class="game-link">
                <img src="https://upload.wikimedia.org/wikipedia/commons/d/df/Snake_%28heraldry%29.svg" alt="Snake Game" class="game-icon">
                <div class="game-title">Snake</div>
            </a>
            <a href="{{site.baseurl}}/cookie_clicker" class="game-link">
                <img src="https://upload.wikimedia.org/wikipedia/commons/9/9a/Choco_chip_cookie.jpg" alt="Cookie Clicker" class="game-icon">
                <div class="game-title">Cookie Clicker</div>
            </a>
        </div>
</div>

