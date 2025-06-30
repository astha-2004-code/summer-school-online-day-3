# 🍽 DelishBites – Sticky Blog Layout with CSS Grid

## 📚 Project Overview

This project is a food blog named *DelishBites, built using **HTML5* and *CSS3* as part of a web development assignment. It demonstrates:

- A *responsive layout* using *CSS Grid*
- A *sticky sidebar* using position: sticky
- Semantic and accessible HTML tags
- Smooth scroll and fade-in animations


## 🧱 HTML Tags Used (With Explanation & Examples)

Tag	Purpose / Why It’s Used	Example from Code

<!DOCTYPE html>	Declares the document as HTML5	<!DOCTYPE html>
<html lang="en">	Root element that wraps the whole document and sets the language to English	<html lang="en">
<head>	Contains meta information, title, and links to CSS	<head> ... </head>
<meta>	Provides metadata like character encoding and viewport settings	<meta charset="UTF-8">, <meta name="viewport" ...>
<title>	Sets the page title shown in the browser tab	<title>DelishBites-Food Blog</title>
<link>	Connects external CSS file to the HTML	<link rel="stylesheet" href="style.css" />
<body>	Wraps all the visible content on the page	<body> ... </body>
<div class="container">	Main wrapper for grid layout using CSS Grid	<div class="container"> ... </div>
<header>	Semantic tag for the top section (blog title)	<header>🍽DelishBites Food Blog</header>
<aside>	Contains sidebar content like the category links	<aside> ... </aside>
<nav>	Navigation section, used for the category menu	<nav class="sticky-sidebar"> ... </nav>
<h3>	Sidebar heading	<h3>🍴Categories</h3>
<ul>	Unordered list for sidebar links	<ul> ... </ul>
<li>	List item in the sidebar	<li><a href="#breakfast">Breakfast</a></li>
<a>	Anchor links that allow users to jump to sections	<a href="#lunch">Lunch</a>
<main>	Main blog content area	<main> ... </main>
<section>	Wraps each food post category like Breakfast, Lunch, etc.	<section id="desserts"> ... </section>
<h2>	Headings for individual blog post sections	<h2>🥞 Fluffy Pancakes for Breakfast</h2>
<img>	Displays images for each food section	<img src="..." alt="Pancakes" />
<p>	Paragraph description for each dish	<p>Start your day with fluffy pancakes served with syrup...</p>
<footer>	Bottom section of the blog, usually copyright info	<footer><p>&copy; 2025 DelishBites</p></footer>
---

## 🎨 CSS Properties and Selectors (With Reason and Use)

| Selector / Property           | Purpose / Why Used                                          | Example from CSS Code                             |
|-------------------------------|-------------------------------------------------------------|---------------------------------------------------|
| *                             | Global reset for padding and margin                         | * { box-sizing: border-box; margin: 0; ...}       |
| body                          | Sets font, background, and base color                       | body { font-family: 'Segoe UI'; ... }             |
| .container                    | Defines the grid structure for layout                       | Uses grid-template-areas                          |
| grid-template-areas           | Defines named grid layout sections                          | "header header", "sidebar main", ...              |
| grid-template-columns         | Sets sidebar width and main area to flexible space          | 250px 1fr                                         |
| position: sticky              | Keeps sidebar in view while scrolling                       | .sticky-sidebar { position: sticky; top: 1rem; }  |
| section + @keyframes          | Adds scroll animation to content sections                   | fadeInUp animation used                           |
| main img                      | Makes images responsive with hover effects                  | img:hover { transform: scale(1.03); }             |
| media queries                 | Makes layout responsive for mobile view                     | @media (max-width: 768px)                         |
| transition, transform         | Smooth hover and animation transitions                      | Sidebar and image hover                           |
| background-color              | Differentiates header, sidebar, main, and footer visually   | #ff7043, #ffe0b2, #fff8f0, etc.                   |

---

## 🖼 Final Layout (Using Grid)

The blog layout is created using CSS Grid to arrange the header, sidebar, main content, and footer in a clean structure.

🧩 Grid Structure

|  Header            |
|  Sidebar |  Main   |
|  Footer            |

This structure was built using the following grid properties:


🔹 display: grid

Defines the layout container as a grid.

.container {
  display: grid;
}


🔹 grid-template-areas

Defines named grid areas so elements can be placed easily.

.container {
  grid-template-areas:
    "header header"
    "sidebar main"
    "footer footer";
}

Here:

"header header" makes the header span both columns.

"sidebar main" places sidebar and main content side by side.

"footer footer" makes the footer full width again.


🔹 grid-template-columns & grid-template-rows

Specifies the size of columns and rows.

.container {
  grid-template-columns: 250px 1fr;
  grid-template-rows: auto 1fr auto;
}

First column (sidebar) is fixed at 250px

Second column (main) takes remaining space

Rows are: header, main area, and footer


🔹 grid-area

This assigns HTML elements to named areas defined above.

header   { grid-area: header; }
aside    { grid-area: sidebar; }
main     { grid-area: main; }
footer   { grid-area: footer; }


📱 Responsive Layout with Media Queries

The layout is fully responsive, and for screen widths below 768px, the grid layout becomes vertical using a media query.

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

All elements stack vertically on mobile

No horizontal scroll

Sidebar and content are easier to read


📌 Sticky Sidebar (Using position: sticky)

The navigation sidebar uses the position: sticky property so it stays fixed in place while scrolling the main content.

.sticky-sidebar {
  position: sticky;
  top: 1rem;
}

position: sticky makes the sidebar "stick" when it reaches top: 1rem from the top of the viewport.

It's better than fixed because it scrolls within its container.

This keeps navigation visible and user-friendly.
