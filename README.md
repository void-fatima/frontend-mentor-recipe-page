<div align="center">

# 🍳 Recipe Page

A clean, responsive, and accessible recipe page built with pure HTML and CSS.

[![HTML5](https://img.shields.io/badge/HTML5-semantic-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-responsive-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![Frontend Mentor](https://img.shields.io/badge/Frontend_Mentor-challenge-3F54A3?style=for-the-badge&logo=frontendmentor&logoColor=white)](https://www.frontendmentor.io/challenges/recipe-page-KiTsR8QQKm)

[View Challenge](https://www.frontendmentor.io/challenges/recipe-page-KiTsR8QQKm) · [GitHub Repository](https://github.com/void-fatima/frontend-mentor-recipe-page)

</div>

---

## Preview

![Desktop preview of the recipe page](./design/desktop-design.jpg)

This project is a solution to the **Recipe Page** challenge on Frontend Mentor. The goal was to recreate the provided omelette recipe design while practicing semantic HTML, mobile-first development, and responsive web design.

## Features

- Responsive layout for mobile and desktop screens
- Mobile-first implementation with a clear breakpoint
- Semantic elements such as `main`, `article`, `header`, `section`, `aside`, and `footer`
- Semantic table for nutritional information
- Locally hosted fonts with no external font dependency
- Centralized color palette using CSS custom properties
- BEM-style class naming
- No JavaScript, frameworks, or external dependencies

## Technologies Used

| Technology | Purpose |
|---|---|
| HTML5 | Semantic content structure |
| CSS3 | Styling, spacing, and responsive layout |
| `@font-face` | Loading the local Outfit and Young Serif fonts |
| CSS Custom Properties | Centralized color management |
| Media Queries | Adapting the layout for larger screens |

## Project Structure

```text
frontend-mentor-recipe-page/
├── assets/
│   ├── fonts/
│   │   ├── outfit/
│   │   │   ├── static/                   # Static Outfit font weights
│   │   │   ├── Outfit-VariableFont_wght.ttf
│   │   │   ├── OFL.txt                   # Font license
│   │   │   └── README.txt
│   │   └── young-serif/
│   │       ├── YoungSerif-Regular.ttf
│   │       └── OFL.txt                   # Font license
│   └── images/
│       ├── favicon-32x32.png             # Browser favicon
│       └── image-omelette.jpeg           # Main recipe image
├── design/
│   ├── desktop-design.jpg                # Desktop design reference
│   └── mobile-design.jpg                 # Mobile design reference
├── AGENTS.md                             # Guidance for coding assistants
├── CLAUDE.md                             # Guidance for Claude-based tools
├── index.html                            # Page structure and content
├── preview.jpg                           # Original challenge preview
├── README.md                             # Project documentation
├── style-guide.md                        # Design colors and typography
└── style.css                             # Complete page styling
```

## Page Structure

```text
body
├── main
│   └── article.recipe
│       ├── img.recipe__image
│       └── div.recipe__content
│           ├── header.recipe__header
│           │   ├── h1
│           │   └── p
│           ├── aside.preparation
│           │   ├── h2
│           │   └── ul
│           ├── section.recipe__section — Ingredients
│           ├── section.recipe__section — Instructions
│           └── section.recipe__section — Nutrition
│               └── table.nutrition-table
└── footer.attribution
```

## Getting Started

This project does not require any packages or build tools.

1. Clone the repository:

   ```bash
   git clone https://github.com/void-fatima/frontend-mentor-recipe-page.git
   ```

2. Enter the project directory:

   ```bash
   cd frontend-mentor-recipe-page
   ```

3. Open `index.html` directly in your browser.

Alternatively, if you use VS Code, right-click `index.html` and select **Open with Live Server**.

## Design Approach

The base styles are written for mobile screens first. At widths of `48rem` and above, a media query activates the desktop layout:

- The page background changes to a light cream color.
- The recipe card is centered on the page.
- The card receives a maximum width, internal spacing, and rounded corners.
- The main image also receives rounded corners.

The project's main colors are defined in `:root`, making them easy to maintain and update:

```css
:root {
  --white: hsl(0, 0%, 100%);
  --stone-100: hsl(30, 54%, 90%);
  --stone-600: hsl(30, 10%, 34%);
  --stone-900: hsl(24, 5%, 18%);
  --brown-800: hsl(14, 45%, 36%);
  --rose-50: hsl(330, 100%, 98%);
  --rose-800: hsl(332, 51%, 32%);
}
```

## What I Learned

- Separating content in HTML from presentation in CSS
- Choosing semantic elements based on the meaning of the content
- Creating ordered and unordered lists
- Building an accessible table with `th` and `scope="row"`
- Understanding the box model and managing `margin`, `padding`, and `border`
- Using relative units such as `rem` and `%`
- Loading local fonts with `@font-face`
- Building a responsive interface with media queries

## Accessibility

- The main image includes descriptive alternative text.
- The heading order from `h1` to `h2` preserves a logical document structure.
- Nutritional information is presented in a semantic table.
- `scope="row"` connects each row heading to its value for screen readers.
- Color contrast follows the palette provided with the challenge.

## Resources

- [Frontend Mentor Challenge](https://www.frontendmentor.io/challenges/recipe-page-KiTsR8QQKm)
- [MDN Web Docs — HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [MDN Web Docs — CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)

## Author

Built by [@void-fatima](https://github.com/void-fatima) as part of a Frontend Mentor learning challenge.

---

<div align="center">

If you found this project useful, consider giving it a ⭐.

</div>

---

**Author:** Fatima
