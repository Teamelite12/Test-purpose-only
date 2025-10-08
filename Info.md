# Programming Languages - Basic Structure Guide

This document provides clear explanations about the basic structure and file setup for various programming languages.

## 1. HTML (HyperText Markup Language)

HTML is the standard markup language for creating web pages.

### Basic Structure

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Page Title</title>
</head>
<body>
    <!-- Content goes here -->
    <h1>Hello World</h1>
</body>
</html>
```

### Key Components

- **`<!DOCTYPE html>`**: Declares the document type and HTML version (HTML5)
- **`<html>`**: Root element that wraps all content on the page
- **`<head>`**: Contains metadata, title, links to stylesheets, and scripts
- **`<body>`**: Contains the visible page content (text, images, links, etc.)

### Purpose of Each Tag

- `<head>`: Holds meta information not displayed on the page
- `<title>`: Sets the browser tab title
- `<meta>`: Provides metadata like character encoding and viewport settings
- `<body>`: Contains all visible content users see and interact with

---

## 2. CSS (Cascading Style Sheets)

CSS is used to style and layout web pages.

### Basic Syntax

```css
selector {
    property: value;
}
```

### Example

```css
body {
    background-color: #f0f0f0;
    font-family: Arial, sans-serif;
}

h1 {
    color: blue;
    text-align: center;
}

.container {
    width: 80%;
    margin: 0 auto;
}

#header {
    padding: 20px;
}
```

### Selectors

- **Element selector**: `h1`, `p`, `div` - targets HTML elements
- **Class selector**: `.classname` - targets elements with specific class
- **ID selector**: `#idname` - targets element with specific ID
- **Universal selector**: `*` - targets all elements

### Linking CSS to HTML

**External stylesheet (recommended):**
```html
<head>
    <link rel="stylesheet" href="styles.css">
</head>
```

**Internal stylesheet:**
```html
<head>
    <style>
        body {
            background-color: white;
        }
    </style>
</head>
```

**Inline style:**
```html
<p style="color: red;">This is red text</p>
```

---

## 3. JavaScript (JS)

JavaScript adds interactivity and dynamic behavior to web pages.

### Basic Structure of a .js File

```javascript
// Variables
let name = "John";
const age = 25;
var oldStyle = "avoid using var";

// Functions
function greet(person) {
    return "Hello, " + person;
}

// DOM Manipulation
document.getElementById("myButton").addEventListener("click", function() {
    alert("Button clicked!");
});

// Console output
console.log("This appears in browser console");
```

### Including JavaScript in HTML

**External script (recommended):**
```html
<body>
    <!-- Content -->
    <script src="script.js"></script>
</body>
```

**Internal script:**
```html
<body>
    <script>
        console.log("Hello from JavaScript!");
    </script>
</body>
```

### DOM Interaction

JavaScript can interact with the Document Object Model (DOM) to:
- Select elements: `document.getElementById()`, `document.querySelector()`
- Modify content: `element.innerHTML`, `element.textContent`
- Change styles: `element.style.color = "red"`
- Add event listeners: `element.addEventListener("click", function)`

---

## 4. C

C is a powerful general-purpose programming language.

### Basic Structure of a .c Program

```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    printf("Hello, World!\n");
    return 0;
}
```

### Key Components

- **`#include <stdio.h>`**: Preprocessor directive that includes standard input/output library
- **`#include <stdlib.h>`**: Includes standard library functions
- **`int main()`**: The main function - program execution starts here
- **`return 0;`**: Indicates successful program termination

### Standard I/O Functions

```c
#include <stdio.h>

int main() {
    int number;
    char name[50];
    
    // Output
    printf("Enter your name: ");
    
    // Input
    scanf("%s", name);
    printf("Hello, %s!\n", name);
    
    return 0;
}
```

### Compilation and Execution

```bash
gcc program.c -o program
./program
```

---

## 5. C++

C++ is an extension of C with object-oriented features.

### Basic Structure of a .cpp Program

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hello, World!" << endl;
    return 0;
}
```

### Key Components

- **`#include <iostream>`**: Includes input/output stream library
- **`using namespace std;`**: Allows use of standard library objects without `std::` prefix
- **`int main()`**: Main function where program execution begins
- **`return 0;`**: Indicates successful program termination

### Input/Output with cout and cin

```cpp
#include <iostream>
using namespace std;

int main() {
    string name;
    int age;
    
    // Output
    cout << "Enter your name: ";
    
    // Input
    cin >> name;
    
    cout << "Enter your age: ";
    cin >> age;
    
    cout << "Hello, " << name << "! You are " << age << " years old." << endl;
    
    return 0;
}
```

### Compilation and Execution

```bash
g++ program.cpp -o program
./program
```

---

## 6. Java

Java is a popular object-oriented programming language.

### Basic Structure of a .java File

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

### Key Components

- **`public class HelloWorld`**: Class definition (filename must match class name: `HelloWorld.java`)
- **`public static void main(String[] args)`**: Main method - program entry point
  - `public`: Accessible from anywhere
  - `static`: Can be called without creating an object
  - `void`: Returns no value
  - `String[] args`: Command-line arguments

### More Complete Example

```java
public class Example {
    // Main method
    public static void main(String[] args) {
        // Variable declaration
        String name = "Alice";
        int age = 25;
        
        // Output
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        
        // Method call
        greet(name);
    }
    
    // Custom method
    public static void greet(String person) {
        System.out.println("Hello, " + person + "!");
    }
}
```

### Compilation and Execution

```bash
javac HelloWorld.java
java HelloWorld
```

---

## 7. Python

Python is a high-level, interpreted programming language known for its simplicity.

### Basic Structure of a .py File

```python
# This is a comment
print("Hello, World!")
```

### Key Features

- **Indentation**: Python uses indentation (spaces/tabs) to define code blocks
- **No semicolons**: Line breaks indicate statement ends
- **Dynamic typing**: No need to declare variable types

### Complete Example

```python
# Variables
name = "Alice"
age = 25
is_student = True

# Output
print("Name:", name)
print(f"Age: {age}")  # f-string formatting

# Input
user_input = input("Enter your name: ")
print(f"Hello, {user_input}!")

# Functions
def greet(person):
    return f"Hello, {person}!"

# Function call
message = greet("Bob")
print(message)

# Conditional statements (note indentation)
if age >= 18:
    print("Adult")
else:
    print("Minor")

# Loops
for i in range(5):
    print(i)

# Lists
numbers = [1, 2, 3, 4, 5]
for num in numbers:
    print(num)
```

### Execution

```bash
python script.py
# or
python3 script.py
```

### Important Concepts

- **Indentation**: Defines code blocks (use 4 spaces)
- **No braces**: Unlike C/C++/Java, Python uses indentation instead of `{}`
- **Interpreted**: No compilation needed, runs directly
- **Dynamic typing**: Variables don't need type declarations

---

## Summary

Each programming language has its own structure and conventions:

- **HTML**: Markup language for web structure
- **CSS**: Styling language for web design
- **JavaScript**: Scripting language for web interactivity
- **C**: Low-level compiled language
- **C++**: Object-oriented extension of C
- **Java**: Platform-independent OOP language
- **Python**: High-level interpreted language with simple syntax

Choose the right language based on your project requirements!
