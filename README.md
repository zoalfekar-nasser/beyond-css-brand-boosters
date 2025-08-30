# BrandBoosters - Digital Marketing Agency Website

![BrandBoosters Homepage](/public/site-preview.png)

**Live Site:** [brandboosterskp.netlify.app](https://brandboosterskp.netlify.app)

---

## Project Overview

This is a complete, multi-page marketing website for a fictional agency, "BrandBoosters," built as a capstone project for **Kevin Powell's ["Beyond CSS"](https://beyondcss.dev/) course**.

The primary focus of this project is to implement a robust, scalable, and maintainable front-end architecture using a professional workflow. The core of the styling is powered by a custom **Design Token System** built with **Sass**, demonstrating modern CSS techniques for creating flexible and consistent user interfaces.

The project features three distinct pages, each showcasing different layout challenges and components:

- **Home Page:** An engaging landing page to introduce the agency.
- **Pricing Page:** A detailed breakdown of service plans, featuring a responsive comparison table.
- **About Page:** A look into the company's process and values, including an interactive tabs component.

## Key Learnings & Core Concepts

This project is a practical application of the concepts taught in the "Beyond CSS" course.

### 1. Advanced Sass Architecture (7-1 Pattern)

The project utilizes a modular and scalable Sass architecture based on the 7-1 pattern. This organizes the codebase into logical directories, making it easy to manage and extend.

```
src/sass/
|
|-- abstracts/    # Functions,colors, mixins, typography,  and design tokens (variables)
|-- base/         # Global styles, resets, and root
|-- components/   # Styles for individual components (buttons, cards, etc.)
|-- layout/       # Styles for page structure (header, footer, grid)
|-- pages/        # Page-specific styles
|-- utilities/    # Helper classes and utility classes
|
`-- style.scss    # Main entry point that imports all other files
```

### 2. Design Token System

The heart of the project's styling is a sophisticated design token system. Instead of hardcoding values, the entire design is built upon a foundation of reusable variables (tokens) for colors, spacing, fonts, and more.

- **Tokens as CSS Custom Properties:** Sass maps are used to generate a comprehensive set of CSS Custom Properties (`:root`), allowing for global control over the design system.
- **Contextual Variables:** "Contextual" tokens (e.g., `$button-primary-background-color`) are derived from the global "choice" tokens, making it simple to theme components or make site-wide design changes by updating a single source of truth.
- **Fluid Typography & Spacing:** `clamp()` is used extensively for font sizes and spacing, ensuring a smooth, fluid design that scales perfectly across all viewport sizes without requiring dozens of media queries.

### 3. Semantic & Accessible HTML

From the outset, the project prioritizes clean, semantic HTML and a high standard of accessibility.

- **Structural Integrity:** Proper use of landmark elements (`<header>`, `<main>`, `<footer>`), a logical heading hierarchy on every page, and self-contained sections.
- **WAI-ARIA Implementation:** For interactive components like the "Feature Benefits" tabs, the proper ARIA roles (`tablist`, `tab`, `tabpanel`) and states (`aria-selected`, `aria-controls`) are used to ensure they are fully accessible to screen reader users.
- **Accessibility Best Practices:** The project includes a "Skip to Main Content" link, descriptive `alt` text for all contextual images, and accessible naming for sections via `aria-labelledby`.

### 4. Modern Build Process with Vite

The project is built and optimized using **Vite**, a modern front-end build tool.

- **Multi-Page Configuration:** Vite is configured to handle multiple HTML entry points (`home`, `about`, `pricing`).
- **Asset Optimization:** `vite-plugin-image-optimizer` automatically compresses images to improve performance.
- **CSS Purging:** `vite-plugin-purgecss` scans the final HTML and JS to remove unused CSS, resulting in a smaller, faster stylesheet for production.

---

## Technical Stack

- **HTML5:** Structured with a focus on semantics and accessibility.
- **Sass (SCSS):** Advanced features like maps, functions, mixins, and a 7-1 architecture.
- **Vite:** For development server, builds, and optimizations.

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (version 18.x or higher recommended)

### Installation & Setup

1.  **Clone the repository:**

    ```sh
    git clone https://github.com/zoalfekar-nasser/beyond-css-brandboosters.git
    ```

2.  **Navigate to the project directory:**

    ```sh
    cd beyond-css-brandboosters
    ```

3.  **Install NPM packages:**
    ```sh
    npm install
    ```

### Running the Project

1.  **Start the development server:**

    ```sh
    npm run dev
    ```

    This command will start the Vite development server. You can view the project in your browser at `http://localhost:5173` (or the port Vite indicates).

2.  **Build for production:**
    ```sh
    npm run build
    ```
    This command will create a `dist` folder with the optimized, minified files ready for deployment.

---

## Acknowledgments

A huge thank you to **Kevin Powell** for the ["Beyond CSS"](https://beyondcss.dev/) course. The principles and techniques taught within are the foundation of this entire project, providing a roadmap for moving from writing simple CSS to architecting professional, enterprise-level front-end systems.
