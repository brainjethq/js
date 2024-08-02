# JS

  

**What is JavaScript?**

  

JavaScript (JS) is a versatile and powerful programming language primarily used for web development. It enables developers to create interactive and dynamic elements on websites, going beyond static content. Here's what JavaScript can do:

  

*  **Interactivity:** Add elements like dropdown menus, image sliders, form validation, and interactive maps.

*  **Dynamic Content:** Update content on a page without a full refresh, like real-time stock tickers or chat applications.

*  **Animations:** Create smooth transitions, animations, and visual effects to enhance user experience.

*  **User Input Handling:** Process forms, validate user input, and respond to user actions.

*  **Browser Control:** Manipulate the web browser, such as opening new windows or modifying the URL.

*  **Server-Side Scripting:** (with Node.js) Build server-side applications, APIs, and handle backend logic.

  

**Why JavaScript?**

  

There are several reasons why JavaScript has become an essential tool in web development:

  

1.  **Ubiquity:** JavaScript is supported by all major web browsers, making it the de facto language for front-end web development.

  

2.  **Client-Side Execution:** JS code runs directly in the user's browser, reducing the need for server requests and making applications faster and more responsive.

  

3.  **Rich Ecosystem:** JavaScript has a vast ecosystem of libraries and frameworks (e.g., React, Angular, Vue.js) that simplify and accelerate development.

  

4.  **Community:** The JavaScript community is massive and active, providing extensive support, resources, and learning opportunities.

  

5.  **Versatility:** JavaScript can be used for both front-end and back-end development (with Node.js), making it a full-stack language.

  

6.  **Easy to Learn:** JS has a relatively gentle learning curve compared to some other languages, making it accessible to beginners.

  

**In Summary:**

  

JavaScript is the engine that powers the interactive and dynamic web experiences we enjoy today. Its widespread adoption, versatility, and robust ecosystem make it an indispensable skill for web developers and a crucial technology for creating engaging online applications.

  

---

  

# Hello World Program

  

Here's how you can create a "Hello, World!" program in JavaScript, along with explanations:

  

**In a Web Page (HTML):**

  

* Create an HTML file (e.g., `index.html`):

  

```html

<!DOCTYPE  html>

<html>

<head>

<title>Hello, World!</title>

</head>

<body>

<script>

alert("Hello, World!"); // Display the message in a popup box

console.log("Hello, World!"); // Output to the browser's developer console

</script>

</body>

</html>

```

  

* Open `index.html` in your web browser. You'll see a popup alert saying "Hello, World!"

  

**Explanation:**

  

*  `<script>`: This tag tells the browser that the code inside is JavaScript.

*  `alert()`: Displays a popup box with the specified message.

*  `console.log()`: Prints a message to the browser's developer console (accessible by pressing F12 or right-clicking and choosing "Inspect").

  
  
  

**Key Points:**

  

*  **alert() vs. console.log():**  `alert()` is primarily for user interaction, while `console.log()` is for debugging and logging information during development.

  

---

  

# Linking a JavaScript File

  

Here's how you can link a JavaScript file to your HTML page, along with the best practices:

  

**Basic Linking:**

  

1.  **Create Your JavaScript File:**

- Save your JavaScript code in a separate file with the `.js` extension (e.g., `script.js`).

- Example `script.js` content:

  

```javascript

console.log("This is from my external script!");

  

function  greet(name) {

alert(`Hello, ${name}!`);

}

```

  

2.  **Link the File in Your HTML:**

- Place the following `<script>` tag within the `<head>` or `<body>` section of your HTML file:

  

```html

<script  src="script.js"></script>

```

  

- Make sure the `src` attribute correctly points to the path of your JavaScript file.

  

**Explanation:**

  

- The `<script src="script.js"></script>` tag tells the browser to fetch and execute the code in your `script.js` file.

- When the HTML page loads, the browser will run the JavaScript code in the linked file.

  

**Best Practices:**

  

*  **File Placement:**

-  **`<head>`:** Use if your script needs to run before the page content loads or if it modifies the HTML structure.

-  **`<body>` (End):** This is generally preferred. It ensures the HTML content is loaded before your scripts run, preventing errors if your script depends on elements in the page.

  

