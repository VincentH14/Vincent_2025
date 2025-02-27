---
layout: base
title: Binary Calc Overview
description: Overview
hide: true
---

# Overview of Binary Caluclator

The functions of the binary calculator include the ability to to perform operations on an 8-bit binary number. It displays the value in multiple numeral systems (binary, octal, decimal, and hexadecimal) and lets users adjust bits individually via "on/off" toggles or add/subtract operations. The interface includes a responsive design, with interactive buttons and visual feedback to indicate active bits.

## Purpose

Our team hopes that this interaction with the Big Idea 2 material and the creation of this calculator will allow you to better understand and get a grasp on the topic.

## Overview of Code

## API

### Increment and Decrememnt Counter

```python
   @app.route('/increment', methods=['POST'])
   def increment_counter():
       """Increments the counter value in the database."""
       calc = binaryCalc.query.first()
       if not calc:
           return jsonify({"error": "Counter not initialized in the database."}), 400


       calc._decimal_value += 1
       try:
           calc.update()
           conversions = calculate_conversions(calc._decimal_value)
           return jsonify(conversions)
       except Exception as e:
           return jsonify({"error": str(e)}), 500
```