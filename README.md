# Everwind Ship Upgrades

A single-page, lightweight reference for **Everwind** ship upgrade costs—covering **Size**, **Speed**, and **Altitude** tiers—plus a running **Total Materials** legend. Built with plain HTML + CSS, no frameworks.

## Preview
Open `index.html` in any modern browser to view the page locally. The layout is a centered 3-column grid with upgrade rows on the left/middle and a materials legend on the right.

## Features
- **Zero-dependency static site** — just HTML and CSS.
- **Three upgrade panels**: Size, Speed, and Altitude (with per-tier material badges).  
- **Materials legend** that totals all required items and currency.
- **Responsive-ish grid** with tidy spacing and visual hierarchy.
- **Design tokens** via CSS custom properties (colors, radius, and a `--version-text` footer tag).

## Tech Stack
- **HTML5** (`index.html`) for structure.  
- **CSS** (`upgrades.css`) for layout, grid, and visual styling (variables, grid columns, badges).

## Getting Started
1. Clone the repository:
   ```bash
   git clone https://github.com/bcr666/everwind-ship-upgrade-materials.git
   cd everwind-ship-upgrade-materials
   ```

2. Open locally:
   - Double-click `index.html`, or
   - Serve it with a simple dev server:
   ```bash
   python3 -m http.server 8080
   ```

3. Check images: The page expects assets under `/images` (e.g., `forest-plank.png`, `copper-ingot.png`, `everwind-logo.png`, etc.).

## Project Structure
```
.
├── index.html
├── upgrades.css
├── README.md
└── images/
    ├── altitude.png
    ├── blue-crystal-dust.png
    ├── bronze-ingot.png
    ├── coin.png
    ├── copper-ingot.png
    ├── copper-nail.png
    ├── crystal-of-force.png
    ├── everwind-logo.png
    ├── forest-plank.png
    ├── iron-ingot.png
    ├── size.png
    └── speed.png
```

## How It Works
- **Grid Layout:** The main `.container` uses a 3-column grid sized to ~18rem per column, with small gaps for compactness.  
- **Panels:**  
  - **Size** and **Speed/Altitude** sections list tiers as `.row`s with a left-side header and right-side materials (each `.material` tile overlays a quantity via `data-quantity`).  
  - **Legend** on the right shows totals with an optional `--version-text` label appended as a pseudo-footer.
- **Design Tokens:** Colors, borders, and radius are centralized in `:root` variables. Update once to re-theme.

## Customization
- **Theme/Colors:** Edit the CSS variables in `upgrades.css`’s `:root` block.  
- **Version Tag:** Change or remove the `"Version: Demo"` label by updating `--version-text`.  
- **Add a Tier:** Duplicate a `.row` under the desired section in `index.html`.  
- **Adjust Layout:** Modify `.container` grid sizes or gaps.

## Accessibility & Notes
- Add `alt` text to images for screen readers.
- Numbers shown on materials come from `data-quantity` attributes (rendered via CSS `::after`).

## Deploying to GitHub Pages
1. Commit and push files.
2. In repo Settings → Pages, set Source = `main`, Folder = `/ (root)`.
3. Visit `https://<user>.github.io/<repo>/`.

## Roadmap
- Toggle between different totals (planned vs. completed).
- Add print style.
- Mobile layout.

## License
Choose a license (e.g., MIT).
