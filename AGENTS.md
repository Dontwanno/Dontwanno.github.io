# AGENTS.md

## Project Overview
This is a personal portfolio website for an MSc Robotics student at TU Delft. 
It is built using the Astro web framework and deployed as a static site to GitHub Pages (`<username>.github.io`).

## Tech Stack
- **Framework:** Astro
- **Language:** TypeScript / Vanilla JavaScript
- **Styling:** Tailwind CSS
- **Content:** Markdown / MDX (used for robotics project showcases and posts)
- **Simulations:** HTML5 `<canvas>` + Vanilla JS (No heavy physics/UI libraries unless explicitly requested)

## Setup and Commands
- **Install dependencies:** `npm install`
- **Start local dev server:** `npm run dev`
- **Build for production:** `npm run build`
- **Check formatting/linting:** `npm run lint`

## Architecture & Code Conventions
- **Routing:** Use Astro's standard file-based routing in `src/pages/`.
- **Components:** Default to `.astro` components for all UI elements to keep the site lightweight. 
- **Robotics Visualizations & UI:** For interactive physics elements (e.g., pendulums, robotic arms, control loops in the UI), write custom lightweight simulations using `requestAnimationFrame` on an HTML5 `<canvas>` inside `.astro` files. Do not use libraries like Matter.js or heavy React components unless absolutely necessary.
- **Content Collections:** Portfolio projects and blog posts live in `src/content/`. Always validate that new Markdown/MDX files match the frontmatter schema defined in `src/content/config.ts`.
- **Assets:** Place optimized images or videos in `src/assets/` and use Astro's `<Image />` component. Public static files go in `public/`.

## Deployment Context (GitHub Pages)
- The site is hosted via GitHub Actions on GitHub Pages.
- When adding internal links or referencing assets, ensure they are compatible with the `site` and `base` path configurations defined in `astro.config.mjs`.

## Specific Instructions for Jules
- **Test Before Pushing:** Always run `npm run build` to verify that your changes do not break the static generation process before completing a task.
- **Accessibility & Speed:** Keep the design clean and accessible. Prioritize static HTML generation over client-side JavaScript for standard content.
- **Rigorous Mathematics:** When asked to create robotics-themed UI elements or simulations, apply accurate kinematics, dynamics, and control theory (e.g., LQR, PID). Treat the UI physics with the same mathematical rigor as a real robotics project. 
- **Contextual Awareness:** If asked to add a new project, scaffold the `.md` or `.mdx` file in the correct content collection directory with the required frontmatter (e.g., title, date, tech stack, GitHub link).