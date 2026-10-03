# Holy Grail Layout with CSS Grid

A small layout project inspired by The Odin Project's Holy Grail layout assignment. The goal is to build a familiar web-page structure with CSS Grid: a header across the top, navigation and a sidebar around the main content, and a footer across the bottom.

## Layout

The page is organized into five regions:

- **Header** for the page title or site branding
- **Navigation** for links to other sections
- **Main content** for the primary page material
- **Sidebar** for supporting information or secondary links
- **Footer** for copyright or other page details

On a wide screen, the navigation and sidebar sit beside the main content. On a narrow screen, the regions should rearrange into a readable single-column layout.

## CSS Grid Approach

Use a grid container and named areas to describe the page structure. For example:

```css
.page {
  display: grid;
  grid-template-areas:
    "header header header"
    "nav main sidebar"
    "footer footer footer";
  grid-template-columns: 1fr 3fr 1fr;
  gap: 1rem;
}

header { grid-area: header; }
nav { grid-area: nav; }
main { grid-area: main; }
aside { grid-area: sidebar; }
footer { grid-area: footer; }
```

The area names connect each semantic HTML element to its place in the grid. A media query can redefine `grid-template-areas` and the columns for smaller screens.

## What This Project Practices

- Building page structure with semantic HTML
- Defining rows, columns, and spacing with CSS Grid
- Placing elements with named grid areas
- Making a multi-column layout responsive


## Credit

This exercise is based on the Holy Grail layout assignment in [The Odin Project](https://www.theodinproject.com/).