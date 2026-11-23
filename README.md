# Web Layout Starter Template (Vite + SCSS)

A clean, lightweight front-end starter template powered by **Vite** and **Sass (SCSS)**. Designed for rapid, scalable web layout development with a pre-configured build pipeline and utility functions.

## Tech Stack
- **Build Tool:** Vite
- **Styling:** Sass / SCSS (with custom `px` to `rem` conversion helper)
- **Markup & Scripting:** HTML5, Modern JavaScript (ES Modules)

---

## 1. Getting Started

1. Click **Use this template** ➔ **Create a new repository** on GitHub to initialize a fresh project without commit history.
2. Clone your new repository and install dependencies:
```bash
git clone https://github.com/Zeroqe/your-project-name.git
cd your-project-name
npm i
```
3. Start the local development server with Hot Module Replacement (HMR):
```bash
npm run dev
```

---

## 2. Dependency Management & Updates

Check for outdated packages in the project:
```bash
npm outdated
```

Update **Vite** to the latest version:
```bash
npm i -D vite@latest
```

Update **all dependencies** in `package.json` to their latest versions (including major releases):
```bash
npx npm-check-updates -u
npm i
```
*(After updating, verify the build via `npm run dev` and commit the updated `package.json` and `package-lock.json` files).*

---

## 3. Production Build & Git Workflow

Build optimized production-ready assets into the `dist/` directory:
```bash
npm run build
```

Stage, commit, and push changes to GitHub:
```bash
git add .
git commit -m "feat: describe your changes"
git push
```

---

## 4. Architecture & Built-in Utilities

- **`px` to `rem` Conversion (`src/sass/pxtorem.scss`):**
  Import the helper at the top of any `.scss` file using `@use "pxtorem" as *;` and pass unitless pixel values to the `rem()` function (e.g., `font-size: rem(18);` compiles to `1.125rem`).
- **Multi-Page Setup (`vite.config.js`):**
  To include additional HTML pages (e.g., `about.html`) in the production bundle, register them inside the `build.rollupOptions.input` object in `vite.config.js`.