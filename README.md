# Python List Loop Project

A simple Python project that demonstrates how to loop through a list and print items, with a REST API endpoint.

## Project Structure

```
.
├── main.py          # Main Python script (console app)
├── api.py           # Flask API server
├── requirements.txt # Python dependencies
└── README.md        # This file
```

## Prerequisites

- Python 3.6 or higher installed on your system
- No external dependencies required

## Setup Steps

1. **Verify Python Installation**

   ```bash
   python3 --version
   ```

   If Python is not installed, download it from [python.org](https://www.python.org/downloads/)

2. **Navigate to Project Directory**
   ```bash
   cd "/Users/gauravsapkal/CodeMode/Python practice"
   ```

## Running the Program

### Option 1: Direct Execution

```bash
python3 main.py
```

### Option 2: Make it Executable (Unix/macOS/Linux)

```bash
chmod +x main.py
./main.py
```

## What the Program Does

The program demonstrates two methods of looping through a list:

1. **Simple iteration**: Loops through each item directly
2. **Enumerated iteration**: Loops with index numbers

The sample list contains fruit names: Apple, Banana, Orange, Mango, and Grapes.

## Expected Output

```
=== Looping through the list ===

Method 1: Simple iteration
  - Apple
  - Banana
  - Orange
  - Mango
  - Grapes

Method 2: With index
  1. Apple
  2. Banana
  3. Orange
  4. Mango
  5. Grapes

=== Done! ===
```

## Customization

To use your own list, modify the `fruits` list in `main.py`:

```python
fruits = ["Your", "Custom", "Items", "Here"]
```

## Running the API Server

### 1. Install Dependencies

First, install Flask:

```bash
pip3 install -r requirements.txt
```

### 2. Start the API Server

```bash
python3 api.py
```

The server will start at `http://127.0.0.1:5000`

### 3. Test the API Endpoints

**Option 1: Using curl**

```bash
# Get API information
curl http://127.0.0.1:5000/

# Get the fruit list
curl http://127.0.0.1:5000/fruits
```

**Option 2: Open in Browser**

- Visit `http://127.0.0.1:5000/` for API info
- Visit `http://127.0.0.1:5000/fruits` for the fruit list

### API Response Examples

**GET /** - API Information

```json
{
  "message": "Welcome to the Fruit List API",
  "endpoints": {
    "/fruits": "GET - Returns the list of fruits"
  }
}
```

**GET /fruits** - Fruit List

```json
{
  "success": true,
  "count": 5,
  "data": ["Apple", "Banana", "Orange", "Mango", "Grapes"]
}
```

### Stopping the Server

Press `Ctrl + C` in the terminal to stop the server.

## Learning Points

- How to create and iterate through lists in Python
- Using `for` loops
- Using `enumerate()` for indexed iteration
- String formatting with f-strings
- Basic Python script structure
- Creating REST APIs with Flask
- JSON responses and HTTP endpoints
