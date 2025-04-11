# amandacdunbar.com Website

This is the codebase for the personal website of Amanda Dunbar, RMT Student Therapist.
Built with [Astro](https://astro.build/).

## Project Setup

1.  **Clone the repository:**
    ```bash
    git clone <repository-url>
    cd amandacdunbar-website
    ```
2.  **Install dependencies:**
    ```bash
    npm install
    ```
3.  **Run the development server:**
    ```bash
    npm run dev
    ```
    Visit `http://localhost:4321` in your browser.

4.  **Build for production:**
    ```bash
    npm run build
    ```
    The static site will be generated in the `dist/` directory, ready for deployment to services like Vercel or Netlify.

## Brand Guidelines

### Color Palette

-   Deep Teal: `var(--color-teal)` (#006d6f)
-   Soft Sand: `var(--color-sand)` (#f7f4f1)
-   Muted Blush: `var(--color-blush)` (#f6cfd6)
-   Midnight Navy: `var(--color-navy)` (#0e1724)
-   Accent Neon Violet: `var(--color-violet-accent)` (#8d4cff)

CSS variables are defined in `src/styles/global.css`.

### Typography

-   **Headings:** Playfair Display (600 weight) - `var(--font-heading)`
-   **Body:** Inter (400/500 weights) - `var(--font-body)`

Fonts are self-hosted using `@fontsource` packages.
Fluid typography steps are defined as CSS variables (e.g., `--step-0`, `--step-1`) in `src/styles/global.css`.

## Content Editing

Most text content can be edited directly within the `.astro` files located in `src/components/` and `src/pages/`. Look for the relevant section component (e.g., `src/components/Hero.astro` for the hero text).

-   **Hero Text:** Edit `src/components/Hero.astro`
-   **About Text & Badges:** Edit `src/components/About.astro`
-   **Treatment Focus Cards:** Edit `src/components/TreatmentFocus.astro` (titles) and potentially `src/components/FocusCard.astro` (structure).
-   **Clinic Info/Hours:** Edit `src/components/ClinicBooking.astro`
-   **Footer Links/Text:** Edit `src/components/Footer.astro`

## Images

-   Place images in the `public/` directory.
-   Reference them in components using a root-relative path (e.g., `/my-image.webp`).
-   Ensure images are optimized for the web (WebP format preferred, compressed).
-   Hero image should ideally be `< 350kB`.
-   Use descriptive `alt` text for all images for accessibility.

## Important Placeholders

Remember to replace the following placeholders before launch:

-   **Booking URL:** In `src/layouts/BaseLayout.astro` (JSON-LD script) and `src/components/Hero.astro` (CTA button).
-   **Clinic Address/Postal Code:** In `src/layouts/BaseLayout.astro` (JSON-LD script) if different from placeholder.
-   **Clinic Phone:** In `src/layouts/BaseLayout.astro` (JSON-LD script).
-   **Clinic Hours:** In `src/layouts/BaseLayout.astro` (JSON-LD script) and potentially `src/components/ClinicBooking.astro`.
-   **Portrait Image:** In `src/layouts/BaseLayout.astro` (JSON-LD script) and `src/components/Hero.astro`.
-   **Social Share Image:** In `src/layouts/BaseLayout.astro` (meta tags).
-   **Instagram URL:** In `src/components/Footer.astro`.
-   **Mailchimp Embed:** Add to `src/components/Footer.astro`.
-   **Privacy/Accessibility Pages:** Create actual pages or link appropriately in `src/components/Footer.astro`.
-   **Google Analytics ID:** Set up environment variable `PUBLIC_GA_TRACKING_ID` in your deployment platform (e.g., Vercel) and uncomment the GA script in `src/layouts/BaseLayout.astro` for production builds.
