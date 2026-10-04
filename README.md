# Responsive Design Lab

**Name:** Saida Khairova
**Group:** IT 2502

## Project structure and link

```
project/
├── index.html    # All five tasks (HTML structure + Bootstrap CDN links)
├── styles.css    # Custom CSS and media queries
└── README.md     # This report
```
Link : https://saeshaa.github.io/web3_folder/
## Breakpoints

| Device  | Width           | Used in            |
|---------|-----------------|--------------------|
| Mobile  | under 768px     | Tasks 0, 1, 4      |
| Tablet  | 768px – 1023px  | Tasks 0, 1, 4      |
| Desktop | 1024px and up   | Tasks 0, 1, 4      |

The custom CSS is written mobile-first: the default styles are for mobile, and `min-width` media queries add the tablet and desktop styles. Bootstrap uses its own breakpoints (`md` = 768px, `lg` = 992px) in Tasks 2–4.

## Task summary

### Part 1: Media Queries

**Task 0: Responsive Typography**
A page with headings and paragraphs whose font sizes change with screen width.

| Element   | Mobile  | Tablet  | Desktop |
|-----------|---------|---------|---------|
| Heading 1 | 1.6rem  | 2.2rem  | 3rem    |
| Heading 2 | 1.25rem | 1.6rem  | 2rem    |
| Paragraph | 0.95rem | 1.1rem  | 1.25rem |

**Task 1: Responsive Layout with Media Queries**
Three boxes laid out with CSS Flexbox only (no Bootstrap).
- Desktop: three boxes side by side
- Tablet: two boxes in a row, the third below
- Mobile: boxes stacked vertically

This works by changing the `flex-basis` of each box (`100%`, `50%`, `33.3%`) at each breakpoint.

### Part 2: Bootstrap Grid System

**Task 2: Bootstrap Responsive Columns**
Three columns using the classes `col-12 col-md-6 col-lg-4`.
- Desktop: each column takes 4 of 12 grid units (three equal parts)
- Tablet: two columns on the first row, one on the second
- Mobile: all columns stacked

**Task 3: Bootstrap Navigation Bar**
A navbar built with Bootstrap components (`navbar`, `navbar-expand-lg`, `navbar-toggler`, `collapse`).
- Logo on the left
- Links on the right (pushed with `ms-auto`)
- Collapses into a hamburger menu on screens below 992px

### Part 3: Combined Project

**Task 4: Responsive Portfolio Page**
A portfolio page that combines Bootstrap and custom media queries.

- **Header:** Bootstrap navbar with a collapsing menu.
- **Main section:**
  - Left (`col-lg-8`): project cards arranged with `row-cols-1 row-cols-md-2`.
  - Right (`col-lg-4`): sidebar with personal info and contact details.
- **Footer:** Full-width dark footer with copyright text.

Custom media queries adjust the following:

| Feature         | Mobile                    | Tablet               | Desktop                  |
|-----------------|---------------------------|----------------------|--------------------------|
| Font sizes      | Smallest                  | Medium               | Largest                  |
| Section spacing | Small padding             | Medium padding       | Large padding            |
| Intro text      | Hidden                    | Visible              | Visible                  |
| Bio paragraph   | Hidden                    | Hidden               | Visible                  |
| Sidebar         | Below the projects        | Below the projects   | Beside them, sticky      |
| Cards per row   | 1                         | 2                    | 2                        |

## Key concepts learned

- **Mobile-first design:** write the small-screen styles as the default, then add `min-width` queries for larger screens.
- **Viewport meta tag:** `<meta name="viewport" content="width=device-width, initial-scale=1">` is required for media queries to work properly on phones.
- **Bootstrap's 12-column grid:** the `col-*` classes let a layout change at different screen sizes without writing media queries.
- **Bootstrap + custom CSS together:** the custom stylesheet is loaded after Bootstrap so its rules can override Bootstrap's defaults.
- **Separating CSS from HTML:** linking an external `styles.css` keeps the structure and the presentation apart.