*  **Defer or Async:**

- Add the `defer` or `async` attribute to the `<script>` tag to control how the script loads:

-  `defer`: The script is fetched in the background and executed in order after the HTML is parsed.

-  `async`: The script is fetched in the background and executed as soon as it's ready, potentially out of order.

  

```html

<script  src="script.js"  defer></script>

<script  src="script.js"  async></script>

```

  

*  **Multiple Scripts:**

- You can link multiple JavaScript files:

  

```html

<script  src="script1.js"></script>

<script  src="script2.js"></script>

```

  
  

**Example:**

  

```html

<!DOCTYPE  html>

<html>

<head>

<title>Linking JavaScript</title>

</head>

<body>

<button  onclick="greet('User')">Click Me</button>

  

<script  src="script.js"  defer></script>

</body>

</html>

```

**Key Points:**

  

*  **Relative vs. Absolute Paths:** Use relative paths (`script.js`) if the JavaScript file is in the same directory as your HTML or absolute paths (e.g., `/scripts/script.js`) for files in different locations.

*  **Module Scripts:** For larger projects, consider using JavaScript modules (`<script type="module" src="module.js"></script>`) for better organization and dependency management.

*  **Error Handling:** Use browser developer tools (e.g., F12) to check for JavaScript errors if your script isn't working.

  

---

  

# Values and Variables

  

Let's explore values and variables in JavaScript:

  

**Values:**

  

*  **What Are They?** Values are the fundamental building blocks of any program. They represent the data that your code works with. Think of them as the nouns in a sentence.

  

*  **Types of Values:** JavaScript has several types of values:

-  **Numbers:**  `10`, `3.14`, `-5` (represent numerical data)

-  **Strings:**  `"Hello"`, `"This is a string!"`, `"123"` (represent text)

-  **Booleans:**  `true`, `false` (represent logical values)

-  **Null:**  `null` (represents the intentional absence of a value)

-  **Undefined:**  `undefined` (represents a variable that has been declared but not assigned a value)

