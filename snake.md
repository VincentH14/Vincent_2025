---
layout: base
title: Binary Calc Overview
description: Overview
hide: true
---
# Binary Calculator

## Purpose of our group code and site 

- Help students learn how to convert and use binary numbers
- Create an interactive site where people expand and solidify their understanding
- Create an area for collaboration for students 

## Purpose of my code

- Provide a reliable and easy way to show calculations and conversions with binary, decimal, hexdecimal, and octal values.
- Create a feature that allows people to learn about how binary conversions and calculations work

## Input/Output Requests

```javascript
async function incrementCounter() {
        try {
            const response = await fetch(`${API_BASE_URL}/increment`, {
                method: "POST",
                headers: { "Content-Type": "application/json" },
            });
            if (response.ok) {
                const data = await response.json();
                console.log("Increment response:", data); // Debugging
                updateCounterDisplay(data);
            } else {
                console.error("Failed to increment counter:", response.status);
            }
        } catch (error) {
            console.error("Error incrementing counter:", error);
        }
    }

    async function decrementCounter() {
        try {
            console.log('Decrement button pressed! Sending POST request...');
            const response = await fetch(`${API_BASE_URL}/decrement`, {
                method: 'POST',
                headers: { 'Content-Type': 'application/json' }
            });

            if (response.ok) {
                const data = await response.json();
                console.log('Response:', data);

                // Update the values displayed on the frontend
                document.getElementById('binary').innerText = data.binary;
                document.getElementById('octal').innerText = data.octal;
                document.getElementById('hexadecimal').innerText = data.hexadecimal;
                document.getElementById('decimal').innerText = data.decimal;
            } else {
                console.error('Request failed with status:', response.status);
            }
        } catch (error) {
            console.error('Error:', error);
        }
    }
}

```

- The frontend sends a POST request to /increment.
- The server processes this request and updates a counter in the database.
- The API converts the decimal to hexdecimal, binary, and octal.
- The server then returns a JSON response with the updated counter.
- The frontend displays the new counter value in the console.


### Example API response

```json
{
    "binary": "00000010",
    "octal": "2",
    "hexadecimal": "2",
    "decimal": 2
}
```

## Using Postman for API Testing

- Example Request: POST /increment
- URL: http://localhost:8887/increment
- Method: POST
- Headers: { "Content-Type": "application/json" }
- Body: Empty


### Response (Normal)
```json
{
    "binary": "00000010",
    "octal": "2",
    "hexadecimal": "2",
    "decimal": 2
}
```

### Response(Error)

```json
{
    "error": "Counter not initialized in the database."
}
```

## Database Initialization & Recovery

### Initialize Database (db_init)

```python
def initBinaryCalc():
    """Initialize binary counter data"""
    with app.app_context():
        db.create_all()  # Creates tables if they do not exist
        test_data = [
            binaryCalc(user_id="1", decimal_value=1),
            binaryCalc(user_id="2", decimal_value=3),
            binaryCalc(user_id="3", decimal_value=7),
            binaryCalc(user_id="4", decimal_value=15)
        ]
        for record in test_data:
            try:
                record.create()  # Adds record to the database
                print(f"Record created: {repr(record)}")
            except IntegrityError:
                db.session.remove()
                print(f"Duplicate entry found for user_id: {record._user_id}")
```

- Creates  database tables.
- It inserts four test records into the binaryCalc table.
- If theres a duplicate entry, it skips that record and prints an error.

## Using Lists & Dictionaries

```python
def get_all_counters():
    counters = binaryCalc.query.all()  # Returns a list of all records
    return [counter.read() for counter in counters]  # Converts to dictionary format
```

```json
[
    {"id": 1, "user_id": "1", "decimal_value": 5},
    {"id": 2, "user_id": "2", "decimal_value": 10}
]
```

- List: Each item is a database row.
- Dictionary: Each row is converted into a dictionary.

## Formatting API Response Data into DOM

