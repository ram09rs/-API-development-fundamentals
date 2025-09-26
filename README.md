How to Run (Inside Jupyter Notebook)

Install dependencies:

pip install flask requests


Copy the API code into a Jupyter cell and run it.

This will start the Flask server at http://127.0.0.1:5000

In another Jupyter cell, test the API using requests:

import requests

# Get all users
print(requests.get("http://127.0.0.1:5000/users").json())

# Add a new user
print(requests.post("http://127.0.0.1:5000/users", 
                    json={"name": "Charlie", "email": "charlie@example.com"}).json())

# Update a user
print(requests.put("http://127.0.0.1:5000/users/1", 
                   json={"email": "alice_new@example.com"}).json())

# Delete a user
print(requests.delete("http://127.0.0.1:5000/users/2").json())