-  **Objects:** Complex data structures (we'll discuss these later)

  

**Variables:**

  

*  **What Are They?** Variables are containers that store values. They give you a way to refer to values by name, making your code more readable and maintainable.

  

*  **Declaring Variables:** In JavaScript, you use the following keywords to declare variables:

-  `let`: Declares a variable with block-level scope (the value can change)

-  `const`: Declares a variable with block-level scope (the value cannot change after assignment)

-  `var`: (Older style) Declares a variable with function-level or global scope (generally avoid using `var` in modern JavaScript)

  

*  **Assigning Values:** You assign a value to a variable using the assignment operator (`=`):

  

```javascript

let  age = 30;

const  pi = 3.14159;

let  message = "Hello there!";

let  isLoggedIn = true;

```

  

**Examples:**

  

```javascript

// Using let

let  x = 10;

console.log(x); // Output: 10

x = 20; // You can change the value of x

console.log(x); // Output: 20

  

// Using const (constant)

const  PI = 3.14159;

console.log(PI); // Output: 3.14159

// PI = 3.14; // This will throw an error because you cannot change the value of a constant

  

// String concatenation

const  firstName = "John";

const  lastName = "Doe";

const  fullName = firstName + " " + lastName;

console.log(fullName); // Output: John Doe

```

  

**Important Considerations:**

  

*  **Naming:** Choose meaningful names for your variables. Follow JavaScript conventions:

- Use camelCase (e.g., `myVariableName`).

- Start with a letter, `$`, or `_`.

- Avoid using reserved keywords (e.g., `let`, `if`, `for`).

*  **Scope:** Be mindful of where you declare variables as it determines their visibility and lifetime within your code.

  

---

# Data Types

The primary data types in JavaScript can be classified into two categories:

1.  **Primitive Types**
    
    -   Numbers: Used to represent integers and approximate real numbers.
    -   Strings: Sequences of characters representing text.
    -   Booleans: The logical values `true` and `false`.
    -   `null`: Represents the intentional absence of a value.
    -   `undefined`: Represents a variable that has been declared but not assigned a value.
    -   Symbols (ES6): Unique and immutable values, primarily used as property names for objects.
2.  **Object Types**
    
    -   Objects: Collections of properties, where each property has a name and a value.
    -   Arrays: Ordered collections of numbered values.
    -   Functions: Parameterized blocks of code that can be invoked.
    -   Other built-in objects: The language also defines a number of other built-in object types, including:
        -   `Set`: Represents a collection of unique values.
        -   `Map`: Represents a collection of key-value pairs.
        -   Typed Arrays: Provide a mechanism for accessing raw binary data.
        -   `RegExp`: Represents patterns in text and is used for text processing.
        -   `Date`: Represents dates and times.
        -   `Error`: Represents errors that can occur during program execution.

**Key Differences:**

-   **Mutability:** Objects are mutable (their values can change), while primitive values are immutable (their values cannot be changed once created).
-   **Comparison:** Primitives are compared by value (two primitives are equal if they have the same value), while objects are compared by reference (two objects are equal only if they refer to the same underlying object).


## Examples:

Here are a few illustrative ones:

### **Primitive Types**

-   **Numbers:**
    
    JavaScript
    
    ```
    let age = 30;        // An integer
    const pi = 3.14159;  // A floating-point number
    let price = 9.99;    // Another floating-point number
    
    ```
    
-   **Strings:**
    
    JavaScript
    
    ```
    let greeting = "Hello, world!";  // A string of text
    let name = 'Alice';              // Another string, using single quotes
    
    ```
    
-   **Booleans:**
    
    JavaScript
    
    ```
    let isLoggedIn = true;   // Represents a true/false value
    let hasDiscount = false;  // Another true/false value
    
    ```
    
-   **null and undefined:**
    
    JavaScript
    
    ```
    let emptyValue = null;        // Explicitly represents no value
    let uninitializedValue;     // Implicitly has no value (undefined)
    
    ```
    
-   **Symbols:**
    
    JavaScript
    
    ```
    const uniqueId = Symbol('id');  // Creates a unique symbol
    
    ```
    

### **Object Types**

-   **Objects:**
    
    JavaScript
    
    ```
    let person = { 
        name: 'Bob',
        age: 25,
        isStudent: false
    };
    
    ```
    
-   **Arrays:**
    
    JavaScript
    
    ```
    let numbers = [1, 2, 3, 4, 5];     // An array of numbers
    let mixedData = [true, 'apple', 7]; // An array with mixed data types
    
    ```
    
-   **Functions:**
    
    JavaScript
    
    ```
    function greet(name) {
        console.log('Hello, ' + name + '!');
    }
    
    ```
    

These examples showcase the fundamental data types you'll encounter when working with JavaScript. The text also provides more elaborate examples involving built-in objects like `Set`,  `Map`,  `Date`, and others, which you can explore further as you delve deeper into the language.

---


# let, const and var


Absolutely, let's explore the `let`,  `const`, and `var` keywords in JavaScript, along with illustrative examples:

### **1. `let`**

-   **Purpose:** Declares a variable whose value can be changed (reassigned) later in the code.
    
-   **Scope:** Block-level scope, meaning it's accessible only within the nearest enclosing block (e.g., within a function, loop, or `if` statement).
    
-   **Example:**
    
    JavaScript
    
    ```
    let age = 30;
    console.log(age); // Output: 30
    
    age = 35; // Reassigning the value
    console.log(age); // Output: 35
    
    ```
    

### **2. `const`**

-   **Purpose:** Declares a constant whose value cannot be changed after its initial assignment.
    
-   **Scope:** Also block-level scope.
    
-   **Example:**
    
    JavaScript
    
    ```
    const PI = 3.14159;
    console.log(PI); // Output: 3.14159
    
    PI = 3; // This will throw an error because you can't reassign a const
    
    ```
    

### **3. `var`** (Legacy)**

-   **Purpose:** Declares a variable, but its behavior differs from `let` in terms of scope.
    
-   **Scope:** Function-level or global scope, depending on where it's declared. If declared inside a function, it's accessible throughout that function. If declared outside any function, it becomes a global variable.
    
-   **Example:**
    
    JavaScript
    
    ```
    var name = 'John';
    console.log(name); // Output: John
    
    name = 'Jane'; // Reassigning is allowed
    console.log(name); // Output: Jane
    
    ```
    

**Recommendation:** In modern JavaScript, it's generally recommended to use `let` and `const` instead of `var`.  `let` provides the flexibility to reassign variables when needed, while `const` helps prevent accidental changes to values that should remain constant, leading to more predictable and maintainable code.

**Key Differences Summarized:**
| Keyword | Scope | Reassignment Allowed |  Best Practice
| :-- | :--: | :--: | :--: |
| `let` |  Block-level | Yes | Use for variables that may change their value|
| `const` |  Block-level | No | Use for values that should remain constant|
| `var` |  Function-level/Global | Yes | Generally avoid in modern JavaScript |

---

# Basic Operators

A comprehensive overview of JavaScript's basic operators, categorizing them based on their functionality. The fundamental categories of operators in JavaScript, along with illustrative examples, are as follows:

### **Arithmetic Operators**

-   Perform mathematical calculations on numeric operands.
    -   **Addition (+):**  `3 + 2` evaluates to `5`
    -   **Subtraction (-):**  `5 - 2` evaluates to `3`
    -   **Multiplication (*):**  `3 * 2` evaluates to `6`
    -   **Division (/):**  `6 / 2` evaluates to `3`
    -   **Modulo (Remainder) (%):**  `7 % 3` evaluates to `1`
    -   **Exponentiation (**) (ES6 and later):** `2 ** 3` evaluates to `8`

### **Relational Operators**

-   Compare two values and return a boolean (`true` or `false`) result.
    -   **Equality (==):**  `3 == 3` evaluates to `true`
    -   **Strict Equality (===):**  `3 === '3'` evaluates to `false` (different types)
    -   **Inequality (!=):**  `3 != 5` evaluates to `true`
    -   **Strict Inequality (!==):**  `3 !== 3` evaluates to `false`
    -   **Less than (<):**  `2 < 5` evaluates to `true`
    -   **Greater than (>):**  `5 > 2` evaluates to `true`
    -   **Less than or equal to (<=):**  `3 <= 3` evaluates to `true`
    -   **Greater than or equal to (>=):**  `5 >= 2` evaluates to `true`

### **Logical Operators**

-   Combine or modify boolean values
    -   **Logical AND (&&):**  `true && false` evaluates to `false`
    -   **Logical OR (||):**  `true \|\| false` evaluates to `true`
    -   **Logical NOT (!):**  `!true` evaluates to `false`

### **Assignment Operators**

-   Assign a value to a variable
    -   **Basic Assignment (=):**  `x = 5` assigns the value 5 to the variable `x`
    -   **Add and Assign (+=):**  `x += 2` is equivalent to `x = x + 2`
    -   **Subtract and Assign (-=):**  `y -= 3` is equivalent to `y = y - 3`

### **Bitwise Operators**

-   Perform operations on the individual bits of integer values
    -   **Bitwise AND (&):**  `5 & 1` evaluates to `1`
    -   **Bitwise OR (|):**  `5 | 1` evaluates to `5`
    -   **Bitwise XOR (^):**  `5 ^ 1` evaluates to `4`

These examples illustrate the core operators used in JavaScript for various computations and comparisons. Understanding these operators is crucial for writing effective JavaScript code.

---

# Operator precedence

**Operator precedence** in JavaScript determines the order in which operations are performed in an expression. The operators with higher precedence are evaluated before operators with lower precedence.

The reference text provides the following example to illustrate this:

JavaScript

```
w = x + y * z;

```

In this expression, the multiplication operator (`*`) has a higher precedence than the addition operator (`+`). Therefore, the multiplication `y * z` is performed first. Subsequently, the result is added to `x`, and the final outcome is assigned to the variable `w` due to the assignment operator (`=`), which holds the lowest precedence.

**Explicit Control with Parentheses**

You can utilize parentheses to explicitly manage the order of evaluation, overriding the default precedence rules.

JavaScript

```
w = (x + y) * z;

```

In this modified expression, the addition within the parentheses is executed first, and then the result is multiplied by `z`.

**Key Points**

-   Understanding operator precedence is crucial for writing correct JavaScript code, especially when dealing with complex expressions.
-   When in doubt, use parentheses to make the intended order of operations clear.


> Reference: [MDN Docs 📖](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_precedence)