```javascript
    async function updateCounter() {
        const newValue = parseInt(document.getElementById('updateValue').value, 10);

        if (isNaN(newValue) || newValue < 0) {
            alert("Please enter a valid non-negative number.");
            return;
        }

        try {
            console.log("Updating counter to:", newValue);
            const response = await fetch('http://127.0.0.1:8887/update-counter', {
                method: 'PUT',
                headers: { 'Content-Type': 'application/json' },
                body: JSON.stringify({ value: newValue })
            });

            if (response.ok) {
                const data = await response.json();
                console.log("Counter updated successfully:", data);

                // Update the UI with the new values
                document.getElementById('binary').innerText = data.binary;
                document.getElementById('octal').innerText = data.octal;
                document.getElementById('hexadecimal').innerText = data.hexadecimal;
                document.getElementById('decimal').innerText = data.value;

                // Update the bulbs
                const binary = data.binary;
                for (let i = 0; i < binary.length; i++) {
                    const digit = binary[i];
                    const bulb = document.getElementById('bulb' + i);
                    const button = document.getElementById('butt' + i);
                    const input = document.getElementById('digit' + i);

                    input.value = digit;
                    if (digit === "1") {
                        bulb.src = "/portfolio_2025/images/bulb_on.gif";
                        button.innerHTML = "Turn off";
                    } else {
                        bulb.src = "/portfolio_2025/images/bulb_off.png";
                        button.innerHTML = "Turn on";
                    }
                }
            } else {
                console.error("Failed to update counter. Status:", response.status);
                alert("Failed to update counter. Please try again.");
            }
        } catch (error) {
            console.error("Error updating counter:", error);
            alert("An error occurred. Please try again.");
        }
    }
```
- The frontend requests data from the backend.
- The backend returns JSON.
- JavaScript updates the webpage with this data.

## Querying Database for Python Lists

```python
counters = binaryCalc.query.all()
print([counter.read() for counter in counters])  # Returns list of dictionaries
```

```json
[
    {"id": 1, "user_id": "1", "decimal_value": 5},
    {"id": 2, "user_id": "2", "decimal_value": 10}
]
```


## CRUD Methods in Model
```python
    def create(self):
      """
      The create method adds the object to the database and commits the transaction.
    
      Uses:
          The db ORM methods to add and commit the transaction.
    
      Raises:
          Exception: An error occurred when adding the object to the database.
      """
      try:
          db.session.add(self)
          db.session.commit()
      except Exception as e:
          db.session.rollback()
          raise e
    
    def read(self):
      """
      The read method retrieves the object data from the object's attributes and returns it as a dictionary.
    
      Uses:
          The Group.query and User.query methods to retrieve the group and user objects.
    
      Returns:
          dict: A dictionary containing the post data, including user and group names.
      """
      user = User.query.get(self._user_id)
      data = {
          "id": self.id,
          "user_id": self._user_id if user else None,
          "decimal_value": self._decimal_value
      }
      return data
  

    def update(self):
      """
      The update method commits the transaction to the database.
    
      Uses:
          The db ORM method to commit the transaction.
    
      Raises:
          Exception: An error occurred when updating the object in the database.
      """
      try:
          db.session.commit()
      except Exception as e:
          db.session.rollback()
          raise e
    def delete(self):
      """
      The delete method removes the object from the database and commits the transaction.
    
      Uses:
          The db ORM methods to delete and commit the transaction.
    
      Raises:
          Exception: An error occurred when deleting the object from the database.
      """  
      try:
          db.session.delete(self)
          db.session.commit()
      except Exception as e:
          db.session.rollback()
          raise e

```


## CRUD Methods in the API Class

