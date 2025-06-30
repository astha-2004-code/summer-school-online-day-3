# 🍽 DelishBites – Sticky Blog Layout with CSS Grid

## 📚 Project Overview

This project is a food blog named *DelishBites, built using **HTML5* and *CSS3* as part of a web development assignment. It demonstrates:

- A *responsive layout* using *CSS Grid*
- A *sticky sidebar* using position: sticky
- Semantic and accessible HTML tags
- Smooth scroll and fade-in animations

---


## 🧱 HTML Tags Used (With Explanation & Examples)

| Tag                            | Purpose / Why Used                                  | Example from Code                                           |
|--------------------------------|-----------------------------------------------------|-------------------------------------------------------------|
| !DOCTYPE html               | Declares document as HTML5                          | <!DOCTYPE html>                                             |
| html lang="en"               | Wraps whole document and sets language              | <html lang="en">                                            |
| head                        | Contains meta info, title, stylesheet link          | <head> ... </head>                                          |
| meta                         | Viewport and character encoding                     | <meta name="viewport" content="width=device-width...">      |
| title                       | Sets the browser tab title                          | <title>DelishBites-Food Blog</title>                        |
| link                        | Connects HTML to external CSS                       | <link rel="stylesheet" href="style.css"/>                   |
| body                       | Contains all visible page content                   | <body> ... </body>                                          |
| div class="container"       | Grid layout wrapper                                 | Wraps header, sidebar, main, and footer                     |
| header                  | Semantic tag for page header                        | <header>🍽DelishBites Food Blog</header>                    |
| aside                   | Represents sidebar content                          | <aside> ... </aside>                                        |
| nav                         | Holds navigation links                              | <nav class="sticky-sidebar"> ... </nav>                     |
| h3                         | Sub-heading for categories                          | <h3>🍴Categories</h3>                                       |
| ul                         | Unordered list for navigation links                 | <ul> ... </ul>                                              |
| li                       | List items for each category                        | <li><a href="#breakfast">Breakfast</a></li>                 |
| a                            | Anchor tag for navigation                           | <a href="#lunch">Lunch</a>                                  |
| main                        | Semantic tag for main content                       | <main> ... </main>                                          |
| section                      | Divides blog content into sections                  | <section id="desserts"> ... </section>                      |
| h2                           | Section headings                                    | <h2>🥞Fluffy Pancakes for Breakfast</h2>                    |
| img                         | Displays images of dishes                           | <img src="..." alt="Pancakes" />                             |
| p                            | Paragraphs of text                                  | <p>Start your day with fluffy pancakes...</p>                |
| footer                       | Page footer section                                 | <footer><p>&copy; 2025 DelishBites</p></footer>              |

---

## 🎨 CSS Properties and Selectors (With Reason and Use)

| Selector / Property           | Purpose / Why Used                                          | Example from CSS Code                         |
|------------------------------|--------------------------------------------------------------|-----------------------------------------------|
| *                          | Global reset for padding and margin                         | * { box-sizing: border-box; margin: 0; ...} |
| body                       | Sets font, background, and base color                       | body { font-family: 'Segoe UI'; ... }       |
| .container                 | Defines the grid structure for layout                       | Uses grid-template-areas                     |
| grid-template-areas       | Defines named grid layout sections                          | "header header", "sidebar main", ...         |
| grid-template-columns     | Sets sidebar width and main area to flexible space          | 250px 1fr                                    |
| position: sticky          | Keeps sidebar in view while scrolling                       | .sticky-sidebar { position: sticky; top: 1rem; } |
| section + @keyframes    | Adds scroll animation to content sections                   | fadeInUp animation used                     |
| main img                  | Makes images responsive with hover effects                   | img:hover { transform: scale(1.03); }       |
| media queries             | Makes layout responsive for mobile view                     | @media (max-width: 768px)                   |
| transition, transform   | Smooth hover and animation transitions                      | Sidebar and image hover                       |
| background-color          | Differentiates header, sidebar, main, and footer visually   | #ff7043, #ffe0b2, #fff8f0, etc.         |

---

## 🖼 Final Layout (Using Grid)

The layout is created using CSS Grid, which divides the page into 4 areas:

|  Header            |
|  Sidebar |  Main   |
|  Footer            |

This structure is implemented using these CSS Grid properties:


---

🔹 display: grid

This is used to define a grid container.

.container {
  display: grid;
}


---

🔹 grid-template-areas

This helps define named areas in the grid. It makes the layout easier to read and assign.

.container {
  grid-template-areas:
    "header header"
    "sidebar main"
    "footer footer";
}

This means:

The header takes two columns

Sidebar is on the left, main content on the right

Footer again takes full width



---

🔹 grid-template-columns and grid-template-rows

These define the size of columns and rows.

.container {
  grid-template-columns: 250px 1fr;   /* Sidebar = 250px, Main = remaining space */
  grid-template-rows: auto 1fr auto;  /* Auto for header/footer, main takes remaining */
}


---

🔹 grid-area

This assigns a specific area of the grid to each element (e.g., header, main, footer, sidebar):

header {
  grid-area: header;
}

aside {
  grid-area: sidebar;
}

main {
  grid-area: main;
}

footer {
  grid-area: footer;
}

Each element is placed in its respective named area defined in grid-template-areas.


---

📱 Responsive Grid (Using Media Query)

For smaller screens (like mobile), the layout changes into a single-column layout using this media query:

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



---
