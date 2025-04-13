# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Interactive Page</title>
  <script src="script.js" defer></script>
</head>
<body>

  <header>
    <h1 id="title">Welcome to My Website</h1>
  </header>

  <nav>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">Services</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>

  <section>
    <article id="main-article">
      <h2>About Us</h2>
      <p id="description">We are excited to have you here!</p>
    </article>
    <button id="change-text">Change Text</button>
    <button id="toggle-element">Add/Remove Element</button>
  </section>

  <footer>
    <p>© 2025 My Website</p>
  </footer>

</body>
</html>


// Change text content dynamically
const title = document.getElementById('title');
const description = document.getElementById('description');
const changeTextBtn = document.getElementById('change-text');

changeTextBtn.addEventListener('click', () => {
  title.textContent = 'Thanks for Visiting!';
  description.textContent = 'Stay tuned for more updates!';
  // Modify CSS styles
  title.style.color = 'tomato';
  description.style.fontSize = '1.5rem';
});

// Add or remove an element
const toggleElementBtn = document.getElementById('toggle-element');
let newElement;

toggleElementBtn.addEventListener('click', () => {
  if (!newElement) {
    newElement = document.createElement('p');
    newElement.textContent = 'You clicked the button!';
    newElement.style.color = 'green';
    document.getElementById('main-article').appendChild(newElement);
  } else {
    newElement.remove();
    newElement = null;
  }
});
