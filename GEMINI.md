# Tennis Academy Website

A visually rich, responsive  website for a Tennis Academy, featuring program details, hero sections, and interactive elements.

## Project Overview

*   **Purpose:** Marketing and informational website for a sports academy specializing in tennis.
*   **Technologies:**
    *   **HTML5:** Structure and content.
    *   **CSS3:** Custom styles in `styles.css` using CSS variables for branding.
    *   **Tailwind CSS:** Used via CDN for utility-based styling.
    *   **Vanilla JavaScript:** Interactivity (mobile menu, smooth scroll, scroll animations).
    *   **Google Fonts:** Barlow and Barlow Condensed.

## Directory Structure

*   `code/`: Contains the source code.
    *   `index.html`: The main entry point.
    *   `styles.css`: Custom styling and theme variables.
    *   `main.js`: Client-side logic and animations.
*   `assets/`: Image assets used across the site.

## Design System

*   **Primary Color:** `#FF4F28` (Orange)
*   **Navy:** `#0d1b2e`
*   **Typography:** 'Barlow' (Body), 'Barlow Condensed' (Headings).

## Running the Project

Since this is a static website, you can view it by opening `code/index.html` in any modern web browser.

To run with a local server for better development experience:
*   Using Node.js: `npx serve code`
*   Using Python: `python3 -m http.server -d code`

## Local Server
- **Always serve on localhost** — never screenshot a `file:///` URL.
- Start the dev server: `node serve.mjs` (serves the project root at `http://localhost:3000`)
- `serve.mjs` lives in the project root. Start it in the background before taking any screenshots.
- If the server is already running, do not start a second instance.

## Development Conventions

## Screenshot Workflow (Linux)
- **Environment:** Puppeteer is in your project directory
- **Engine:** Puppeteer running Firefox.
- **Run:** `node screenshot.mjs http://localhost:3000 [optional-label]`
- **Storage:** `./temporary screenshots/screenshot-N.png` (auto-incremented).
- **Labeling:** `node screenshot.mjs http://localhost:3000 label` → `screenshot-N-label.png`
- **Execution:** `screenshot.mjs` is in project root.
- **Analysis:** After generation, use the Read tool to provide the PNG to the AI for visual diffing.
- **Review Criteria:** 
  * Spacing/Padding (px)
  * Typography (size/weight/line-height)
  * Colors (exact hex)
  * Component alignment & shadows
-  
- **Note:** Ensure your local dev server (Vite, Live Server, etc.) is running on port 3000 before executing.

### General
*   **Surgical Edits:** When modifying styles, prefer using the existing CSS variables in `:root`.
*   **Interactivity:** Keep JavaScript lightweight and dependency-free.
*   **Assets:** Place new images in the `assets/` directory and reference them using relative paths.
*   **Tailwind:** Use Tailwind utility classes for quick adjustments, but keep complex component styling in `styles.css`.

### Design & Workflow
*   **Invoke `frontend-design`:** Always invoke the `frontend-design` skill before writing any frontend code, every session, no exceptions.
*   **Reference Accuracy:** If a reference image is provided, match layout, spacing, typography, and color exactly. Swap in placeholders only for content. Do not "improve" the design.
*   **Asset Priority:** Always check the `assets/` folder before designing. Use existing logos and color palettes if available.
*   **Output Defaults:** Use Tailwind via CDN, `https://placehold.co/` for placeholders, and a mobile-first responsive approach.

### Anti-Generic Guardrails
*   **Colors:** Never use the default Tailwind palette. Use custom brand colors.
*   **Shadows:** Use layered, color-tinted shadows with low opacity.
*   **Typography:** Pair a display/serif with a clean sans. Use tight tracking for headings and generous line-height for body text.
*   **Depth & Layering:** Use an intentional layering system (base → elevated → floating).
*   **Animations:** Only animate `transform` and `opacity`. Avoid `transition-all`.
*   **Interactive States:** Every clickable element must have hover, focus-visible, and active states.
