# JavaScript

## Introduction to JavaScript

JavaScript is a versatile scripting language primarily used for front-end web development. It allows you to add interactivity, dynamic behavior, and complex functionality to websites. JavaScript code runs in the user's web browser, manipulating the Document Object Model (DOM) to change the content and appearance of a web page. It's also used in server-side development (Node.js) and other environments.

### How to add js to a project.

There are three ways to add javaScript to an HTML file:

- **Inline:**

  You can embed JavaScript code directly within HTML tags using the `on` event handlers (e.g., `onclick`, `onload`). However, this is generally not recommended for larger amounts of code.

  ```html
  <button onclick="alert('Hello!')">Click Me</button>
  ```

- **Internal (Embedded):**

  Internal JavaScript places code within `<script>` tags directly inside the HTML file. This is suitable for small, page-specific scripts.

  - **Placement:** `<script>` tags can be placed in the `<head>` or `<body>`. Placing them just before the closing `</body>` tag is a common practice for performance reasons, as it allows the HTML to parse and render before the script executes. If placed in the `<head>`, and your script interacts with the DOM, use the `DOMContentLoaded` event:

  ```html
  <script>
    document.addEventListener("DOMContentLoaded", function () {
      // DOM-manipulation code here
      let myElement = document.getElementById("myId");
      if (myElement) {
        myElement.textContent = "Updated!";
      }
    });
  </script>
  ```

- **External JavaScript (Recommended)**

  The preferred method for most projects is to use external JavaScript files. This involves creating separate `.js` files and linking them to your HTML using the `<script>` tag's `src` attribute.

  - **Benefits:**
    - **Maintainability:** Code is organized and easier to update.
    - **Reusability:** JavaScript code can be reused across multiple HTML pages.
    - **Caching:** Browsers can cache external JavaScript files, improving page load times.
    - **Separation of Concerns:** Keeps HTML (structure) and JavaScript (behavior) separate.

  ```html
  <script src="script.js"></script>

  <script src="script.js"></script>
  script.js: JavaScript console.log("Hello from script.js!"); // More complex
  logic can go here
  ```

  And in `script.js`:

  ```javascript
  console.log("Hello from script.js!");
  ```

```

# JavaScript
```