### Create
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
### Read
```python
   @app.route('/get-counter', methods=['GET'])
   def get_counter():
       """Fetch the current counter value from the database."""
       calc = binaryCalc.query.first()
       if not calc:
           return jsonify({"error": "Counter not initialized in the database."}), 400


       conversions = calculate_conversions(calc._decimal_value)
       return jsonify(conversions)
```
### Update
```python
   @app.route('/update-counter', methods=['PUT'])
   def update_counter():
       """Updates the counter to a specific value provided in the request."""
       data = request.get_json()
       new_value = data.get('value')


       if new_value is None or not isinstance(new_value, int):
           return jsonify({"error": "Invalid value. Please provide an integer."}), 400


       if new_value < 0:
           return jsonify({"error": "Value must be a non-negative integer."}), 400


       calc = binaryCalc.query.first()
       if not calc:
           return jsonify({"error": "Counter not initialized in the database."}), 400


       calc._decimal_value = new_value
       try:
           calc.update()
           conversions = calculate_conversions(new_value)
           return jsonify({"value": new_value, **conversions}), 200
       except Exception as e:
           db.session.rollback()
           return jsonify({"error": f"Failed to update counter: {str(e)}"}), 500
```
- Extracts JSON data from the request.
- Validates that the input is an integer.
- Finds the first record in the database.
- Updates the counter value.
- Returns a formatted response.

### Delete
```python
   @app.route('/reset', methods=['DELETE'])
   def reset_decimal():
       """Reset the decimal value to 0 in the database."""
       calc = binaryCalc.query.first()
       if not calc:
           return jsonify({"error": "Counter not initialized in the database."}), 400


       calc._decimal_value = 0
       try:
           calc.update()
           conversions = calculate_conversions(calc._decimal_value)
           return jsonify(conversions), 200
       except Exception as e:
           return jsonify({"error": str(e)}), 500
```


## Call to API (Frontend Fetch)

```javascript
    async function updateCounter() {
        const newValue = parseInt(document.getElementById('updateValue').value, 10);

        if (isNaN(newValue) || newValue < 0) {
            alert("Please enter a valid non-negative number.");
            return;
        }

        try {
            console.log("Updating counter to:", newValue);
            const response = await fetch('http://127.0.0.1:8887/update-counter', {
                method: 'PUT',
                headers: { 'Content-Type': 'application/json' },
                body: JSON.stringify({ value: newValue })
            });

            if (response.ok) {
                const data = await response.json();
                console.log("Counter updated successfully:", data);

                // Update the UI with the new values
                document.getElementById('binary').innerText = data.binary;
                document.getElementById('octal').innerText = data.octal;
                document.getElementById('hexadecimal').innerText = data.hexadecimal;
                document.getElementById('decimal').innerText = data.value;

                // Update the bulbs
                const binary = data.binary;
                for (let i = 0; i < binary.length; i++) {
                    const digit = binary[i];
                    const bulb = document.getElementById('bulb' + i);
                    const button = document.getElementById('butt' + i);
                    const input = document.getElementById('digit' + i);

                    input.value = digit;
                    if (digit === "1") {
                        bulb.src = "/portfolio_2025/images/bulb_on.gif";
                        button.innerHTML = "Turn off";
                    } else {
                        bulb.src = "/portfolio_2025/images/bulb_off.png";
                        button.innerHTML = "Turn on";
                    }
                }
            } else {
                console.error("Failed to update counter. Status:", response.status);
                alert("Failed to update counter. Please try again.");
            }
        } catch (error) {
            console.error("Error updating counter:", error);
            alert("An error occurred. Please try again.");
        }
    }
```

- The frontend sends a PUT request with value: 10.
- The backend updates the counter in the database.
- The server returns the updated value.

### Normal Response

```json
{
    "value": 5,
    "binary": "00000101",
    "octal": "5",
    "hexadecimal": "5",
    "decimal": 5
}
```

### Error Response
```json
{
    "error": "Invalid value. Please provide an integer."
}
```



```python
def calculate_conversions(value):
   """Helper function to calculate binary, octal, and hexadecimal."""
   return {
       "binary": bin(value)[2:].zfill(8),  # Binary with 8 bits
       "octal": oct(value)[2:],  # Octal representation
       "hexadecimal": hex(value)[2:].upper(),  # Hexadecimal representation
       "decimal": value,  # Decimal value
   }
```