---
layout: base
title: Cookie Clicker
description: Cookie
hide: true

---

{% include nav/home.html %}

<h1>Cookie Clicker</h1>
    
<img id="cookie" src="https://upload.wikimedia.org/wikipedia/commons/9/9a/Choco_chip_cookie.jpg" alt="cookie" width="200px">
    
<div id="counter">Cookies: 0</div>
    
<button id="autoClicker" class="upgrade" disabled>Buy Auto Clicker (Cost: 10)</button>
<button id="doubleClick" class="upgrade" disabled>Buy Double Click (Cost: 20)</button>
<button id="cheats" class="upgrade" style="color: transparent; background-color: transparent; border: none;" disabled ></button>

<script>
    let cookies = 0;
    let cookiesPerClick = 1;
    let autoClickerCost = 10;
    let doubleClickCost = 20;
    let cheatsCost = 0;
    let autoClickerActive = false;
    let autoClickerInterval;

    const cookieImage = document.getElementById('cookie');
    const counterDisplay = document.getElementById('counter');
    const autoClickerButton = document.getElementById('autoClicker');
    const doubleClickButton = document.getElementById('doubleClick');
    const cheatsButton = document.getElementById('cheats');

        // Update the cookie counter display
        function updateCounter() {
            counterDisplay.textContent = `Cookies: ${cookies}`;
        }

        // Cookie click event
        cookieImage.addEventListener('click', function() {
            cookies += cookiesPerClick;
            updateCounter();
            checkUpgrades();
        });

        // Check if upgrades can be bought
        function checkUpgrades() {
            if (cookies >= autoClickerCost && !autoClickerActive) {
                autoClickerButton.disabled = false;
            } else {
                autoClickerButton.disabled = true;
            }
            if (cookies >= doubleClickCost) {
                doubleClickButton.disabled = false;
            } else {
                doubleClickButton.disabled = true;
            }
            if (cookies >= cheatsCost) {
                cheatsButton.disabled = false;
            } else {
                cheatsButton.disabled = true;
            }
        }

        // Buy auto clicker
        autoClickerButton.addEventListener('click', function() {
            if (cookies >= autoClickerCost) {
                cookies -= autoClickerCost;
                autoClickerCost *= 2; // Increase the cost for the next purchase
                autoClickerButton.textContent = `Buy Auto Clicker (Cost: ${autoClickerCost})`;
                autoClickerActive = true;
                autoClickerButton.disabled = true;
                autoClickerInterval = setInterval(() => {
                    cookies += cookiesPerClick;
                    updateCounter();
                    checkUpgrades();
                }, 1000); // Auto click every 1 second
            }
        });

        // Buy double click upgrade
        doubleClickButton.addEventListener('click', function() {
            if (cookies >= doubleClickCost) {
                cookies -= doubleClickCost;
                cookiesPerClick *= 2; // Double the cookies per click
                doubleClickCost *= 2;  // Increase the cost for the next purchase
                doubleClickButton.textContent = `Buy Double Click (Cost: ${doubleClickCost})`;
                doubleClickButton.disabled = true;
                updateCounter();
            }
        });
        
        cheatsButton.addEventListener('click', function() {
            if (cookies >= cheatsCost) {
                cookies -= cheatsCost;
                cookiesPerClick *= 5000; // Double the cookies per click
                cookies = 100000000000;
                autoClickerCost = 0;
                doubleClickCost = 0;
                cheatsButton.disabled = true;
                updateCounter();
            }
        });
</script>

