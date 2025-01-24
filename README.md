# PurgeCSS removes dynamically added Tailwind CSS styles

This repository demonstrates a common issue when using PurgeCSS with Tailwind CSS: the removal of dynamically added styles.  When JavaScript adds Tailwind classes to elements, PurgeCSS might not detect these styles, leading to missing styles in the production build.

## Bug

The `bug.js` file shows how dynamically adding a Tailwind class using JavaScript results in the class not being applied after the PurgeCSS optimization.

## Solution

The `bugSolution.js` file presents a solution to retain these dynamically added styles.  It uses the `safelist` option in PurgeCSS to explicitly include the dynamic class or a pattern matching the dynamically generated classes to prevent their removal.

## Setup

1. Make sure you have Node.js and npm (or yarn) installed.
2. Clone this repository: `git clone https://github.com/yourusername/yourrepo`
3. Navigate to the project directory: `cd yourrepo`
4. Install dependencies: `npm install`
5. Run the app: `npm start` (or similar, depending on your project setup)