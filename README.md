🍽 DelishBites – Sticky Blog Layout with CSS Grid

📙 Project Overview

DelishBites is a simple and responsive food blog page created using HTML5 and CSS3. The project was developed as part of a web development assignment to practice using CSS Grid layout and position: sticky for a fixed sidebar navigation.


---

🎯 Assignment Objective

Create a blog layout using CSS Grid with:

A sticky sidebar (position: sticky) that remains visible while scrolling.

A header at the top, sidebar on the left, main content on the right, and footer at the bottom.

Semantic tags and responsive design for mobile devices.



---

🧱 HTML Tags Used (with Explanation & Examples)

<!DOCTYPE html>

Declares the document as HTML5.

<!DOCTYPE html>

<html lang="en">

Root element of the page; lang="en" helps with accessibility.

<html lang="en">

<head>, <meta>, <title>, <link>

Used for metadata, page title, and linking CSS.

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>DelishBites-Food Blog</title>
  <link rel="stylesheet" href="style.css">
</head>

<body>

Wraps all visible content.

<body> ... </body>

<div class="container">

Main wrapper for the grid layout.

<div class="container"> ... </div>

<header>

Contains the blog title.

<header>🍽DelishBites Food Blog</header>

<aside>, <nav>, <ul>, <li>, <a>

Used for the sticky sidebar and navigation menu.

<aside>
  <nav class="sticky-sidebar">
    <ul>
      <li><a href="#breakfast">Breakfast</a></li>
    </ul>
  </nav>
</aside>

<main>

Main content area containing blog posts.

<main> ... </main>

<section>, <h2>, <img>, <p>

Each blog post section.

<section id="breakfast">
  <h2>🥞 Fluffy Pancakes for Breakfast</h2>
  <img src="..." alt="Pancakes">
  <p>Description of the recipe.</p>
</section>

<footer>

Footer at the bottom of the page.

<footer><p>&copy; 2025 DelishBites</p></footer>


---

🎨 CSS Concepts Used (with Explanation & Examples)

display: grid

Turns the container into a CSS Grid layout.

.container {
  display: grid;
}

grid-template-areas

Defines named areas for layout.

.container {
  grid-template-areas:
    "header header"
    "sidebar main"
    "footer footer";
}

grid-template-columns and grid-template-rows

Defines column widths and row heights.

.container {
  grid-template-columns: 250px 1fr;
  grid-template-rows: auto 1fr auto;
}

grid-area

Assigns elements to the defined grid areas.

header { grid-area: header; }
aside  { grid-area: sidebar; }
main   { grid-area: main; }
footer { grid-area: footer; }

position: sticky

Used to keep the sidebar visible while scrolling.

.sticky-sidebar {
  position: sticky;
  top: 1rem;
}

@media Query

Makes the layout responsive on smaller screens.

@media (max-width: 768px) {
  .container {
    grid-template-areas:
      "header"
      "sidebar"
      "main"
      "footer";
    grid-template-columns: 1fr;
  }
}

Additional Styling

transition and transform for image hover effects

background-color for visual sections

animation and @keyframes for section fade-in



---

📊 Layout Diagram

| Header             |
| Sidebar | Main     |
| Footer             |

On small screens:

| Header  |
| Sidebar |
| Main    |
| Footer  |


---

